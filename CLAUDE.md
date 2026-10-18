# Alter World Models合同会社 コーポレートサイト

静的HTML（ビルドツールなし）のコーポレートサイト。GitHub Pages で `alterworldmodels.com` として公開（`main` ブランチ直下がそのまま公開される）。
会話・コメント・コミットメッセージ・回答は**日本語**で行う。余計な前置きや装飾は不要、結果を簡潔に報告する。

## 事業の概要（文言を書くときの前提）
「システム思考」をベースとした共通認識・評価プラットフォーム（Vensim®ベースのシミュレーション）の提供、プロフェッショナルサービス、トレーニング/セミナー。代表: 堤 廉（代表社員）。

## 構成
```
index.html / service.html / company.html / contact.html
policies/privacy.html, policies/security.html   # ルートのページへは ../ で参照
assets/logo-mark.png, assets/vensim-diagram.png
CNAME   # 触らない
```
- 各HTMLは単体完結。`<style>` と `<script>` はページごとに直書きで、共通CSS/JSはない。
- **ヘッダー・フッター・ロゴ・共通CSS変数を変更するときは、全6ページを必ず同じ内容に揃える。**
- 外部依存は Google Fonts（Zen Kaku Gothic New / Noto Sans JP / Inter）のみ。
- お問い合わせフォームは Formspree（`https://formspree.io/f/xoeqnykb`）へPOST。IDを変えない。

## デザイン（変更しない）
- ヘッダー=空、本文=海面のグラデーション、フッター=深海。氷山モチーフ。シンプルに保つ。
- CSS変数: `--sky-100:#F6FBFD; --sky-200:#E4F2FA; --header-top:#8AC9ED; --header-bottom:#E4F2FA; --surface-top:#CDE9F8; --surface-mid:#7FC3E8; --surface-deep:#2C86BE; --deep-900:#081F38; --deep-800:#0B2E52; --navy:#0B2E52; --blue:#1C6FA8; --blue-light:#3B93C9; --ice-200:#CFE8F7; --text:#16324A`
- ヘッダーのロゴは、氷山ひし形SVG＋「Alter World Models合同会社」。クリックで `index.html` へ。
- 共通構造: sticky ヘッダー（ナビ、JA/EN切替）→ サブページはパンくず → `<main class="ocean">` → 3列フッター → 最下部にポリシーリンク。ブログのリンクは note（外部リンク矢印SVG付き、`target="_blank" rel="noopener"`）。

## 表記ルール
- 「Vensim」は必ず **Vensim®**（®付き）。
- 営業・紹介文では「コンサルティング」ではなく**「プロフェッショナルサービス」**。ただし会社概要の事業内容（法的表記）と経歴中の「アビームコンサルティング株式会社」はそのまま。
- 会社名は「Alter World Models合同会社」（空白を入れない）。
- 設立日は「2026年08月25日」、プライバシーポリシー制定日は「2026年09月01日」。日付の書式は `YYYY年MM月DD日`。
- サービス名は Platform / Professional Service / Training/Seminar（英語ラベル）。
- メール: info@ / privacy@ / security@ alterworldmodels.com（Microsoft 365）。
- noteアカウント: https://note.com/alterworldmodels 。「システム思考」の解説記事: https://note.com/alterworldmodels/n/n3f8c7e9b59a6

## 更新時の作業手順
1. 依頼内容を確認し、あいまいな点（どの箇所か、文言の確定版か）があれば編集前に質問する。
2. 対象ファイルを編集する。依頼されていない箇所は変更しない。
3. 確認チェック（下記）を行う。
4. 変更内容（ファイル・箇所・前後の文言）を簡潔に報告し、**コミット/pushの前にユーザーの承認を得る**。
5. 承認後、`main` にコミットして push する（GitHub Pages に自動反映。反映まで1〜2分）。

## 確認チェック
- 全HTMLで `<style>` / `</style>` / `</footer>` の数が崩れていない。
- 内部リンク・アンカー・画像パスが実在する（`policies/` 内は `../` 付き）。
- ナビの current 表示が正しい（サービス/会社概要/お問い合わせ。プライバシー等のポリシーページはcurrentなし）。
- 全ページでヘッダー/フッターが一致している。
- 表記ルール違反（®漏れ、「コンサルティング」の混入など）がない。

## Git運用
- 通常は `main` へ直接コミットでよいが、大きな変更はブランチ＋PRにする。
- コミットメッセージは日本語で、1行目に要点（例: 「会社概要: 代表者の想いを更新」）。
- 認証情報やトークンをファイルに書かない。`gh` の認証を使う。
