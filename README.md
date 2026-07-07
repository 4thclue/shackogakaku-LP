# 社長の画角 LP — Vercel デプロイ

静的サイトです。ビルド不要。`index.html` をそのまま公開します。

## 構成
```
vercel-deploy/
├─ index.html            # LP本体（画像・SVG・サムネはすべて埋め込み済み）
├─ videos/
│  ├─ template-1.mp4     # パターン1（クリックで再生）
│  ├─ template-2.mp4     # パターン2
│  └─ template-3.mp4     # パターン3
└─ vercel.json           # 静的配信設定（動画のキャッシュ）
```
※フォントは Google Fonts(CDN) から読み込みます。

## デプロイ方法（どちらか）

### A. ブラウザでドラッグ&ドロップ
1. https://vercel.com/new を開く
2. この `vercel-deploy` フォルダごとアップロード（または GitHub に push して Import）
3. Framework Preset は **Other**、Build Command / Output は空のまま → Deploy

### B. CLI
```bash
cd vercel-deploy
npx vercel        # プレビュー公開
npx vercel --prod # 本番公開
```
Framework を聞かれたら **Other**、設定はすべて空（デフォルト）でEnter。

## 公開後にやること
- 問い合わせ先メール: `contact@4thclue.com`（変更したい場合は index.html 内を編集）
- 各CTAボタンのリンク先: index.html 内の `#contact` を実際のフォームURLに差し替え
