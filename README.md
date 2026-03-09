## 顧客情報登録 LIFF ページ

この `docs` ディレクトリには、GitHub Pages で公開する LINE LIFF 用のページが含まれています。

- **`index.html`**
  - LINE LIFF SDK v2 を読み込み
  - 指定した `LIFF_ID` で `liff.init()` を実行
  - `liff.getProfile()` で取得した `userId` を Google フォームのクエリパラメータとして付与
  - `liff.openWindow()` で Google フォームを外部ブラウザで開く

### 設定値の変更

`index.html` 内の以下の定数を変更することで、別の LIFF やフォームに切り替えられます。

- `LIFF_ID` : LINE Developers で発行された LIFF ID
- `FORM_BASE` : リダイレクト先の Google フォーム URL
- `ENTRY_LINEID` : フォーム側で LINE ID を受け取る項目のエントリ ID（例: `entry.1968653097`）

GitHub Pages の設定で「Branch: main / Folder: /docs」を指定すると、この `index.html` が公開されます。

