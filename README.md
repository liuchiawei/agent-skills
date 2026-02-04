# Agent Skills

> A curated collection of AI Agent Skills for AI Agents—my personal frontend web dev knowledge and public skills from the community.

[English](README.md) · [简体中文](docs/README.zh-CN.md) · [日本語](docs/README.ja.md)

---

## Overview

This repository contains **Agent Skills** (`/skills`) that extend AI agents with domain-specific guidance. Skills are Markdown files with structured metadata and instructions that help AI assistants write better code in specific contexts.

**Focus areas:**

- 🖥️ Frontend web development (React, Next.js, Three.js)
- 📱 React Native & Expo
- 🎮 3D / WebGL / MediaPipe
- 🌐 Web design & accessibility

---

## Skills

### Personal Skills


| Skill                                                  | Description                                                                                |
| ------------------------------------------------------ | ------------------------------------------------------------------------------------------ |
| [google-3d-tiles-r3f](skills/google-3d-tiles-r3f/)     | Google Maps Photorealistic 3D Tiles with React Three Fiber, ECEF→ENU coordinate correction |
| [mediapipe-usage](skills/mediapipe-usage/)             | MediaPipe for hand tracking, pose estimation, and computer vision                          |
| [multiplayer-websocket](skills/multiplayer-websocket/) | Real-time multiplayer patterns with WebSocket                                              |


### Public Skills (from community)


| Skill                                                              | Description                                                           |
| ------------------------------------------------------------------ | --------------------------------------------------------------------- |
| [vercel-react-best-practices](skills/vercel-react-best-practices/) | React & Next.js performance optimization (Vercel Engineering)         |
| [vercel-composition-patterns](skills/vercel-composition-patterns/) | React composition patterns—compound components, render props, context |
| [vercel-react-native-skills](skills/vercel-react-native-skills/)   | React Native & Expo best practices for mobile apps                    |
| [web-design-guidelines](skills/web-design-guidelines/)             | Web Interface Guidelines for UI review and accessibility              |


---

## Project Structure

```
agent-skills/
├── skills/                    # Skill definitions
│   ├── google-3d-tiles-r3f/   # 3D Tiles + R3F
│   ├── mediapipe-usage/       # MediaPipe
│   ├── multiplayer-websocket/ # WebSocket multiplayer
│   ├── vercel-composition-patterns/
│   ├── vercel-react-best-practices/
│   ├── vercel-react-native-skills/
│   └── web-design-guidelines/
├── docs/                      # Translations
│   ├── README.zh-CN.md        # Chinese
│   └── README.ja.md           # Japanese
└── README.md
```

Each skill typically includes:

- `SKILL.md` – Main skill definition with metadata and instructions
- `reference.md` / `rules/` – Supporting references and rules

---

## Usage

1. Clone or copy this repository.
2. Symlink or copy the `skills/` folder into your project’s `.cursor/skills/` directory, or place the repo at `~/.cursor/skills/` so Cursor can load skills globally.
3. Cursor will automatically pick up skills based on their metadata and trigger conditions.

For detailed setup, see [Cursor Docs: Skills](https://docs.cursor.com/context/agent-skills).

---

## Contributing

Contributions are welcome:

- Open an issue to suggest new skills or improvements.
- Submit a PR for new skills, fixes, or documentation updates.

---

## License

Individual skills may have their own licenses (e.g., MIT for Vercel-derived content). Check each skill folder for details.