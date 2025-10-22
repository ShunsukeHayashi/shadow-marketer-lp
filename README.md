# シャドーマーケッター® ランディングページ

## 概要

このランディングページは、**LPGenAgent（つくるんLP）**によって自動生成されました。

**参考サイト**: https://happytry-lp.site?vos=meta
**生成日時**: 2025-10-22

## ファイル構成

```
generated-lp/
├── index.html              # メインHTMLファイル（約50KB）
├── design-analysis.json    # デザイン分析結果（3KB）
└── README.md              # このファイル
```

## セクション構成

1. **ヘッダー（ナビゲーション）** - ロゴ + メニュー + CTA
2. **ヒーローセクション** - メインキャッチコピー + 2つのCTA
3. **実績セクション** - 3名の成功事例（テストモニアル）
4. **課題提示セクション** - 3つの顧客課題
5. **選ばれる理由セクション** - 3つの価値提案
6. **プログラム内容セクション** - 5つのコンテンツ紹介
7. **Win-Winセクション** - 関わる人全員が得する理由
8. **FAQセクション** - 5つのよくある質問（アコーディオン）
9. **CTAフォームセクション** - メールアドレス登録フォーム
10. **プロフィールセクション** - 藤原由基氏のプロフィール
11. **最終CTAセクション** - 最後の行動喚起
12. **フッター** - リンク + 会社情報

## デザイン情報

### カラーパレット

- **プライマリカラー**: `#10b981` (緑系 - 成長・安心)
- **プライマリライト**: `#d1fae5` (淡い緑)
- **アクセントカラー**: `#34d399` (明るい緑)
- **背景色**: `#ffffff` (白)
- **テキストカラー**: `#1f2937` (濃いグレー)
- **グレー**: `#6b7280` (中間グレー)

### フォント

- **フォントファミリー**: Noto Sans JP (Google Fonts)
- **見出し**: 太字（700-800）
- **本文**: 通常（400-500）

### レスポンシブ対応

- **Mobile**: 320px〜
- **Tablet**: 768px〜
- **Desktop**: 1024px〜
- **Desktop Large**: 1280px〜
- **Desktop XL**: 1536px〜

## カスタマイズ方法

### 1. カラー変更

`index.html`内の以下のクラスを検索・置換してください：

#### 緑系 → 青系に変更する場合

```bash
# 検索・置換（VS Code、Sublime Text等）
green-600 → blue-600
green-700 → blue-700
green-500 → blue-500
green-50  → blue-50
green-100 → blue-100
```

#### カラーパレット参考

```css
/* 青系（信頼・安定） */
primary: #2563eb
hover: #1d4ed8
light: #dbeafe

/* 紫系（革新・創造） */
primary: #8b5cf6
hover: #7c3aed
light: #ede9fe

/* オレンジ系（活力・情熱） */
primary: #f97316
hover: #ea580c
light: #ffedd5
```

### 2. コンテンツ変更

#### キャッチコピー

`index.html`の以下の部分を編集：

```html
<!-- 行42-50あたり -->
<h1 class="text-4xl md:text-5xl font-bold text-gray-900 mb-6 leading-tight">
  なぜ、地方在住の無名副業<br class="hidden md:block">セールスライターが<br>
  <span class="text-green-600">年間300万円＋売上5%の成果報酬</span><br class="hidden md:block">
  の契約でも<br>
  平日は1日2時間稼働、<br class="hidden md:block">休日は家族と過ごす余裕があるのか？
</h1>
```

#### 実績（テストモニアル）

`index.html`の行70-150あたりの3つの実績ブロックを編集：

```html
<div class="bg-gradient-to-br from-green-50 to-white p-8 rounded-lg shadow-lg border-2 border-green-100">
  <div class="mb-6">
    <div class="inline-block bg-green-600 text-white px-4 py-2 rounded-full text-sm font-semibold mb-4">
      [名前] ([年齢])
    </div>
    <p class="text-gray-600 text-sm">[職業]</p>
  </div>
  <p class="text-gray-700 leading-relaxed mb-4">
    [実績内容]
  </p>
</div>
```

#### FAQ項目

`index.html`の行450-550あたりのFAQセクションを編集：

```html
<div class="border border-gray-200 rounded-lg">
  <button @click="open = open === 1 ? null : 1" class="...">
    <span class="font-semibold text-lg text-gray-900">[質問内容]</span>
  </button>
  <div x-show="open === 1" x-transition class="px-6 pb-4">
    <p class="text-gray-600">[回答内容]</p>
  </div>
</div>
```

### 3. 画像差し替え

#### プレースホルダー画像を実際の画像に置換

```html
<!-- Before -->
<img src="https://placehold.co/600x400/10b981/white?text=Hero+Image" alt="ヒーロー画像">

<!-- After -->
<img src="./images/hero.jpg" alt="シャドーマーケッター®イメージ画像">
```

#### レスポンシブ画像（推奨）

```html
<img
  src="./images/hero.jpg"
  alt="シャドーマーケッター®イメージ画像"
  srcset="
    ./images/hero-320w.jpg 320w,
    ./images/hero-640w.jpg 640w,
    ./images/hero-1024w.jpg 1024w
  "
  sizes="
    (max-width: 640px) 320px,
    (max-width: 1024px) 640px,
    1024px
  ">
```

### 4. フォーム送信機能の実装

#### Option 1: Netlify Forms（推奨 - 最も簡単）

```html
<form name="contact" method="POST" data-netlify="true" class="space-y-6">
  <input type="hidden" name="form-name" value="contact">

  <div>
    <label for="email" class="block text-sm font-medium text-gray-700 mb-2">
      メールアドレス（GメールかYahooメール推奨）
    </label>
    <input
      type="email"
      id="email"
      name="email"
      required
      placeholder="your-email@example.com"
      class="w-full px-4 py-3 border-2 border-gray-300 rounded-lg focus:ring-2 focus:ring-green-600 focus:border-transparent text-lg">
  </div>

  <button
    type="submit"
    class="w-full bg-green-600 text-white py-4 rounded-lg text-xl font-semibold hover:bg-green-700 transition shadow-lg">
    今すぐ無料オンラインプログラムに参加する
  </button>
</form>
```

**デプロイ後、Netlifyの管理画面で送信内容を確認できます。**

#### Option 2: Google Formsで代用

1. Google Formsでフォーム作成
2. 埋め込みコードを取得
3. `<form>`タグを置き換え

#### Option 3: メールサービス連携（Mailchimp, ConvertKit等）

各サービスの埋め込みコードを使用してください。

### 5. Google Analytics統合

`</head>`の直前に以下を追加：

```html
<!-- Google Analytics 4 -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'G-XXXXXXXXXX');
</script>
```

**`G-XXXXXXXXXX`を実際のトラッキングIDに置き換えてください。**

## デプロイ方法

### 1. GitHub Pages（無料）

```bash
# 生成されたディレクトリに移動
cd generated-lp

# Gitリポジトリ初期化
git init
git add .
git commit -m "Initial commit: Shadow Marketer LP"

# GitHubリポジトリに接続
git remote add origin https://github.com/[ユーザー名]/[リポジトリ名].git
git push -u origin main

# GitHub設定
# Settings → Pages → Source: main branch
# 数分後、https://[ユーザー名].github.io/[リポジトリ名]/ で公開
```

### 2. Vercel（無料 - 推奨）

```bash
# Vercel CLIインストール
npm i -g vercel

# 生成されたディレクトリに移動
cd generated-lp

# デプロイ
vercel

# プロダクションデプロイ
vercel --prod
```

**カスタムドメイン設定も簡単にできます！**

### 3. Netlify（無料 - フォーム機能統合が便利）

#### 方法A: Drag & Drop

1. https://app.netlify.com/ にアクセス
2. `generated-lp`フォルダをドラッグ&ドロップ
3. 即座にデプロイ完了！

#### 方法B: Netlify CLI

```bash
# Netlify CLIインストール
npm i -g netlify-cli

# 生成されたディレクトリに移動
cd generated-lp

# デプロイ
netlify deploy

# プロダクションデプロイ
netlify deploy --prod
```

### 4. Firebase Hosting（無料）

```bash
# Firebase CLIインストール
npm i -g firebase-tools

# Firebaseログイン
firebase login

# プロジェクト初期化
firebase init hosting

# デプロイ
firebase deploy
```

## パフォーマンス最適化

### プロダクション環境での推奨事項

1. **TailwindCSSのPurge設定**

   CDN版からビルド版に移行して、未使用CSSを削除：

   ```bash
   npm install -D tailwindcss
   npx tailwindcss init
   ```

   `tailwind.config.js`:
   ```js
   module.exports = {
     content: ["./index.html"],
     theme: {
       extend: {},
     },
     plugins: [],
   }
   ```

   ビルド:
   ```bash
   npx tailwindcss -i ./src/input.css -o ./dist/output.css --minify
   ```

2. **画像最適化**

   - WebP形式に変換
   - 複数サイズ生成（srcset使用）
   - 遅延読み込み（loading="lazy"）

   ```html
   <img
     src="./images/hero.webp"
     alt="ヒーロー画像"
     loading="lazy"
     srcset="
       ./images/hero-320w.webp 320w,
       ./images/hero-640w.webp 640w,
       ./images/hero-1024w.webp 1024w
     "
     sizes="(max-width: 640px) 320px, (max-width: 1024px) 640px, 1024px">
   ```

3. **CDNキャッシュ設定**

   Vercel、Netlifyは自動で最適化されます。

## トラブルシューティング

### Q1: FAQのアコーディオンが動かない

**A**: Alpine.jsが正しく読み込まれているか確認してください。

```html
<!-- <head>内に以下があるか確認 -->
<script defer src="https://cdn.jsdelivr.net/npm/alpinejs@3.x.x/dist/cdn.min.js"></script>
```

### Q2: フォント（Noto Sans JP）が表示されない

**A**: Google Fontsが正しく読み込まれているか確認してください。

```html
<!-- <head>内に以下があるか確認 -->
<link href="https://fonts.googleapis.com/css2?family=Noto+Sans+JP:wght@400;500;600;700;800&display=swap" rel="stylesheet">
```

### Q3: モバイルで表示が崩れる

**A**: `<meta name="viewport">`タグがあるか確認してください。

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

### Q4: フォーム送信ができない

**A**: 現在のHTMLはフロントエンドのみです。以下のいずれかを実装してください：

- Netlify Forms（推奨）
- Google Forms埋め込み
- Mailchimp等のメールサービス
- カスタムバックエンド（PHP, Node.js等）

### Q5: ページが重い

**A**: 以下を確認してください：

- 画像サイズが大きすぎないか（推奨: 1MB以下）
- TailwindCSSをビルド版に変更（CDN版は5MB以上）
- 不要なJavaScriptを削除

## ブラウザ対応

### 対応ブラウザ

- ✅ Chrome 90+
- ✅ Firefox 88+
- ✅ Safari 14+
- ✅ Edge 90+

### 非対応ブラウザ

- ❌ Internet Explorer（全バージョン）
- ❌ 古いAndroidブラウザ（Android 5.0以前）

## セキュリティ

### 推奨事項

1. **HTTPS必須**: GitHub Pages、Vercel、Netlifyは自動でHTTPS対応
2. **フォーム送信**: reCAPTCHAやhCaptchaでスパム対策
3. **CSP設定**: Content Security Policyヘッダー設定（Netlify、Vercel管理画面で設定可能）

### Netlify CSP設定例

`netlify.toml`ファイルを作成：

```toml
[[headers]]
  for = "/*"
  [headers.values]
    Content-Security-Policy = "default-src 'self'; script-src 'self' 'unsafe-inline' https://cdn.tailwindcss.com https://cdn.jsdelivr.net; style-src 'self' 'unsafe-inline' https://fonts.googleapis.com; font-src 'self' https://fonts.gstatic.com;"
```

## ライセンス

このランディングページのコードは自由に商用利用できます。

**注意事項**:
- 「シャドーマーケッター®」は登録商標です。商標使用には権利者の許可が必要です。
- 実績（テストモニアル）の内容は架空のものであり、実際の成果を保証するものではありません。

## サポート

質問・問題がある場合は、以下までご連絡ください：

- **LPGenAgent仕様書**: `.claude/agents/specs/business/lp-gen-agent.md`
- **実行プロンプト**: `.claude/agents/prompts/business/lp-gen-agent-prompt.md`
- **使用例集**: `.claude/agents/examples/lp-gen-examples.md`

---

## 生成情報

- **生成Agent**: LPGenAgent v1.0.0（つくるんLP）
- **生成日時**: 2025-10-22
- **参考URL**: https://happytry-lp.site?vos=meta
- **技術スタック**: HTML5 + TailwindCSS v3.4 (CDN) + Alpine.js v3 (CDN)
- **デザインテーマ**: 緑系アクセント（成長・安心）
- **セクション数**: 11セクション
- **CTA数**: 6箇所

---

**🎉 ランディングページ生成完了！**

まずは`index.html`をブラウザで開いてプレビューしてください：

```bash
open index.html
```

カスタマイズが必要な場合は、このREADMEを参照してください。

デプロイの準備ができたら、上記の「デプロイ方法」セクションを参照してください。

**Good Luck! 🚀**
