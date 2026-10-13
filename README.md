# kids-quest-support

こどもクエストのサポートページ、利用規約、プライバシーポリシー。GitHub Pages で公開する静的サイト。

| ページ | URL |
|---|---|
| サポート | https://support.kids-quest-api.com/ |
| アカウント削除の案内 | https://support.kids-quest-api.com/#delete-account |
| 利用規約 | https://support.kids-quest-api.com/terms/ |
| プライバシーポリシー | https://support.kids-quest-api.com/privacy/ |

## 構成

- `index.html`: サポートページ
- `terms/index.html`: 利用規約
- `privacy/index.html`: プライバシーポリシー
- `style.css`: 共通スタイル
- `CNAME`: GitHub Pages のカスタムドメイン設定

ビルドは不要。`main` に push すると公開内容に反映される。

## アプリ内表示

利用規約とプライバシーポリシーは、モバイルアプリの WebView からも表示する。URL に `?embed=1` を付けると、ナビゲーション・タイトル・フッターを隠して本文だけを表示する。本文はこのリポジトリだけで管理し、アプリ側には持たない。

## ローカルで確認する

CSS をルート相対パス(`/style.css`)で読み込んでいるため、ファイルを直接開かずローカルサーバー経由で確認する。

```sh
python3 -m http.server 8000
```

## DNS

`kids-quest-api.com` の hosted zone(Route53)に、`support` の CNAME レコード(値: `rits-tech.github.io`)を登録する。
