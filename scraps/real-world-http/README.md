# Real World HTTP のスクラップ

原稿は `001.md`、`002.md`、`003.md` のように分け、1ファイルを1コメントとして投稿します。この README は投稿しません。

## 準備

以下のコマンドは `zenn-article` ディレクトリで実行します。

```bash
cd /Users/fs203/workspace/BLOG/zenn-article
```

ZennのAPIキー設定（https://zenn.dev/settings/api-keys）でスクラップの読み取り・書き込み権限を付けたキーを発行し、ターミナルの環境変数 `ZENN_API_KEY` に設定してください。キーはこのリポジトリに保存しません。

## 最初に1回だけ作成する

以下のコマンドを実行すると、公開スクラップを作成します。限定公開にする場合は `--unlisted` を追加します。

```bash
npx zenn scrap create --title "Real World HTTP" --file ./scraps/real-world-http/001.md
```

成功時に表示されたスクラップのURLを控えます。以降の追記には `create` ではなく `post` を使います。

## 続きを追記する

次の原稿を `scraps/real-world-http/002.md` に書き、下記のURLを実際のスクラップのURLに置き換えて実行します。

```bash
npx zenn scrap post '作成したスクラップのURL' --file ./scraps/real-world-http/002.md
```

3回目以降は `003.md`、`004.md` とファイルを増やし、同じURLに投稿します。ファイルを編集・GitにpushするだけではZennには反映されません。投稿済みのファイルを再度 `post` すると、別のコメントとして追加されます。

## スクラップのURLを確認する

```bash
npx zenn scrap list
```
