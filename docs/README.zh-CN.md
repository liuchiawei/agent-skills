# Agent Skills

> 為你的 AI 助手裝上「技能包」。本倉庫收錄精選的 **Agent Skills**——涵蓋前端、3D 與即時應用、程式品質與設計思維，兼有個人實戰與社群熱門技能。

[English](../README.md) · [简体中文](README.zh-CN.md) · [日本語](README.ja.md)

---

## 關於本倉庫

`/skills` 目錄下是讓 AI 具備領域知識的 **技能**。每個技能是一組帶有元數據與指示的 Markdown，幫助助理在該情境下寫出更好的程式碼。

**主題方向：**

- 🖥️ 前端（React、Next.js、Three.js）
- 📱 React Native 與行動端
- 🎮 3D、WebGL、MediaPipe
- ✨ UI/UX 與無障礙
- 🔧 程式品質、重構與程式碼審查

---

## 技能索引

簡短、一眼能懂的說明。連結指向各技能目錄。

### 3D 與即時 (`3d/`)

| 技能                                                                | 說明                                                          |
| --------------------------------------------------------- | ----------------------------------------------------------- |
| [3d-web-experience](../skills/3d/3d-web-experience/)       | 用 Three.js、R3F、WebGL、Spline 打造 3D 網頁體驗。                     |
| [google-3d-tiles-r3f](../skills/3d/google-3d-tiles-r3f/)   | 在 React Three Fiber 中使用 Google 真實 3D Tiles，並處理 ECEF→ENU 座標。 |
| [threejs-skills](../skills/3d/threejs-skills/)             | 在網頁中加入 3D 元素與互動。                                            |
| [mediapipe-usage](../skills/3d/mediapipe-usage/)           | 網頁上的 MediaPipe：姿勢與手部追蹤、關鍵點、即時影像。                            |
| [multiplayer-websocket](../skills/3d/multiplayer-websocket/) | 以 WebSocket 做即時多人：同步、hooks、訊息協定。                            |


### 前端與 React (`frontend/`)

| 技能                                                                          | 說明                                                       |
| --------------------------------------------------------------------- | -------------------------------------------------------- |
| [frontend-patterns](../skills/frontend/frontend-patterns/)             | React、Next.js、狀態、效能與 UI 的常見模式。                           |
| [frontend-dev-guidelines](../skills/frontend/frontend-dev-guidelines/) | React + TypeScript 開發規範：Suspense、MUI、TanStack Router、效能。 |
| [frontend-developer](../skills/frontend/frontend-developer/)           | 撰寫 React 元件與響應式版面。                                       |
| [react-ui-patterns](../skills/frontend/react-ui-patterns/)             | React 的載入、錯誤與資料取得模式。                                     |
| [vercel-react-best-practices](../skills/frontend/vercel-react-best-practices/) | React & Next.js 效能最佳實踐（Vercel Engineering）。              |
| [vercel-composition-patterns](../skills/frontend/vercel-composition-patterns/) | React 組合模式：複合元件、render props、context。                    |
| [tailwind-patterns](../skills/frontend/tailwind-patterns/)             | Tailwind CSS v4：CSS 優先設定、container queries、設計 token。     |
| [next-intl-app-router](../skills/frontend/next-intl-app-router/)       | 使用 next-intl 與 App Router 的 i18n。                             |


### UI/UX 與設計 (`design/`)

| 技能                                                                      | 說明                             |
| ----------------------------------------------------------- | ------------------------------ |
| [ui-ux-pro-max](../skills/design/ui-ux-pro-max/)             | UI/UX 設計：風格、色板、字型、技術棧、元件。      |
| [claude-frontend-design](../skills/design/claude-frontend-design/) | 有辨識度、可上線的前端介面與版面。              |
| [web-design-guidelines](../skills/design/web-design-guidelines/)   | 依網頁介面與無障礙準則審查 UI。              |
| [mobile-design](../skills/design/mobile-design/)             | iOS/Android 行動優先設計：觸控、效能、平台慣例。 |
| [scroll-experience](../skills/design/scroll-experience/)     | 捲動驅動與視差體驗、敘事式網頁。               |


### 程式品質與重構 (`refactor/`)

| 技能                                                                                      | 說明                   |
| ------------------------------------------------------------------------------- | -------------------- |
| [clean-code](../skills/refactor/clean-code/)                                     | 務實的程式風格：簡潔、直接、不過度設計。 |
| [code-refactoring-refactor-clean](../skills/refactor/code-refactoring-refactor-clean/)   | 朝乾淨程式碼與 SOLID 重構。    |
| [code-refactoring-tech-debt](../skills/refactor/code-refactoring-tech-debt/)             | 找出、量化並排定技術債優先順序。     |
| [code-refactoring-context-restore](../skills/refactor/code-refactoring-context-restore/) | 重構情境與語意記憶的還原。        |


### 程式碼審查 (`review/`)

| 技能                                                                          | 說明                 |
| --------------------------------------------------------------- | ------------------ |
| [code-reviewer](../skills/review/code-reviewer/)                 | 程式碼審查專家。           |
| [code-review-excellence](../skills/review/code-review-excellence/)     | 有效的程式碼審查與建設性回饋。    |
| [code-review-checklist](../skills/review/code-review-checklist/)       | 功能、安全、效能、可維護性審查清單。 |
| [code-review-ai-ai-review](../skills/review/code-review-ai-ai-review/) | 以 AI 輔助程式碼審查與靜態分析。 |


### 內容與行銷 (`content/`)

| 技能                                                      | 說明               |
| --------------------------------------------- | ---------------- |
| [copywriting](../skills/content/copywriting/)             | 撰寫與優化行銷、UI 文案。   |
| [brainstorming](../skills/content/brainstorming/)         | 把點子收斂成具體設計與下一步。  |
| [marketing-ideas](../skills/content/marketing-ideas/)     | SaaS 行銷策略與可行性評分。 |


### 資料與後端 (`backend/`)

| 技能                                                                  | 說明                                                |
| ----------------------------------------------------------- | ------------------------------------------------- |
| [backend-dev-guidelines](../skills/backend/backend-dev-guidelines/) | Node.js + Express + TypeScript 後端規範：分層、Prisma、Zod、Sentry、測試。 |
| [neon-postgres](../skills/backend/neon-postgres/)             | Neon 無伺服器 Postgres：分支、連線池、Prisma/Drizzle。             |
| [rag-implementation](../skills/backend/rag-implementation/)   | 為 LLM 建 RAG：向量、分塊、檢索。                            |

### 分析與轉化 (`analytics/`)

| 技能                                                              | 說明                                                |
| ----------------------------------------------------- | ------------------------------------------------- |
| [analytics-tracking](../skills/analytics/analytics-tracking/)   | 設計與審計分析（GA4、GTM、事件、轉化），產出可靠、可決策的數據。           |
| [page-cro](../skills/analytics/page-cro/)                       | 分析並優化頁面轉化；診斷表現不佳原因並給出可測試的建議。                  |

### 錯誤診斷與除錯 (`debug/`)

| 技能                                                                                          | 說明                                           |
| ------------------------------------------------------------------------------- | -------------------------------------------- |
| [error-diagnostics-error-analysis](../skills/debug/error-diagnostics-error-analysis/) | 除錯分散式系統、分析線上事故、根因分析與可觀測性。                 |
| [error-diagnostics-error-trace](../skills/debug/error-diagnostics-error-trace/)           | 建立錯誤追蹤、告警與結構化日誌，快速發現與處理線上問題。               |
| [error-diagnostics-smart-debug](../skills/debug/error-diagnostics-smart-debug/)           | AI 輔助除錯與現代化工具下的根因分析。                        |

### 行動端與工具 (`mobile/`)

| 技能                                                                              | 說明                                |
| ------------------------------------------------------------------- | --------------------------------- |
| [vercel-react-native-skills](../skills/mobile/vercel-react-native-skills/) | React Native & Expo 最佳實踐（Vercel）。 |
| [screenshots](../skills/mobile/screenshots/)                                       | 用 Playwright 產生 App 截圖（行銷、文件用）。   |
| [search-specialist](../skills/mobile/search-specialist/)                           | 進階網路搜尋與研究技巧。                      |


---

## 專案結構

```
agent-skills/
├── skills/           # 技能定義（SKILL.md，可選 reference / rules）
│   ├── 3d/           # 3D、WebGL、即時
│   ├── frontend/     # React、Next.js、Tailwind
│   ├── design/       # UI/UX、無障礙
│   ├── refactor/     # 乾淨程式碼、技術債
│   ├── review/       # 程式碼審查
│   ├── content/      # 文案、腦力激盪、行銷
│   ├── backend/      # Node、資料庫、RAG
│   ├── analytics/    # GA4、CRO、追蹤
│   ├── debug/        # 錯誤診斷
│   └── mobile/       # React Native、工具
├── docs/              # 翻譯
│   ├── README.zh-CN.md
│   └── README.ja.md
└── README.md
```

每個技能通常包含：

- `SKILL.md` – 主定義、元數據與使用說明
- `reference.md` / `rules/` – 參考與規則

---

## 使用方式

1. 克隆或複製本倉庫。
2. 將 `skills/` 符號連結或複製到專案的 `.cursor/skills/`；或放在 `~/.cursor/skills/` 供全域使用。
3. Cursor 會依元數據與觸發條件載入技能。

詳見 [Cursor Docs: Skills](https://docs.cursor.com/context/agent-skills)。

---

## 貢獻

- 歡迎開 issue 建議新技能或改進。
- 歡迎 PR 新增技能、修正或更新文件。

---

## 授權

各技能可能有不同授權（例如 Vercel 相關為 MIT）。請查看各技能目錄。