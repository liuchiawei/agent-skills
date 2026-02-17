# Agent Skills

> AI エージェントに「スキル」を追加。厳選した **Agent Skills** コレクション——フロントエンド、3D・リアルタイム、コード品質、デザインまで、個人ノウハウとコミュニティの定番をまとめました。

[English](../README.md) · [简体中文](README.zh-CN.md) · [日本語](README.ja.md)

---

## このリポジトリについて

`/skills` には、AI エージェントに分野別の知識を教える **スキル** が入っています。各スキルはメタデータと指示を含む Markdown のまとまりで、その文脈でより良いコードを書く手助けをします。

**テーマ：**

- 🖥️ フロントエンド（React、Next.js、Three.js）
- 📱 React Native とモバイル
- 🎮 3D、WebGL、MediaPipe
- ✨ UI/UX とアクセシビリティ
- 🔧 コード品質・リファクタ・レビュー

---

## スキル一覧

ひと目で分かる短い説明です。リンク先は各スキルのフォルダです。

### 3D・リアルタイム (`3d/`)

| スキル                                                                 | 内容                                                            |
| --------------------------------------------------------- | ------------------------------------------------------------- |
| [3d-web-experience](../skills/3d/3d-web-experience/)       | Three.js、R3F、WebGL、Spline で 3D Web 体験を構築。                     |
| [google-3d-tiles-r3f](../skills/3d/google-3d-tiles-r3f/)  | Google フォトリアル 3D Tiles を React Three Fiber で使い、ECEF→ENU 座標対応。 |
| [threejs-skills](../skills/3d/threejs-skills/)             | Web に 3D 要素とインタラクティブな 3D を追加。                                 |
| [mediapipe-usage](../skills/3d/mediapipe-usage/)           | Web 上の MediaPipe：ポーズ・手のトラッキング、ランドマーク、リアルタイム動画。                |
| [multiplayer-websocket](../skills/3d/multiplayer-websocket/) | WebSocket によるリアルタイムマルチプレイヤー：同期、フック、メッセージプロトコル。                |


### フロントエンド・React (`frontend/`)

| スキル                                                                             | 内容                                                               |
| --------------------------------------------------------------------- | ---------------------------------------------------------------- |
| [frontend-patterns](../skills/frontend/frontend-patterns/)             | React、Next.js、状態、パフォーマンス、UI のパターン。                               |
| [frontend-dev-guidelines](../skills/frontend/frontend-dev-guidelines/) | React + TypeScript のスタンダード：Suspense、MUI、TanStack Router、パフォーマンス。 |
| [frontend-developer](../skills/frontend/frontend-developer/)           | React コンポーネントとレスポンシブレイアウトの構築。                                    |
| [react-ui-patterns](../skills/frontend/react-ui-patterns/)             | React のローディング、エラー、データ取得パターン。                                     |
| [vercel-react-best-practices](../skills/frontend/vercel-react-best-practices/) | React & Next.js のパフォーマンス（Vercel Engineering）。                    |
| [vercel-composition-patterns](../skills/frontend/vercel-composition-patterns/) | React のコンポジション：複合コンポーネント、render props、context。                   |
| [tailwind-patterns](../skills/frontend/tailwind-patterns/)             | Tailwind CSS v4：CSS ファースト設定、コンテナクエリ、デザイントークン。                    |
| [next-intl-app-router](../skills/frontend/next-intl-app-router/)       | next-intl と App Router による i18n。                                          |


### UI/UX・デザイン (`design/`)

| スキル                                                                     | 内容                                             |
| ----------------------------------------------------------- | ---------------------------------------------- |
| [ui-ux-pro-max](../skills/design/ui-ux-pro-max/)             | UI/UX デザイン：スタイル、パレット、タイポグラフィ、スタック、コンポーネント。     |
| [claude-frontend-design](../skills/design/claude-frontend-design/) | 個性ある本番品質のフロントエンド UI・レイアウト。                     |
| [web-design-guidelines](../skills/design/web-design-guidelines/)   | Web インターフェース・アクセシビリティに沿った UI レビュー。             |
| [mobile-design](../skills/design/mobile-design/)             | iOS/Android のモバイルファースト：タッチ、パフォーマンス、プラットフォーム慣習。 |
| [scroll-experience](../skills/design/scroll-experience/)     | スクロール連動・パララックス、シネマティックなストーリー体験。                |


### コード品質・リファクタ (`refactor/`)

| スキル                                                                                     | 内容                        |
| ------------------------------------------------------------------------------- | ------------------------- |
| [clean-code](../skills/refactor/clean-code/)                                     | 実践的なコーディング：簡潔で直接的、過剰設計なし。 |
| [code-refactoring-refactor-clean](../skills/refactor/code-refactoring-refactor-clean/)   | クリーンコード・SOLID に向けたリファクタ。  |
| [code-refactoring-tech-debt](../skills/refactor/code-refactoring-tech-debt/)             | 技術的負債の特定・定量化・優先順位付け。      |
| [code-refactoring-context-restore](../skills/refactor/code-refactoring-context-restore/) | リファクタの文脈・セマンティックメモリの復元。   |


### コードレビュー (`review/`)

| スキル                                                                         | 内容                             |
| --------------------------------------------------------------- | ------------------------------ |
| [code-reviewer](../skills/review/code-reviewer/)                 | コードレビュー専門。                     |
| [code-review-excellence](../skills/review/code-review-excellence/)     | 効果的なコードレビューと建設的フィードバック。        |
| [code-review-checklist](../skills/review/code-review-checklist/)       | 機能・セキュリティ・パフォーマンス・保守性のチェックリスト。 |
| [code-review-ai-ai-review](../skills/review/code-review-ai-ai-review/) | AI を活用したコードレビューと静的解析。          |


### コンテンツ・マーケティング (`content/`)

| スキル                                                      | 内容                      |
| --------------------------------------------- | ----------------------- |
| [copywriting](../skills/content/copywriting/)             | マーケ・UI のコピーを書く・改善する。    |
| [brainstorming](../skills/content/brainstorming/)         | アイデアを具体的な設計・次の一手に落とし込む。 |
| [marketing-ideas](../skills/content/marketing-ideas/)     | SaaS 向けマーケ戦略と実行可能性スコア。  |


### データ・バックエンド (`backend/`)

| スキル                                                                  | 内容                                                    |
| ----------------------------------------------------------- | ----------------------------------------------------- |
| [backend-dev-guidelines](../skills/backend/backend-dev-guidelines/) | Node.js + Express + TypeScript バックエンド標準：レイヤ、Prisma、Zod、Sentry、テスト。 |
| [neon-postgres](../skills/backend/neon-postgres/)             | Neon サーバーレス Postgres：ブランチ、プール、Prisma/Drizzle。             |
| [rag-implementation](../skills/backend/rag-implementation/)   | LLM 向け RAG：ベクトル、チャンク、検索の実装。                            |

### 分析・コンバージョン (`analytics/`)

| スキル                                                              | 内容                                                          |
| --------------------------------------------------------- | ----------------------------------------------------------- |
| [analytics-tracking](../skills/analytics/analytics-tracking/)       | GA4・GTM・イベント・コンバージョンの設計・監査。信頼できる意思決定用データを目指す。        |
| [page-cro](../skills/analytics/page-cro/)                           | ページのコンバージョン分析・改善。成果の出ない原因診断とテスト可能な提案。              |

### エラー診断・デバッグ (`debug/`)

| スキル                                                                                              | 内容                                               |
| --------------------------------------------------------------------------------- | ------------------------------------------------ |
| [error-diagnostics-error-analysis](../skills/debug/error-diagnostics-error-analysis/)   | 分散システムのデバッグ、本番障害分析、原因追究とオブザーバビリティ。         |
| [error-diagnostics-error-trace](../skills/debug/error-diagnostics-error-trace/)           | エラー追跡・アラート・構造化ログの構築。本番問題の早期発見と対応。           |
| [error-diagnostics-smart-debug](../skills/debug/error-diagnostics-smart-debug/)           | AI 支援デバッグとモダンなツールによる原因分析。                    |

### モバイル・ツール (`mobile/`)

| スキル                                                                              | 内容                                         |
| ------------------------------------------------------------------- | ------------------------------------------ |
| [vercel-react-native-skills](../skills/mobile/vercel-react-native-skills/) | React Native & Expo のベストプラクティス（Vercel）。    |
| [screenshots](../skills/mobile/screenshots/)                                        | Playwright でアプリのスクリーンショットを生成（マーケ・ドキュメント用）。 |
| [search-specialist](../skills/mobile/search-specialist/)                            | 高度な Web リサーチと検索手法。                         |


---

## プロジェクト構成

```
agent-skills/
├── skills/           # スキル定義（SKILL.md + 必要に応じて reference / rules）
│   ├── 3d/           # 3D、WebGL、リアルタイム
│   ├── frontend/     # React、Next.js、Tailwind
│   ├── design/       # UI/UX、アクセシビリティ
│   ├── refactor/     # クリーンコード、技術的負債
│   ├── review/       # コードレビュー
│   ├── content/      # コピー、ブレスト、マーケティング
│   ├── backend/      # Node、DB、RAG
│   ├── analytics/    # GA4、CRO、トラッキング
│   ├── debug/        # エラー診断
│   └── mobile/       # React Native、ツール
├── docs/              # 翻訳
│   ├── README.zh-CN.md
│   └── README.ja.md
└── README.md
```

スキルには通常以下が含まれます：

- `SKILL.md` – メイン定義・メタデータ・指示
- `reference.md` / `rules/` – 参考資料・ルール

---

## 使い方

1. このリポジトリをクローンまたはコピーする。
2. `skills/` をプロジェクトの `.cursor/skills/` にシンボリックリンクまたはコピー。または `~/.cursor/skills/` に置いてグローバルに利用。
3. Cursor がメタデータとトリガー条件に基づいてスキルを読み込む。

詳しくは [Cursor Docs: Skills](https://docs.cursor.com/context/agent-skills) を参照。

---

## 貢献

- 新規スキルや改善案は issue で提案してください。
- スキル追加・修正・ドキュメント更新は PR で送ってください。

---

## ライセンス

各スキルは個別のライセンスを持つ場合があります（例：Vercel 由来は MIT）。各スキルフォルダを確認してください。