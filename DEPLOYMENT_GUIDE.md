# 🚀 GitHub & Render デプロイ手順書

このガイドでは、MoisT Mask LPをGitHubにプッシュし、Renderで公開する手順を説明します。

---

## 📋 前提条件

- GitHubアカウントを持っている
- Renderアカウントを持っている（無料で作成可能）
- Gitがインストールされている

---

## ステップ1: GitHubリポジトリの作成

### 1-1. GitHubにログイン
https://github.com にアクセスしてログインします。

### 1-2. 新しいリポジトリを作成
1. 右上の「+」ボタンをクリック → 「New repository」を選択
2. リポジトリ名を入力（例: `moist-mask-lp`）
3. 「Public」または「Private」を選択
4. **「Initialize this repository with a README」はチェックしない**（既にローカルで作成済みのため）
5. 「Create repository」をクリック

### 1-3. リポジトリURLをコピー
作成したリポジトリのページに表示されるURLをコピーします。
例: `https://github.com/あなたのユーザー名/moist-mask-lp.git`

---

## ステップ2: ローカルからGitHubへプッシュ

### 2-1. ターミナルを開く
すでに `/Users/shiori/Desktop/face-maskLP` ディレクトリにいることを確認してください。

### 2-2. GitHubリポジトリをリモートに追加
```bash
git remote add origin https://github.com/あなたのユーザー名/moist-mask-lp.git
```

> **注意**: `あなたのユーザー名` を実際のGitHubユーザー名に置き換えてください。

### 2-3. プッシュする
```bash
git branch -M main
git push -u origin main
```

GitHubのユーザー名とパスワード（またはPersonal Access Token）を求められた場合は入力してください。

### 2-4. GitHubで確認
ブラウザでGitHubリポジトリを開き、ファイルがアップロードされていることを確認します。

---

## ステップ3: Renderでデプロイ

### 3-1. Renderにログイン
https://render.com にアクセスしてログインします。
（アカウントがない場合は、GitHubアカウントで無料登録できます）

### 3-2. 新しいStatic Siteを作成
1. ダッシュボードで「New +」ボタンをクリック
2. 「Static Site」を選択

### 3-3. GitHubリポジトリを連携
1. 「Connect a repository」セクションで、GitHubアカウントを連携
2. 先ほど作成した `moist-mask-lp` リポジトリを選択
3. 「Connect」をクリック

### 3-4. デプロイ設定
以下の設定を入力します:

| 項目 | 設定値 |
|------|--------|
| **Name** | `moist-mask-lp`（任意の名前） |
| **Branch** | `main` |
| **Build Command** | （空白のままでOK） |
| **Publish Directory** | `.`（ドット1つ） |

### 3-5. デプロイを開始
1. 「Create Static Site」ボタンをクリック
2. デプロイが自動的に開始されます（数分かかります）
3. デプロイが完了すると、公開URLが表示されます

例: `https://moist-mask-lp.onrender.com`

---

## ステップ4: 公開URLで確認

### 4-1. URLにアクセス
Renderから提供されたURLをブラウザで開きます。

### 4-2. 動作確認
- レスポンシブデザインが正しく表示されているか
- スクロールアニメーションが動作しているか
- すべてのセクションが表示されているか

を確認してください。

---

## 🎉 完了!

おめでとうございます! MoisT Mask LPが公開されました!

公開されたURLは以下のような形式です:
```
https://moist-mask-lp.onrender.com
```

このURLをSNSやメールで共有できます。

---

## 📱 モバイル表示の確認方法

### Chrome DevTools を使用
1. 公開されたページを開く
2. 右クリック → 「検証」
3. デバイスツールバーアイコン（📱）をクリック
4. 様々なデバイスサイズで表示を確認

---

## 🔄 更新方法

LPを更新したい場合:

1. ローカルでファイルを編集
2. Gitでコミット:
   ```bash
   git add .
   git commit -m "更新内容の説明"
   git push origin main
   ```
3. Renderが自動的に再デプロイします（数分で反映）

---

## 🆓 料金について

### GitHub
- パブリックリポジトリは無料
- プライベートリポジトリも無料（ただし一部制限あり）

### Render
- 静的サイトは **完全無料**
- 帯域幅制限: 100GB/月（十分すぎる容量）
- カスタムドメインも無料で設定可能

---

## 🌐 カスタムドメインの設定（オプション）

独自ドメイン（例: `www.moistmask.com`）を使いたい場合:

### Renderでの設定
1. Renderのサイトダッシュボードで「Settings」を開く
2. 「Custom Domain」セクションで「Add Custom Domain」をクリック
3. ドメイン名を入力（例: `www.moistmask.com`）
4. 表示されるDNS設定をドメインレジストラ（お名前.com、ムームードメインなど）で設定

### SSL証明書
Renderは自動的に無料のSSL証明書（Let's Encrypt）を発行します。

---

## ❓ トラブルシューティング

### デプロイが失敗する場合
- Publish Directoryが `.` になっているか確認
- GitHubリポジトリに `index.html` があるか確認

### ページが表示されない場合
- デプロイが完了しているか確認（Renderのダッシュボードで確認）
- ブラウザのキャッシュをクリアして再読み込み

### アニメーションが動かない場合
- JavaScriptのエラーがないかブラウザのコンソールで確認
- 別のブラウザで試してみる

---

## 📞 サポート

問題が解決しない場合は、以下をご確認ください:

- **Renderドキュメント**: https://render.com/docs/static-sites
- **GitHubドキュメント**: https://docs.github.com/ja

---

## 🎨 次のステップ（オプション）

### アクセス解析の導入
Google Analytics や Microsoft Clarity を導入して、訪問者の行動を分析できます。

### A/Bテストの実施
複数バージョンのLPを作成して、コンバージョン率を比較できます。

### SEO最適化
- メタディスクリプションの追加
- OGP（Open Graph Protocol）の設定
- 構造化データの追加

---

以上で、MoisT Mask LPの公開手順は完了です!

質問があれば、いつでもお気軽にお尋ねください。
