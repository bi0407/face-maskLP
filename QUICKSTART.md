# ⚡️ クイックスタートガイド

このガイドでは、最速でLPを公開する手順を説明します。

---

## 🚀 3ステップで公開

### ステップ1: GitHubにプッシュ（5分）

```bash
# GitHubで新しいリポジトリを作成後、以下を実行:
git remote add origin https://github.com/あなたのユーザー名/リポジトリ名.git
git branch -M main
git push -u origin main
```

### ステップ2: Renderに連携（3分）

1. https://render.com にアクセス
2. 「New +」→「Static Site」
3. GitHubリポジトリを選択
4. Publish Directory: `.`（ドット）
5. 「Create Static Site」

### ステップ3: 公開完了！（自動）

数分でデプロイ完了。公開URLが表示されます!

---

## 💻 ローカルでプレビュー

### 方法1: ブラウザで直接開く

```bash
open index.html
```

### 方法2: ローカルサーバーで開く（推奨）

#### Python（macOSに標準搭載）
```bash
python3 -m http.server 8000
```
その後、ブラウザで http://localhost:8000 を開く

#### Node.js（インストールされている場合）
```bash
npx http-server
```

---

## 📝 よく使うコマンド

### ファイルを更新してプッシュ
```bash
git add .
git commit -m "更新内容"
git push
```

### 変更を確認
```bash
git status
git diff
```

### ブランチを確認
```bash
git branch
```

---

## 🔗 重要なリンク

- **詳細なデプロイ手順**: `DEPLOYMENT_GUIDE.md` を参照
- **プロジェクト概要**: `README.md` を参照
- **LPコピー**: `LP_COPY.md` を参照

---

## ❓ 困ったときは

### デプロイエラーが出る
→ `DEPLOYMENT_GUIDE.md` のトラブルシューティングを確認

### Gitコマンドがわからない
→ 基本的なコマンドは上記の「よく使うコマンド」を参照

### LPの内容を変更したい
→ `index.html` を直接編集して、再度プッシュ

---

以上！簡単ですね！

何か問題があれば、お気軽にお尋ねください。
