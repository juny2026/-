# 測量写真撮影アプリ：iPhone PWAテスト版

## 公開手順（GitHub Pages）
1. GitHubで新規リポジトリを作成（公開リポジトリの場合、ファイルは誰でも閲覧可能）。
2. このZIPを展開し、`index.html`、`manifest.webmanifest`、`sw.js`、アイコン2個をリポジトリのルートにアップロード。
3. Settings → Pages → Build and deployment → Deploy from a branch → main / (root) → Save。
4. 公開されたHTTPSのURLをiPhoneのSafariで開く。
5. Safariの共有メニュー →「ホーム画面に追加」→「追加」。

## 重要
- 公開するのはアプリ本体だけです。サンプルDXFの埋め込みは削除しました。
- DXFはiPhoneの「ファイル」から読み込んでください。DXFや写真をサーバーに送信する処理は含まれていません。
- 写真は端末内のIndexedDBに保存しますが、容量不足・ブラウザデータ削除などで失われる可能性があります。必ずZIPでこまめに書き出してください。
- 現在の試作版はカメラ入力でiOSがHEIC形式を返す場合、JPEGへの変換を保証しません。ZIP内の拡張子と実データを確認してください。
- サービスワーカーによりアプリ本体はキャッシュされますが、初回はオンラインが必要です。
- アプリの更新後に旧版が表示される場合、Safariで再読み込みしてください。
