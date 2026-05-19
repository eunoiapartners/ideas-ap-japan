# IDEAS Asia Pacific Japan Hub — プロジェクトガイド

このドキュメントは、サイト全体の構成、コンテンツプラン、次のステップを Cursor および
運営チームに伝えるためのものです。

---

## プロジェクトの目的

このサイトは **3.0 への参加誘導ページではありません**。次の 3 つの目的を持ちます。

1. **認知拡大** — IDEAS Asia Pacific と背後の思想(Theory U、システム思考)を日本に広める
2. **若手支援ファンドの基盤** — 将来の支援者・関心層との接点づくり
3. **法人・団体問い合わせの窓口** — 人材開発・教育機関などからの相談受付

運営体制は 2 名(野田浩平氏、井岡氏)。本業を持つため、更新頻度を高くは保てない前提で
「育てる」サイトではなく「完結した名刺・ハブサイト」として設計しています。

---

## サイトマップ

### Phase 1(最初に公開)

```
/                    トップページ (index.html)
/about/              IDEAS とは詳細(ブローシャ Web 版)
/fellows/            日本人フェロー一覧
/fellows/[name]/     個別フェロー(5 ページ)
/team/               運営チーム紹介
/theory-u/           Theory U / システム思考 入門
/contact/            お問い合わせフォーム
/contact/thanks/     送信完了ページ
```

### Phase 2(コンテンツが溜まってから)

```
/news/               活動報告・イベント告知
/fund/               若手支援ファンド詳細(法人化後)
/en/                 英語版(最低限)
```

---

## トップページの構成(現状)

1. **Header** — スティッキー、トランスペアレント → スクロールで白背景
2. **Hero** — 紫グラデーション + 明朝大見出し + 2 つの CTA
3. **Why Now** — JFK 引用 + 日本社会への翻訳
4. **About IDEAS** — L.I.F.E. 4 本柱 + 6 モジュールの旅 + MIT/UID 公式表示
5. **Fellows Preview** — 5 名のプレビューカード
6. **Team** — 野田氏・井岡氏
7. **Theory U / 関連思想** — 紫ダーク背景の 3 カード
8. **Fund(構想中)** — 若手支援への関心登録誘導
9. **Contact** — 4 種の問い合わせ分岐
10. **Footer**

---

## コンテンツ・チェックリスト

公開前に揃える必要があるコンテンツ:

### 必須コンテンツ

- [ ] **ロゴファイル** — UID から提供された IDEAS Asia Pacific ロゴを `/images/logo.png` または `.svg` に配置
- [ ] **フェロー 5 名の情報**(全員分):
  - [ ] 顔写真(正方形、最低 800×800px)
  - [ ] 氏名(漢字+ローマ字)
  - [ ] 所属・役職
  - [ ] コホート(1.0 / 2.0)
  - [ ] 100-300 字のプロフィール
  - [ ] 400-600 字の「IDEAS で学んだこと、いま取り組んでいること」
- [ ] **運営チーム 2 名**:
  - [ ] 野田浩平氏の顔写真 + プロフィール本文(URL は GLOBIS にあるものを参照可)
  - [ ] 井岡氏の顔写真 + プロフィール本文
- [ ] **連絡先メールアドレス** — `hello@ideas-ap-japan.org` 等を取得・設定
- [ ] **OGP 画像** — `/images/og-image.jpg`(1200×630px)

### 推奨コンテンツ

- [ ] MIT キャンパス集合写真(横長、ヒーロー背景用候補)
- [ ] 横浜・バリ島・ジャカルタの会場写真(About ページ用)
- [ ] 過去コホートの活動風景写真(数枚)

---

## 各サブページのコンテンツ指針

### `/about/` — IDEAS とは(詳細版)

ブローシャの内容を Web 用に再構成。

セクション:
1. はじめに(SDGs 進捗とトライセクター・リーダーシップの必要性)
2. IDEAS の歴史(2008 年からインドネシアで実施 → アジア太平洋へ拡張)
3. L.I.F.E. の 4 本柱(詳細解説)
4. 1 年間の学びの旅(6 モジュール、開催地、内容)
5. 学習コンテンツ(理論基盤モジュール、実践型ラボ)
6. MIT 教員陣 + 地域ファカルティ紹介
7. 価値提案(MIT 修了証、アフィリエイト等)
8. 費用(US$20,000、12 ヶ月)+ 奨学制度への言及

### `/fellows/` — 日本人フェロー一覧

5 名のカード一覧。コホート別にグルーピング表示。
各カードからは個別ページへ遷移。

### `/fellows/[name]/` — 個別フェロー

各フェロー 1 ページ:
- 大きな顔写真
- 氏名・所属・コホート
- プロフィール
- 「IDEAS で学んだこと」(長めの本文)
- 現在の取り組み
- 連絡先 or LinkedIn(本人の許可があれば)

### `/team/` — 運営チーム

野田氏・井岡氏の詳細プロフィール + 日本ハブとしてのミッションステートメント。
「なぜこの活動をしているのか」を一人称で書くと共感を得やすい。

### `/theory-u/` — Theory U / 関連思想入門

これは日本ハブの独自価値になる重要ページです。日本語で Theory U や
プレゼンシングを丁寧に解説したサイトは少ないため、SEO 流入と教育的価値の両方を狙えます。

セクション:
1. Theory U とは(概要、U 字プロセス、Open Mind/Heart/Will)
2. プレゼンシングの実践
3. システム思考と学習する組織(センゲ)
4. これらを学ぶための推薦書籍(邦訳あり)
5. オットー・シャーマー博士について

ただし、深掘り解説を無理に書く必要はありません。
「入口を示して、書籍と本家サイト(Presencing Institute)に誘導する」程度で十分。

### `/contact/` — お問い合わせフォーム

**Netlify Forms を使用**(コード不要、設定だけで動く)。

フォーム項目:
- お名前(必須)
- メールアドレス(必須)
- ご所属
- お問い合わせ種別(ラジオボタン)
  - 個人として参加に関心
  - 組織として導入を相談
  - 若手支援ファンドに関心
  - 取材・登壇・その他
- ご相談内容(必須、textarea)
- プライバシーポリシー同意(必須、checkbox)

HTML 例:
```html
<form name="contact" method="POST" data-netlify="true" data-netlify-honeypot="bot-field">
  <input type="hidden" name="form-name" value="contact" />
  <p hidden><label>Don't fill: <input name="bot-field" /></label></p>
  <!-- 各フィールド -->
</form>
```

---

## Netlify セットアップ

### `netlify.toml`(プロジェクトルートに配置)

```toml
[build]
  publish = "."

[[redirects]]
  from = "/contact/thanks"
  to = "/contact/thanks.html"
  status = 200

[[headers]]
  for = "/*"
  [headers.values]
    X-Frame-Options = "DENY"
    X-Content-Type-Options = "nosniff"
    Referrer-Policy = "strict-origin-when-cross-origin"
```

### ドメイン設定

1. Netlify サイト管理画面 → Domain settings
2. `ideas-ap-japan.org` を追加
3. DNS は Netlify DNS に向けるか、外部 DNS で A レコード/CNAME 設定
4. HTTPS 証明書は Let's Encrypt が自動発行される

### フォーム通知

Netlify Forms の Notifications で運営者 2 名のメールアドレスを設定。
スパム対策として reCAPTCHA を有効化(無料)。

---

## 次のステップ(Cursor で進める順序)

### Step 1: Phase 0 — 構造の確認(本日)

- [ ] `index.html` をプロジェクトに配置
- [ ] `DESIGN_SYSTEM.md` と `PROJECT_GUIDE.md` を `/docs/` フォルダに配置
- [ ] ロゴ画像を `/images/logo.png` に配置
- [ ] ブラウザで開いて全体の見え方を確認
- [ ] Netlify にデプロイして実機確認

### Step 2: コンテンツ収集(1〜2 週間)

- [ ] フェロー 5 名にプロフィール原稿を依頼(同じテンプレートで)
- [ ] 野田氏・井岡氏の写真とプロフィール文を準備
- [ ] OGP 画像のデザイン

### Step 3: サブページ実装(Cursor で 1 ページずつ)

優先順:
1. `/contact/` — 一番重要(問い合わせ窓口)
2. `/fellows/` + 個別 5 ページ — 説得力の核
3. `/team/` — 信頼の核
4. `/about/` — 詳細情報
5. `/theory-u/` — SEO とブランディング

各サブページは `index.html` のスタイルを共通 CSS に抽出してから作ると効率的。

### Step 4: 公開後

- [ ] Google Analytics or Plausible 等を設置
- [ ] サーチコンソール登録
- [ ] サイトマップ(`sitemap.xml`)生成
- [ ] LinkedIn / Facebook 等で告知

---

## Cursor で作業するときの指示テンプレート

各サブページを作るとき、Cursor にこう伝えると一貫性が保てます:

> `/docs/DESIGN_SYSTEM.md` と `/docs/PROJECT_GUIDE.md` を読み、
> 既存の `index.html` と同じデザイン言語で `/fellows/index.html` を作成してください。
> CSS は `index.html` から共通部分を抽出してください。

> `index.html` のヘッダー・フッターと整合するように、
> `/contact/index.html` に Netlify Forms 対応のお問い合わせフォームを実装してください。

---

## 注意事項

### コンテンツの正確性

- IDEAS の略称: **Innovative Dynamic Education and Action for Sustainability**(MIT 公式)
- 公式パートナー: **MIT Sloan Global Programs** × **United in Diversity Foundation**
- 「Theory U」は固有名なので大文字小文字に注意
- 4 つの柱の正式名は **L.I.F.E.**(Leadership, Innovation, Foresighting, Entrepreneurship)
- 「3 つの HAPPINESS」(人・地球・精神)は補足的に言及可

### 表現の注意

- 法人格がないため、寄付の直接的な訴求は避ける(現状の「構想中」表現を維持)
- 「公式日本ハブ」という表現は UID/MIT の承認を得ている前提で使用
- フェローのプロフィール掲載は必ず本人の許諾を得ること
- 価格(US$20,000)は変更される可能性があるので明記する際は出典を併記

### 法人格が出来たら

- 法人名と住所をフッターに追加
- 寄付ページを `/fund/` として本格実装
- 税制優遇の有無を明記
- 利用規約・プライバシーポリシーを整備
