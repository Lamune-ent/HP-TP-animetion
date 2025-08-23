Lamune. 背景ヒーロー動画 埋め込みパッケージ

このフォルダをそのまま Netlify / Vercel / 自社サーバ にアップすれば、
背景動画が自動再生・ループで表示されます（音なし）。

■同梱ファイル
- index.html     …… 同じフォルダに movie.mp4 を置いて使う想定です
- index-drive.html …… Google Drive 直リンクのテスト用（多くの環境でブロックされます）
- README.txt

■使い方（最短：Netlify ドラッグ&ドロップ）
1) このフォルダに、あなたの動画ファイルを "movie.mp4" という名前で置く
2) https://app.netlify.com/drop にアクセス
3) フォルダごとドラッグ&ドロップ（index.html と movie.mp4 を含む）
4) 発行された URL を Googleサイト →「挿入」→「埋め込む」→「URL」 で貼り付け
   - 例: https://xxxxx.netlify.app/

■Vercel（同様）
1) 新規プロジェクト → Framework: Other → このフォルダをアップロード
2) デプロイ後の URL を Googleサイトに埋め込み

■自社サーバ
1) 任意の公開ディレクトリに index.html と movie.mp4 を一緒に配置
2) index.html の URL を Googleサイトに埋め込み

■Tips
- モバイル自動再生には "muted/playsinline/autoplay" 指定が必要（index.htmlで設定済み）
- 初回読み込みを早くするには、movie.mp4 を 4〜8 Mbps 程度に再エンコード（H.264/AAC推奨）
- 16:9 の素材を想定、表示は object-fit: cover で画面いっぱいにフィット

■トラブルシュート
- 真っ黒/再生不可：
  - Google Drive 直リンクはブロックされがち → Netlify/Vercel/自社サーバに置き換え
  - 動画コーデックが非対応 → H.264 + AAC に再エンコード
- 音が出ない：
  - モバイルの自動再生条件のため muted 前提。音を出す場合はユーザー操作で再生してください。

© Lamune.
