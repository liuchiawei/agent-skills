# Agent Skills

> 為 Cursor 整理的 AI Agent Skills 集合——個人前端開發知識與網路上的公開技能。

[English](../README.md) · [简体中文](README.zh-CN.md) · [日本語](README.ja.md)

---

## 簡介

本倉庫存放 **Agent Skills**（`.cursor/skills`），用來擴展 Cursor 的領域知識。每個 Skill 是帶有結構化元數據與指令的 Markdown 檔案，幫助 AI 助理在特定場景下寫出更好的程式碼。

**主要方向：**

- 🖥️ 前端網頁開發（React、Next.js、Three.js）
- 📱 React Native & Expo
- 🎮 3D / WebGL / MediaPipe
- 🌐 網頁設計與無障礙

---

## Skills 一覽

### 個人 Skills

| Skill                                                     | 說明                                                              |
| --------------------------------------------------------- | ----------------------------------------------------------------- |
| [google-3d-tiles-r3f](../skills/google-3d-tiles-r3f/)     | Google Maps 真實 3D Tiles 與 React Three Fiber，ECEF→ENU 座標轉換 |
| [mediapipe-usage](../skills/mediapipe-usage/)             | MediaPipe 手勢追蹤、姿勢估計與電腦視覺                            |
| [multiplayer-websocket](../skills/multiplayer-websocket/) | 使用 WebSocket 的即時多人連線模式                                 |

### 公開 Skills（來自社群）

| Skill                                                                 | 說明                                            |
| --------------------------------------------------------------------- | ----------------------------------------------- |
| [vercel-react-best-practices](../skills/vercel-react-best-practices/) | React & Next.js 效能優化（Vercel Engineering）  |
| [vercel-composition-patterns](../skills/vercel-composition-patterns/) | React 組合模式：複合元件、render props、context |
| [vercel-react-native-skills](../skills/vercel-react-native-skills/)   | React Native & Expo 行動應用最佳實踐            |
| [web-design-guidelines](../skills/web-design-guidelines/)             | 網頁介面指南，供 UI 審查與無障礙檢查            |

---

## 專案結構

```
agent-skills/
├── skills/                    # Skill 定義
│   ├── google-3d-tiles-r3f/   # 3D Tiles + R3F
│   ├── mediapipe-usage/       # MediaPipe
│   ├── multiplayer-websocket/ # WebSocket 多人連線
│   ├── vercel-composition-patterns/
│   ├── vercel-react-best-practices/
│   ├── vercel-react-native-skills/
│   └── web-design-guidelines/
├── docs/                      # 翻譯文件
│   ├── README.zh-CN.md        # 簡體中文
│   └── README.ja.md           # 日文
└── README.md
```

每個 skill 通常包含：

- `SKILL.md` – 主 Skill 定義與元數據、使用說明
- `reference.md` / `rules/` – 參考資料與規則

---

## 使用方式

1. 克隆或複製本倉庫。
2. 將 `skills/` 資料夾符號連結或複製到專案的 `.cursor/skills/` 目錄；或將本倉庫放在 `~/.cursor/skills/`，讓 Cursor 全域載入。
3. Cursor 會依照各 skill 的元數據與觸發條件自動載入。

更多設定說明請參考 [Cursor Docs: Skills](https://docs.cursor.com/context/agent-skills)。

---

## 貢獻

歡迎參與：

- 開 issue 建議新 skill 或改進。
- 提交 PR 新增 skill、修正或更新文件。

---

## 授權

各 skill 可能有不同授權（例如 Vercel 相關內容為 MIT）。請查看各 skill 目錄內的說明。
