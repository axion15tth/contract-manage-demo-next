# 契約管理APP - モックアップ

不動産契約管理システムのUIモックアップです。HTMLとCSSのみで動作し、実際のデータベースやAPIは不要です。

## 🚀 クイックスタート

### 方法1: 簡易サーバーで起動（推奨）

**Python 3を使う場合:**
```bash
cd mockup
python3 -m http.server 8080
```

**Node.jsを使う場合:**
```bash
cd mockup
npx http-server -p 8080
```

ブラウザで `http://localhost:8080/01-login.html` を開いてください。

### 方法2: 直接ファイルを開く

```bash
cd mockup
open 01-login.html  # macOS
start 01-login.html # Windows
xdg-open 01-login.html # Linux
```

## 📱 画面一覧

### 認証
- **01-login.html** - ログイン画面

### メイン機能
- **02-dashboard.html** - ダッシュボード（主要機能へのアクセス、簡易カレンダー）
- **05-upload.html** - 契約書登録（PDFアップロード、処理状況）
- **03-contract-list.html** - 契約検索（通常検索タブ）
- **09-rag-search.html** - 契約検索（AI検索タブ）
- **08-rentroll.html** - レントロール作成
- **10-ai-analysis.html** - AI契約分析
- **07-calendar.html** - 期限管理

### サブ画面
- **04-contract-detail.html** - 契約詳細
- **06-verification.html** - AI抽出結果の検証

## 🎨 デザイン

- **カラースキーム**: 青系を基調、赤系をアクセント
- **フォント**: システムフォント（-apple-system, BlinkMacSystemFont, Segoe UI）
- **レスポンシブ**: デスクトップ・タブレット対応
- **スタイル**: `style.css` で全画面共通スタイルを管理

## 🔄 画面遷移フロー

```
ログイン (01-login.html)
    ↓
ダッシュボード (02-dashboard.html)
    │
    ├─→ 契約書登録 (05-upload.html)
    │       ↓
    │   検証画面 (06-verification.html)
    │
    ├─→ 契約検索 (03-contract-list.html / 09-rag-search.html)
    │       ↓
    │   契約詳細 (04-contract-detail.html)
    │
    ├─→ レントロール作成 (08-rentroll.html)
    │
    ├─→ AI契約分析 (10-ai-analysis.html)
    │
    └─→ 期限管理 (07-calendar.html)
```

## ✨ 主要機能

### 1. 契約書登録
- ドラッグ&ドロップでPDFアップロード
- リアルタイム処理状況表示（プログレスバー）
- OCR処理 → AI抽出 → 検証のフロー

### 2. 契約検索
- **通常検索**: キーワード・フィルタによる検索
- **AI検索**: 自然言語での質問（RAG）
- タブ切り替えで両方の検索方法を利用可能

### 3. レントロール作成
- 出力条件の詳細設定
- プレビュー機能
- Excel/CSV/PDF出力

### 4. AI契約分析
- 対話形式でデータ分析
- 統計計算・グラフ表示
- 分析履歴の保存

### 5. 期限管理
- カレンダー表示
- 契約満了・更新期限の可視化
- 今月のイベント一覧

## 📂 ファイル構成

```
mockup/
├── 01-login.html          # ログイン
├── 02-dashboard.html      # ダッシュボード
├── 03-contract-list.html  # 契約検索（通常）
├── 04-contract-detail.html # 契約詳細
├── 05-upload.html         # 契約書登録
├── 06-verification.html   # 検証画面
├── 07-calendar.html       # 期限管理
├── 08-rentroll.html       # レントロール
├── 09-rag-search.html     # 契約検索（AI）
├── 10-ai-analysis.html    # AI分析
├── style.css              # 共通スタイル
└── README.md              # このファイル
```

## 🌐 対応ブラウザ

- Chrome 100+
- Safari 15+
- Edge 100+
- Firefox 100+

## 📝 注意事項

- このモックアップは静的なHTMLファイルです
- データの保存・更新などの機能は実装されていません
- デモ目的のサンプルデータが表示されます

## 🔧 カスタマイズ

`style.css` を編集することで、全画面のデザインを一括変更できます。

### 主要なカラー変数
```css
/* ヘッダー */
background: #1a365d;

/* プライマリカラー（ボタン等） */
background: #3182ce;

/* 背景 */
background: #f8f9fa;
```

## 📄 ライセンス

このモックアップは要件定義に基づいて作成されたデモンストレーション用のUIです。
