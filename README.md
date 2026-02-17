# Agent Skills

> Give your AI agent superpowers. A curated collection of **Agent Skills** for Cursor—frontend craft, 3D & real-time, code quality, and design intelligence, plus community favorites.

[English](README.md) · [简体中文](docs/README.zh-CN.md) · [日本語](docs/README.ja.md)

---

## What’s in here

This repo holds **skills** (in `/skills`) that teach AI agents domain-specific know-how. Each skill is a Markdown bundle with metadata and instructions so your assistant writes better code in that context.

**Themes:**

- 🖥️ Frontend (React, Next.js, Three.js)
- 📱 React Native & mobile
- 🎮 3D, WebGL, MediaPipe
- ✨ UI/UX and accessibility
- 🔧 Code quality, refactoring, and review

---

## Skills index

Short, at-a-glance list. Each link goes to the skill folder.

### 3D & real-time (`3d/`)

| Skill | What it does |
|-------|----------------|
| [3d-web-experience](skills/3d/3d-web-experience/) | Build 3D web experiences with Three.js, R3F, WebGL, Spline. |
| [google-3d-tiles-r3f](skills/3d/google-3d-tiles-r3f/) | Use Google Photorealistic 3D Tiles with React Three Fiber and ECEF→ENU coordinates. |
| [threejs-skills](skills/3d/threejs-skills/) | Add 3D elements and interactive 3D to the web. |
| [mediapipe-usage](skills/3d/mediapipe-usage/) | MediaPipe on the web: pose and hand tracking, landmarks, real-time video. |
| [multiplayer-websocket](skills/3d/multiplayer-websocket/) | Real-time multiplayer over WebSocket: sync, hooks, message protocol. |

### Frontend & React (`frontend/`)

| Skill | What it does |
|-------|----------------|
| [frontend-patterns](skills/frontend/frontend-patterns/) | Patterns for React, Next.js, state, performance, and UI. |
| [frontend-dev-guidelines](skills/frontend/frontend-dev-guidelines/) | Opinionated React + TypeScript standards: Suspense, MUI, TanStack Router, performance. |
| [frontend-developer](skills/frontend/frontend-developer/) | Build React components and responsive layouts. |
| [react-ui-patterns](skills/frontend/react-ui-patterns/) | Loading states, error handling, and data fetching in React. |
| [vercel-react-best-practices](skills/frontend/vercel-react-best-practices/) | React & Next.js performance (Vercel Engineering). |
| [vercel-composition-patterns](skills/frontend/vercel-composition-patterns/) | React composition: compound components, render props, context. |
| [tailwind-patterns](skills/frontend/tailwind-patterns/) | Tailwind CSS v4: CSS-first config, container queries, design tokens. |
| [next-intl-app-router](skills/frontend/next-intl-app-router/) | i18n with next-intl and App Router. |

### UI/UX & design (`design/`)

| Skill | What it does |
|-------|----------------|
| [ui-ux-pro-max](skills/design/ui-ux-pro-max/) | UI/UX design intelligence: styles, palettes, typography, stacks, components. |
| [claude-frontend-design](skills/design/claude-frontend-design/) | Distinctive, production-grade frontend interfaces and layouts. |
| [web-design-guidelines](skills/design/web-design-guidelines/) | Review UI against web interface and accessibility guidelines. |
| [mobile-design](skills/design/mobile-design/) | Mobile-first design for iOS/Android: touch, performance, platform conventions. |
| [scroll-experience](skills/design/scroll-experience/) | Scroll-driven and parallax experiences, cinematic storytelling. |

### Code quality & refactoring (`refactor/`)

| Skill | What it does |
|-------|----------------|
| [clean-code](skills/refactor/clean-code/) | Pragmatic coding: concise, direct, no over-engineering. |
| [code-refactoring-refactor-clean](skills/refactor/code-refactoring-refactor-clean/) | Refactor toward clean code and SOLID. |
| [code-refactoring-tech-debt](skills/refactor/code-refactoring-tech-debt/) | Find, measure, and prioritize technical debt. |
| [code-refactoring-context-restore](skills/refactor/code-refactoring-context-restore/) | Restore refactoring context and semantic memory. |

### Code review (`review/`)

| Skill | What it does |
|-------|----------------|
| [code-reviewer](skills/review/code-reviewer/) | Expert code review. |
| [code-review-excellence](skills/review/code-review-excellence/) | Effective code review and constructive feedback. |
| [code-review-checklist](skills/review/code-review-checklist/) | Checklist for functionality, security, performance, maintainability. |
| [code-review-ai-ai-review](skills/review/code-review-ai-ai-review/) | AI-powered code review and static analysis. |

### Content & marketing (`content/`)

| Skill | What it does |
|-------|----------------|
| [copywriting](skills/content/copywriting/) | Write and improve marketing and UI copy. |
| [brainstorming](skills/content/brainstorming/) | Turn ideas into concrete designs and next steps. |
| [marketing-ideas](skills/content/marketing-ideas/) | Marketing strategies for SaaS with feasibility scoring. |

### Data & backend (`backend/`)

| Skill | What it does |
|-------|----------------|
| [backend-dev-guidelines](skills/backend/backend-dev-guidelines/) | Node.js + Express + TypeScript backend standards: layers, Prisma, Zod, Sentry, testing. |
| [neon-postgres](skills/backend/neon-postgres/) | Neon serverless Postgres: branching, pooling, Prisma/Drizzle. |
| [rag-implementation](skills/backend/rag-implementation/) | Build RAG systems for LLMs: vectors, chunks, retrieval. |

### Analytics & conversion (`analytics/`)

| Skill | What it does |
|-------|----------------|
| [analytics-tracking](skills/analytics/analytics-tracking/) | Design and audit analytics (GA4, GTM, events, conversions) for reliable, decision-ready data. |
| [page-cro](skills/analytics/page-cro/) | Analyze and optimize pages for conversion; diagnose underperformance and recommend tests. |

### Error diagnostics & debugging (`debug/`)

| Skill | What it does |
|-------|----------------|
| [error-diagnostics-error-analysis](skills/debug/error-diagnostics-error-analysis/) | Debug distributed systems, analyze production incidents, root-cause and observability. |
| [error-diagnostics-error-trace](skills/debug/error-diagnostics-error-trace/) | Set up error tracking, alerts, and structured logging for production. |
| [error-diagnostics-smart-debug](skills/debug/error-diagnostics-smart-debug/) | AI-assisted debugging and root-cause analysis with modern tooling. |

### Mobile & tooling (`mobile/`)

| Skill | What it does |
|-------|----------------|
| [vercel-react-native-skills](skills/mobile/vercel-react-native-skills/) | React Native & Expo best practices (Vercel). |
| [screenshots](skills/mobile/screenshots/) | Generate app screenshots with Playwright for marketing or docs. |
| [search-specialist](skills/mobile/search-specialist/) | Advanced web research and search techniques. |

---

## Project structure

```
agent-skills/
├── skills/           # Skill definitions (each has SKILL.md + optional refs)
│   ├── 3d/           # 3D, WebGL, real-time
│   ├── frontend/     # React, Next.js, Tailwind
│   ├── design/       # UI/UX, accessibility
│   ├── refactor/     # Clean code, tech debt
│   ├── review/       # Code review
│   ├── content/      # Copy, brainstorming, marketing
│   ├── backend/      # Node, DB, RAG
│   ├── analytics/    # GA4, CRO, tracking
│   ├── debug/        # Error diagnostics
│   └── mobile/       # React Native, tooling
├── docs/             # Translations
│   ├── README.zh-CN.md
│   └── README.ja.md
└── README.md
```

Typical skill contents:

- `SKILL.md` – Main definition, metadata, and instructions
- `reference.md` / `rules/` – Extra references and rules

---

## How to use

1. Clone or copy this repo.
2. Symlink or copy the `skills/` folder into your project’s `.cursor/skills/`, or put the repo under `~/.cursor/skills/` for global use.
3. Cursor loads skills by metadata and trigger conditions.

See [Cursor Docs: Skills](https://docs.cursor.com/context/agent-skills) for setup details.

---

## Contributing

- Open an issue to suggest new skills or changes.
- Send a PR for new skills, fixes, or docs.

---

## License

Skills may have their own licenses (e.g. MIT for Vercel-derived content). Check each skill folder.
