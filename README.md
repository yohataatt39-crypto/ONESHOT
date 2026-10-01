# ONE SHOT — GitHub Pages 確認版

スマートフォンから ONE SHOT の画面遷移・レイアウト・評価演出を確認するための静的Web版です。

## GitHub Pages で公開する手順

1. GitHubで新しいリポジトリを作成します（例: `oneshot-preview`）。
2. このフォルダ内のファイルを、リポジトリのルートへすべてアップロードします。
3. GitHubの **Settings → Pages** を開きます。
4. **Build and deployment / Source** を `Deploy from a branch` にします。
5. Branchを `main`、Folderを `/(root)` にして **Save** します。
6. 数分後に表示される GitHub Pages のURLをスマートフォンで開きます。

## スマートフォンでの確認

起動設定画面で **「デモ表示で起動」** を押してください。

デモモードではPC専用のフォルダ選択APIを使わず、ブラウザの `localStorage` と疑似ショットデータを使います。そのため iPhone / Android から画面遷移を確認できます。

既存会員の確認用ログインIDは **1234** です。新規会員登録フローも利用できます。

ショット画面では約1.4秒後に疑似ショットデータを自動投入し、評価演出へ進みます。

## 通常モードについて

PC版Chrome / Edgeでは従来どおり、起動時に以下を指定して実動作を確認できます。

- JSON監視フォルダ
- ユーザデータ・ショット実績データ保管先フォルダ

`showDirectoryPicker()` を利用するため、スマートフォンでは通常モードではなくデモモードを使用してください。

## ファイル構成

- `index.html` — エントリ画面
- `app.css` — UI・レスポンシブ表示・評価演出
- `app.js` — 画面遷移、評価処理、フォルダ監視、デモモード
- `club_definition.csv` — クラブ評価定義の参照用
- `sample_shotinfo.json` — VIEW JSONサンプル
- `.nojekyll` — GitHub Pages用

## 注意

この公開版には個人情報・実利用者のショット履歴・サーバ認証情報を含めないでください。デモモードのデータは閲覧端末のブラウザ内だけに保存されます。
