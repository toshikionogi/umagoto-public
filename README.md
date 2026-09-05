# umagoto-public

ウマゴト（推し馬アプリ）のサービスサイト。GitHub Pages で `umagoto.jp` に公開する。

- 素の HTML / CSS のみで構築（ビルドツール・SSGなし）
- 公開ソースは `main` ブランチの `/`（ルート）
- 内部ドキュメント（要件整理・法務原稿ドラフトなど）はこのリポジトリに含めない

## ローカルでの確認

```sh
python3 -m http.server 8000
```

`http://localhost:8000/` で確認できる。

## 独自ドメイン設定メモ

- `CNAME` ファイルに `umagoto.jp` を設定済み
- GitHub リポジトリの Settings → Pages で、公開元をこのリポジトリの `main` ブランチ `/`（ルート）に設定する
- `umagoto.jp` の DNS（Xserverドメイン）に GitHub Pages 向けの A レコード / CNAME レコードを設定する
- 予備ドメイン `umagoto.com` → `umagoto.jp` のリダイレクトは、Cloudflare（無料）のネームサーバー切り替え＋ Redirect Rules（301）で行う。レンタルサーバー側では設定しない
