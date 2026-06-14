# techNote

スマホや PC で投げた技術的な疑問を、静的 HTML 記事として蓄積するための最小構成です。

## 構成

- `index.html`: 新着とカテゴリ一覧を持つトップページ
- `articles/`: 個別記事
- `styles/site.css`: 共通スタイル
- `AGENTS.md`: Codex 向けの記事生成ルール

## 公開方法

GitHub Pages などの静的ホスティングにそのまま配置できます。

## 運用イメージ

1. `質問:` で始まる依頼を Codex に渡す
2. `articles/` に HTML を追加する
3. `index.html` にカードを追記する
4. 差分確認後に公開する
