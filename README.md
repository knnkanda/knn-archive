# KNN Digital Archive — 試験版

4knn.tvの本番環境を変更せず、GitHub + Cloudflare Pagesで公開する静的サイトの試作です。

## 主な内容
- `index.html` : 記事一覧・キーワード／タグ検索
- `articles/001-cloudflare-github-legacy.html` : 第1記事の公開版
- `articles/001-cloudflare-github-legacy.md` : 第1記事の編集・長期保存用Markdown原稿（draft）
- `assets/` : 共通CSS・検索用JavaScript

## Cloudflare Pagesの公開手順
1. GitHubで `knn-archive` という**新規リポジトリ**を作り、ZIPを展開したファイルをルートへアップロードする。
2. Cloudflareダッシュボードの Workers & Pages → Create → Pages → Connect to Git から上記リポジトリを選択する。
3. Framework preset は None、Build command は空欄、Build output directory は `/` を指定する（ダッシュボードの仕様が変わった場合はルートディレクトリを静的成果物として扱う設定）。
4. デプロイ後の `*.pages.dev` URLで記事と検索を検証する。
5. AdSenseは未導入。広告枠のみ配置している。

## 注意
- `.md`原稿と公開HTMLは現時点では手動同期です。次段階でAstro等によるMarkdown自動ビルドへ移行する想定です。
- 実際のWordPress記事・コメント・取材資料・権利未確認の画像はまだ移していません。
- 試験URLとGitHubリポジトリは未作成です。
- 記事原稿は対話の編集要約であり逐語録ではありません。
- GitHubが永続保存を保証するわけではないため、定期的なオフラインバックアップも用意してください。
