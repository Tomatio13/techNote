<h1 align="center">技術ノート</h1>

<p align="center">
  スマホや PC で投げた技術的な疑問を、静的 HTML 記事として蓄積し、GitHub Pages で公開するためのリポジトリです。
</p>

<p align="center">
  <a href="https://tomatio13.github.io/techNote/"><img src="https://img.shields.io/badge/GitHub_Pages-Live-blue" alt="GitHub Pages"></a>
  <a href="https://github.com/Tomatio13/techNote"><img src="https://img.shields.io/badge/GitHub-Repository-black" alt="GitHub Repository"></a>
  <img src="https://img.shields.io/badge/HTML-static-orange" alt="HTML">
  <img src="https://img.shields.io/badge/CSS-custom-blueviolet" alt="CSS">
  <img src="https://img.shields.io/badge/deploy-GitHub_Actions-222222" alt="GitHub Actions">
</p>

## 🌐 公開URL

- GitHub Pages: https://tomatio13.github.io/techNote/
- GitHub Repository: https://github.com/Tomatio13/techNote

## 📌 これは何か

- 1テーマ1ページの HTML 記事を `articles/` に蓄積します
- `index.html` で新着とカテゴリ別の両方から辿れるように整理します
- 記事はビルド不要の静的ファイルとして管理します
- GitHub Actions から GitHub Pages へ公開します

## 📚 現在の収録記事

- `FFFとは何か`
- `CodeGraphとは何か`
- `graphifyとは何か`

## 🗂️ サイト構成

- `index.html`
  - トップページ
  - 新着一覧
  - カテゴリ別一覧
- `articles/`
  - 個別記事の HTML
- `styles/site.css`
  - 共通スタイル
  - 記事内の図カードやレイアウト
- `AGENTS.md`
  - 記事生成ルール
  - 図の入れ方
  - 安全性と更新ルール
- `.github/workflows/static.yml`
  - GitHub Pages 用のデプロイ workflow

## ✍️ 記事の追加方法

1. `質問:` で始まる依頼を Codex に渡す
2. `articles/<slug>.html` を追加する
3. `index.html` の新着セクションを更新する
4. `index.html` の対応カテゴリも更新する
5. 差分を確認する

## 🧭 記事ルール

- 各記事は少なくとも次を含めます
  - タイトル
  - 要点
  - 本文
  - 比較や流れを示す図
  - 参考URL
  - 作成日
- 記事ごとに最低1つは図を入れます
- 図は装飾ではなく、流れ、比較、構造の理解を早める目的で使います
- 仕様、価格、法令、リリース状況など変化しやすい情報は一次情報を優先します
- 秘匿情報、認証情報、個人情報は記事に含めません

詳細な運用ルールは [AGENTS.md](./AGENTS.md) にあります。

## 🔍 ローカルで確認する方法

- もっとも簡単なのは `index.html` をブラウザで開く方法です
- 画像や相対パスを含む確認を安定させたいなら、任意の静的 HTTP サーバーで配信してください

例:

```bash
python3 -m http.server 8000
```

その後、`http://localhost:8000/` を開きます。

## 🚀 GitHub Pages への公開方法

- このリポジトリは `main` への push を契機に GitHub Actions が動きます
- workflow は `.github/workflows/static.yml` にあります
- GitHub Pages は `GitHub Actions` 配信で有効化済みです
- 公開後は https://tomatio13.github.io/techNote/ で閲覧できます

## 🔄 公開フロー

1. 記事を追加または修正する
2. `index.html` の導線も合わせて直す
3. commit する
4. `main` に push する
5. Actions の `Deploy Static Site` 成功を確認する
6. 公開 URL で表示を確認する

## 🎯 このリポジトリが向いている用途

- 調べた内容をその場で記事として残したい
- Markdown ではなく HTML で図を含めた説明を書きたい
- ビルドなしで公開できる軽い知識サイトを作りたい
- AI ツールや設計メモを、自分向けに整理して公開したい

## 🙏 謝辞

- このリポジトリの発想元は、ttaniguchi さんの Zenn 記事
  `移動中でも就寝前でも、Codexと育てる「技術ノート」`
  です。
- 参考記事:
  https://zenn.dev/ttaniguchi/articles/instant-question-html-notes

## 🛠️ 今後の拡張候補

- Web カテゴリの記事追加
- インフラカテゴリの記事追加
- トップページへの導入図追加
- 記事テンプレートの共通化
- カード一覧の自動生成
