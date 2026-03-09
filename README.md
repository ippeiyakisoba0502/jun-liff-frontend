## jun-liff-frontend

LINE LIFF を利用して、顧客情報登録フォーム（Google フォーム）へユーザーの LINE ID を埋め込んで遷移するためのフロントエンドです。

- **使用技術**
  - 静的 HTML / JavaScript
  - LINE LIFF SDK v2 (`https://static.line-scdn.net/liff/edge/2/sdk.js`)
  - Google フォーム

- **主要ファイル（例）**
  - `regist_customer_info/docs/index.html`  
    - LIFF の初期化
    - `liff.getProfile()` で取得した `userId` をクエリパラメータとして Google フォーム URL に付与
    - `liff.openWindow()` でフォームを外部ブラウザで開く

### 開発者向けメモ

- **LIFF ID** や **Google フォーム URL / エントリ ID** を変更する場合は `regist_customer_info/docs/index.html` 内の以下定数を書き換えてください。

  - `LIFF_ID`
  - `FORM_BASE`
  - `ENTRY_LINEID`

- LIFF アプリとして正しく動かすには、LINE Developers コンソールで設定した LIFF URL にこの `index.html` をホスティングしている URL を登録してください。

