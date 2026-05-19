# IDEAS Asia Pacific Japan Hub — Design System

このドキュメントは Cursor および将来の貢献者向けの、デザイン判断の根拠と運用ルールです。
新しいページやコンポーネントを作る際は、このドキュメントを参照してください。

---

## デザインの哲学

**「思索的な気品 × 変革のエネルギー」**

IDEAS Asia Pacific の本質は、効率追求型のリーダーシップではなく、
Theory U に根ざした「内省・対話・共創」のリーダーシップです。
本サイトのビジュアル言語も、そのトーンを反映する必要があります。

- 余白を惜しまない(思索の時間を視覚的に表現)
- 明朝書体を要所に使う(品格と内省性)
- 紫を主役にする(IDEAS ブランド、変革と精神性)
- 赤と緑はアクセントとして(行動への呼びかけ、ロゴ由来)
- 装飾より構造で語る(編集的・マガジン的なレイアウト)

避けるべき方向性:
- SaaS スタートアップ的なフラットさ
- 企業 IR ページのような硬さ
- 過度な装飾やアニメーション
- 万人受けする「無難な」デザイン

---

## カラートークン

```css
/* Brand Purple (IDEAS ブローシャ由来) */
--c-purple-900: #1F1733;   /* 最深部、主要テキスト */
--c-purple-800: #2D2548;   /* フッター、暗背景 */
--c-purple-700: #3D2E5F;   /* 暗アクセント */
--c-purple-600: #5A4080;   /* ミッドトーン */
--c-purple-500: #7A5BA8;   /* コアブランド */
--c-purple-400: #9B7BC8;   /* ライトアクセント */
--c-purple-300: #BFA8DC;   /* より明るいアクセント */
--c-purple-100: #EDE5F5;   /* ごく薄い色味 */
--c-purple-50:  #F8F4FC;   /* セクション背景 */

/* Accent (IDEAS ロゴ由来) */
--c-red:        #D0272D;   /* CTA、強調 */
--c-red-hover:  #B01F25;
--c-green:      #3A9A4A;   /* 装飾的アクセントのみ */

/* Neutrals */
--c-white:      #FFFFFF;
--c-cream:      #FBF8F3;   /* メイン背景(暖かみのあるオフホワイト) */
--c-text:       #2D2548;
--c-text-muted: #6B6280;
--c-border:     #E5DEEF;
```

### 配色ルール

| 用途 | カラー |
|---|---|
| ベース背景 | `--c-cream` |
| セクション背景(交互) | `--c-cream` / `--c-purple-50` / `--c-white` |
| 暗いセクション(対比用) | `--c-purple-800` グラデーション |
| 主要テキスト | `--c-purple-900` または `--c-text` |
| 補助テキスト | `--c-text-muted` |
| 見出しアクセント | `--c-purple-500` |
| プライマリ CTA | `--c-red` 背景 + 白文字 |
| セカンダリ CTA | 透明背景 + `--c-purple-900` ボーダー |
| 細い装飾線 | `--c-red`(28px〜32px の短い水平線) |

---

## タイポグラフィ

3 つのフォントを組み合わせます。

```css
--font-display: "Zen Old Mincho", "Hiragino Mincho ProN", "Yu Mincho", serif;
--font-body:    "Noto Sans JP", system-ui, -apple-system, sans-serif;
--font-latin:   "Cormorant Garamond", "Zen Old Mincho", serif;
```

### 使い分け

| フォント | 用途 |
|---|---|
| **Zen Old Mincho** | 見出し、引用、フェロー名、チーム名、装飾的な日本語テキスト |
| **Noto Sans JP** | 本文、UI ラベル、ナビゲーション、CTA ボタン |
| **Cormorant Garamond** | 英語の eyebrow ラベル(`Why Now / なぜ今、日本に`)、装飾的な番号(`01 / Theory U`) |

### サイズスケール

```
hero 見出し:    clamp(40px, 6vw, 76px)  / Zen Old Mincho / 500
section 見出し: clamp(28px, 3.5vw, 44px) / Zen Old Mincho / 500
カード見出し:    20px / Zen Old Mincho / 500
本文:           16px / Noto Sans JP / 400 / line-height 1.85〜2
小テキスト:      13–14px / Noto Sans JP / 400
eyebrow:        13px / Cormorant Garamond / letter-spacing 0.24em / uppercase
```

### 日本語タイポの注意

- 日本語見出しは `letter-spacing: 0.02em` で微妙に間隔を空ける
- 行間は広め(line-height 1.7〜2.0)で思索的な雰囲気を出す
- 強調は太字や色ではなく、改行と余白で行う

---

## レイアウト

```css
--container:    1200px;   /* 通常コンテナ */
--container-sm: 920px;    /* 文章主体の節 */
--container-xs: 720px;    /* テキストブロック */
--header-h:     76px;
```

### スペーシング

`--space-1` (4px) 〜 `--space-32` (128px) の 4 の倍数スケール。
セクション間のパディングは `--space-24` (96px) を基本とし、
モバイルでは `--space-16` (64px) に縮小。

### グリッド

- フェロー一覧: 5 カラム(タブレットで 3、モバイルで 1)
- L.I.F.E. カード: 4 カラム(タブレットで 2、モバイルで 1)
- ジャーニー: 6 カラム(タブレットで 3、モバイルで 1)
- 2 カラム構成(Intro、Contact 等)はタブレット以下で 1 カラム

---

## コンポーネントパターン

### Eyebrow(セクション小見出し)

```html
<span class="eyebrow">About / IDEASとは</span>
```

赤い短い水平線 + Cormorant Garamond + 日本語の混在。
すべての主要セクションの冒頭に必ず置く。

### Section Heading

```html
<h2 class="heading">
  本文 1 行目、<br />
  <em>強調したいフレーズ</em>
</h2>
```

`<em>` は紫 500 の色変更として使用(イタリックではない)。

### Primary CTA

```html
<a class="btn btn-primary">
  IDEASを知る
  <i data-lucide="arrow-right" class="lucide-icon"></i>
</a>
```

赤背景・白文字。ページに 1〜2 個まで。

### Ghost CTA(セカンダリ)

```html
<a class="btn btn-ghost">
  すべて見る
  <i data-lucide="arrow-right" class="lucide-icon"></i>
</a>
```

透明背景・紫ボーダー。情報導線用。

---

## モーション

控えめに、要所のみ。

- ヒーロー要素の fade-up(0.1s 刻みでステージング)
- カードホバー時の `translateY(-4px)` + ソフトシャドウ
- ステータスバッジの脈動(`pulse-dot`)
- スティッキーヘッダーのスクロール時切り替え

避けるもの: 派手なパララックス、回転、複雑な scroll-driven animation。
Theory U の「内省」のトーンに合わない。

---

## アイコン

[Lucide](https://lucide.dev) を使用(`stroke-width: 1.75`)。
細い線画スタイルで、明朝書体の繊細さと調和する。

主要アイコン:
- `arrow-right` / `arrow-down`: CTA
- `user` / `building-2` / `heart` / `mail`: コンタクト分岐
- `menu` / `x`: モバイルメニュー
- `chevron-right`: フッターリンク

---

## アクセシビリティ

- すべてのインタラクティブ要素にフォーカスインジケーター
- `lang="ja"` を `<html>` に設定済み
- カラーコントラスト WCAG AA 準拠
- セマンティック HTML5(`<section>`, `<article>`, `<nav>` 等)
- 画像には `alt` 属性
- アイコンのみのボタンには `aria-label`

---

## 写真・画像のトーン

- **MIT キャンパスの集合写真**: 多様性が伝わる、自然光の写真を優先
- **フェロー写真**: 丸クロップでなく正方形。プロフェッショナルな印象
- **チーム写真**: 丸クロップ、140px
- **装飾画像**: 使うなら、ブローシャの竹/織物テクスチャを抽象化したもの

避けるべき写真:
- ストックフォト感が強いビジネス握手
- 過度に演出された人物写真
- 装飾的すぎる抽象 CG

---

## ファイル構成(推奨)

```
/
├── index.html
├── about/
│   └── index.html
├── fellows/
│   ├── index.html
│   └── [name]/index.html
├── team/index.html
├── theory-u/index.html
├── fund/index.html
├── contact/
│   ├── index.html
│   └── thanks.html
├── images/
│   ├── logo-ideas.svg
│   ├── logo-mit.svg
│   ├── logo-uid.svg
│   ├── og-image.jpg
│   ├── fellows/
│   └── team/
├── styles/
│   └── main.css      (将来 index.html から抽出する)
├── _redirects        (Netlify)
└── netlify.toml      (Netlify config)
```

---

## ブランドの公式情報

- 公式名: **IDEAS Asia Pacific**
- 略称展開: Innovative Dynamic Education and Action for Sustainability
- 公式 URL: https://mitsloan.mit.edu/global-programs/ideas-asia-pacific
- 提供主体: MIT Sloan Global Programs × United in Diversity Foundation
- 日本ハブ運営: 野田浩平博士、井岡氏

ロゴと公式ブランド要素は UID から提供されたものを使用すること。
独自に色や形状を変更しないこと。
