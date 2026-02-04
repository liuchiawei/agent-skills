# Reference: Project Code Examples

This file contains relevant code from the Tokyo Sounds project for Google 3D Tiles, R3F, and ECEF→ENU 座標系 correction.

---

## 1. Config: Origin and Tiles URL

**File:** `src/config/tokyo-config.ts`

```ts
export const TOKYO_CENTER = {
  lat: 35.6762,
  lng: 139.6503,
  alt: 500, // starting altitude in meters
};

// Google Tiles API configuration
export const GOOGLE_TILES_CONFIG = {
  rootUrl: "https://tile.googleapis.com/v1/3dtiles/root.json",
  errorTarget: 12, // higher for photorealistic tiles
  maxDepth: 20,
};
```

Use one origin (e.g. `TOKYO_CENTER`) for the whole scene so ENU is consistent.

---

## 2. ECEF → ENU Matrix and TilesTransformer

**File:** `src/components/city/GoogleTilesScene.tsx`

Imports:

```ts
import { TilesRenderer, TilesPlugin } from "3d-tiles-renderer/r3f";
import { WGS84_ELLIPSOID } from "3d-tiles-renderer/three";
import {
  GoogleCloudAuthPlugin,
  GLTFExtensionsPlugin,
} from "3d-tiles-renderer/plugins";
```

Build ECEF→ENU matrix with Y-up remap (X=east, Y=up, Z=-north):

```ts
/**
 * Build an ECEF -> local frame matrix using library ENU and a Y-up remap.
 * - getEastNorthUpFrame returns ENU->ECEF (X=east, Y=north, Z=up).
 * - We invert it for ECEF->ENU.
 * - Then apply a remap to match Three.js Y-up world: X=east, Y=up, Z=-north.
 */
function createECEFtoENUMatrix(
  centerLat: number,
  centerLng: number,
): THREE.Matrix4 {
  const enuToECEF = new THREE.Matrix4();
  const latRad = THREE.MathUtils.degToRad(centerLat);
  const lngRad = THREE.MathUtils.degToRad(centerLng);
  WGS84_ELLIPSOID.getEastNorthUpFrame(latRad, lngRad, 0, enuToECEF); // ENU -> ECEF (radians)

  const ecefToENU = new THREE.Matrix4().copy(enuToECEF).invert(); // ECEF -> ENU (X=east, Y=north, Z=up)

  const enuToYUp = new THREE.Matrix4().set(
    1,
    0,
    0,
    0,
    0,
    0,
    1,
    0, // Y <- Z (up)
    0,
    -1,
    0,
    0, // Z <- -Y (north -> -Z)
    0,
    0,
    0,
    1,
  );

  const transformMatrix = new THREE.Matrix4().multiplyMatrices(
    enuToYUp,
    ecefToENU,
  );
  return transformMatrix;
}
```

Apply once to the group that wraps the tiles:

```ts
function TilesTransformer({
  children,
  groupRef,
}: {
  children: React.ReactNode;
  groupRef?: React.RefObject<THREE.Group | null>;
}) {
  const internalRef = useRef<THREE.Group>(null);
  const transformAppliedRef = useRef(false);
  const ref = groupRef || internalRef;

  useEffect(() => {
    if (ref.current && !transformAppliedRef.current) {
      const transformMatrix = createECEFtoENUMatrix(
        TOKYO_CENTER.lat,
        TOKYO_CENTER.lng
      );
      ref.current.matrix.copy(transformMatrix);
      ref.current.matrixAutoUpdate = false;
      transformAppliedRef.current = true;
    }
  }, [ref]);

  return <group ref={ref as React.RefObject<THREE.Group>}>{children}</group>;
}
```

Scene usage: wrap `TilesRenderer` with the transformer and plugins:

```tsx
<TilesTransformer groupRef={tilesGroupRef}>
  <TilesRenderer
    onLoadTileSet={handleLoadTileset}
    onLoadError={handleLoadError}
    onLoadModel={handleLoadModel}
  >
    <TilesPlugin
      plugin={GLTFExtensionsPlugin}
      args={{ dracoLoader: getDRACOLoader() }}
    />
    <TilesPlugin plugin={GoogleCloudAuthPlugin} args={{ apiToken: apiKey }} />
  </TilesRenderer>
</TilesTransformer>
```

---

## 3. Geo Utils: Lat/Lng/Alt ↔ ECEF ↔ ENU

**File:** `src/lib/geo-utils.ts`

WGS84 constants:

```ts
const WGS84_A = 6378137.0; // Semi-major axis (m)
const WGS84_B = 6356752.314245; // Semi-minor axis (m)
const WGS84_E2 = 1 - (WGS84_B * WGS84_B) / (WGS84_A * WGS84_A);
```

Geodetic → ECEF:

```ts
export function latLngAltToECEF(
  lat: number,
  lng: number,
  alt: number = 0,
): THREE.Vector3 {
  const latRad = THREE.MathUtils.degToRad(lat);
  const lngRad = THREE.MathUtils.degToRad(lng);
  const sinLat = Math.sin(latRad);
  const cosLat = Math.cos(latRad);
  const N = WGS84_A / Math.sqrt(1 - WGS84_E2 * sinLat * sinLat);

  const x = (N + alt) * cosLat * Math.cos(lngRad);
  const y = (N + alt) * cosLat * Math.sin(lngRad);
  const z = (N * (1 - WGS84_E2) + alt) * sinLat;

  return new THREE.Vector3(x, y, z);
}
```

Geodetic → ENU (same Y-up as tiles: X=east, Y=up, Z=-north):

```ts
export function latLngAltToENU(
  lat: number,
  lng: number,
  alt: number,
  originLat: number,
  originLng: number,
  originAlt: number = 0,
): THREE.Vector3 {
  const pointECEF = latLngAltToECEF(lat, lng, alt);
  const originECEF = latLngAltToECEF(originLat, originLng, originAlt);
  const diff = pointECEF.clone().sub(originECEF);

  const latRad = THREE.MathUtils.degToRad(originLat);
  const lngRad = THREE.MathUtils.degToRad(originLng);
  const sinLat = Math.sin(latRad);
  const cosLat = Math.cos(latRad);
  const sinLng = Math.sin(lngRad);
  const cosLng = Math.cos(lngRad);

  const east = -sinLng * diff.x + cosLng * diff.y;
  const north =
    -sinLat * cosLng * diff.x - sinLat * sinLng * diff.y + cosLat * diff.z;
  const up =
    cosLat * cosLng * diff.x + cosLat * sinLng * diff.y + sinLat * diff.z;

  // Remap to Three.js Y-up: X=east, Y=up, Z=-north (match GoogleTilesScene enuToYUp)
  return new THREE.Vector3(east, up, -north);
}
```

ENU → Geodetic (inverse of above convention):

```ts
export function enuToLatLngAlt(
  enu: THREE.Vector3,
  originLat: number,
  originLng: number,
  originAlt: number = 0,
): { lat: number; lng: number; alt: number } {
  const east = enu.x;
  const up = enu.y;
  const north = -enu.z; // Y-up remap: Z=-north

  const latRad = THREE.MathUtils.degToRad(originLat);
  const lngRad = THREE.MathUtils.degToRad(originLng);
  const sinLat = Math.sin(latRad);
  const cosLat = Math.cos(latRad);
  const sinLng = Math.sin(lngRad);
  const cosLng = Math.cos(lngRad);

  const dx = -sinLng * east - sinLat * cosLng * north + cosLat * cosLng * up;
  const dy = cosLng * east - sinLat * sinLng * north + cosLat * sinLng * up;
  const dz = cosLat * north + sinLat * up;

  const originECEF = latLngAltToECEF(originLat, originLng, originAlt);
  const pointECEF = new THREE.Vector3(
    originECEF.x + dx,
    originECEF.y + dy,
    originECEF.z + dz,
  );

  return ecefToLatLngAlt(pointECEF);
}
```

Use the **same** `originLat` / `originLng` as in `createECEFtoENUMatrix` (e.g. `TOKYO_CENTER`).

---

## 4. Page: Canvas and GoogleTilesScene

**File:** `src/app/(index)/page.tsx`

```tsx
import { Canvas } from "@react-three/fiber";
import { GoogleTilesScene } from "@/components/city/GoogleTilesScene";

// ...

<Canvas
  shadows="soft"
  camera={{
    position: initialCameraPosition, // ENU position from latLngAltToENU(INITIAL_CAMERA, TOKYO_CENTER)
    fov: 60,
    near: 1,
    far: 1e9,
  }}
  gl={{
    logarithmicDepthBuffer: true,
    antialias: false,
    powerPreference: "high-performance",
  }}
>
  <Suspense fallback={<Loader />}>
    <GoogleTilesScene
      apiKey={ENV_MAPS_API_KEY}
      onTilesLoaded={handleTilesLoaded}
      onStatusChange={setStatus}
      collisionGroupRef={collisionGroupRef}
    />
    {/* Other R3F objects (e.g. PlaneController) use ENU positions from latLngAltToENU */}
  </Suspense>
</Canvas>;
```

Initial camera position should be computed with `latLngAltToENU(INITIAL_CAMERA.lat, INITIAL_CAMERA.lng, INITIAL_CAMERA.alt, TOKYO_CENTER.lat, TOKYO_CENTER.lng, 0)` so it matches the transformed tiles.

---

## 5. Summary: 座標系 Consistency

| Item                         | Coordinate system                                              |
| ---------------------------- | -------------------------------------------------------------- |
| Google 3D Tiles (raw)        | ECEF                                                           |
| Tiles after TilesTransformer | ENU at origin, Y-up (X=east, Y=up, Z=-north)                   |
| Camera / entities / audio    | ENU via `latLngAltToENU(..., originLat, originLng, originAlt)` |

Keep **one** origin (e.g. `TOKYO_CENTER`) and use it in both `createECEFtoENUMatrix` and every `latLngAltToENU` / `enuToLatLngAlt` call.
