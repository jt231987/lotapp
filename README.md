# SZK動態表

採卵養鶏場向け生産動態チャートアプリです。

## 機能
- ロット餌付け日・アウト日齢を入力してグラフ表示
- 横軸：月（無限スクロール）、縦軸：日齢（30日単位、最大690日）
- 育成期（0〜移動日）はオレンジ、移動後はロット色で描画
- 四角マーカーをドラッグして移動日を変更（上限150日）
- 矢印先端をドラッグしてアウト日齢を変更
- マウスホバーで日齢・移動日をリアルタイム表示
- 今日の日付ライン表示
- ダークモード対応

## Vercelへのデプロイ（最短手順）

### 方法1: Vercel CLI（一番簡単）
```bash
npm install -g vercel
vercel
```
ログイン後、すべてEnterで完了。URLが発行されます。

### 方法2: GitHub経由
1. GitHubに新しいリポジトリを作成
2. このフォルダをpush
   ```bash
   git init
   git add .
   git commit -m "first commit"
   git remote add origin https://github.com/あなたのユーザー名/szk-chart.git
   git push -u origin main
   ```
3. https://vercel.com にアクセス → New Project
4. GitHubリポジトリを選択 → Deploy（設定不要）

## ローカルで確認する場合
```bash
npm install
npm run dev
```
→ http://localhost:5173 で動作確認できます

## 注意
- データはブラウザのメモリのみに保存されます（ページリロードでリセット）
- データ永続化が必要な場合はlocalStorageやバックエンドの追加が必要です
