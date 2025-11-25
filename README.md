# MoisT Mask ランディングページ

うるおいで、未来を変える。

[![Deploy to Render](https://render.com/images/deploy-to-render-button.svg)](https://render.com/deploy?repo=https://github.com/bi0407/face-maskLP)

## 概要

MoisT Mask の商品紹介ランディングページです。
EGF・プラセンタ・セラミド配合の日本製フェイスマスクを、
魅力的に紹介するデザインになっています。

## 特徴

- レスポンシブデザイン（PC・タブレット・スマートフォン対応）
- モダンでエレガントなUI/UX
- スクロールアニメーション搭載
- 購買意欲を最大化するコピーライティング
- 日本のコスメEC業界のベストプラクティスを採用

## 技術スタック

- HTML5
- CSS3（アニメーション・グラデーション・レスポンシブ対応）
- Vanilla JavaScript（スムーズスクロール・Intersection Observer API）
- Google Fonts（Noto Sans JP, Playfair Display）

## 🚀 デプロイ

### Renderでワンクリックデプロイ（推奨）

上部の「Deploy to Render」ボタンをクリックするだけで、すぐに公開できます！

詳細な手順は [`RENDER_DEPLOY.md`](RENDER_DEPLOY.md) を参照してください。

### その他のプラットフォーム

このサイトは静的HTMLなので、以下のプラットフォームでも簡単にデプロイできます:

- **Render** - 完全無料、SSL自動、推奨
- GitHub Pages - GitHubで簡単公開
- Netlify - 高速デプロイ
- Vercel - Next.js開発元

## ローカルでの確認

```bash
# プロジェクトディレクトリで
open index.html
```

または、ローカルサーバーを起動:

```bash
# Pythonを使用する場合
python -m http.server 8000

# Node.jsを使用する場合
npx http-server
```

その後、ブラウザで `http://localhost:8000` にアクセス。

## ファイル構成

```
face-maskLP/
├── index.html              # メインLP（レスポンシブ対応）
├── LP_COPY.md              # LPコピー（マークダウン版）
├── README.md               # このファイル
├── DEPLOYMENT_GUIDE.md     # 詳細なデプロイ手順
├── RENDER_DEPLOY.md        # Render専用デプロイガイド
├── QUICKSTART.md           # 3ステップクイックガイド
├── render.yaml             # Render自動設定ファイル
└── .gitignore             # Git除外設定
```

## 製作情報

- **製品**: MoisT Mask
- **製造販売元**: 株式会社ティエラコスメティクス
- **製造国**: 日本（MADE IN JAPAN）

## ライセンス

© 2025 MoisT Mask. All rights reserved.
