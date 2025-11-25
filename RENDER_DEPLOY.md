# 🚀 Renderデプロイ手順（超簡単版）

render.yaml を作成したので、設定が自動化されています！

---

## 方法1: ワンクリックデプロイ（最速）

以下のボタンをクリックするだけでデプロイできます:

[![Deploy to Render](https://render.com/images/deploy-to-render-button.svg)](https://render.com/deploy?repo=https://github.com/bi0407/face-maskLP)

### 手順:
1. 上のボタンをクリック
2. Renderにログイン（GitHubアカウントでログイン可能）
3. 「Create Static Site」をクリック
4. **完了！** 数分で公開されます

---

## 方法2: 手動デプロイ

### ステップ1: Renderにアクセス
https://render.com にアクセスしてログイン

### ステップ2: 新しいStatic Siteを作成
1. ダッシュボードで **「New +」** ボタンをクリック
2. **「Static Site」** を選択

### ステップ3: GitHubリポジトリを接続
1. **「Connect a repository」** をクリック
2. GitHubアカウントを連携（初回のみ）
3. **`face-maskLP`** を検索して選択
4. **「Connect」** をクリック

### ステップ4: 設定（render.yamlがあるので自動入力されます）

以下が自動的に設定されます:
- **Name**: `moist-mask-lp`
- **Branch**: `main`
- **Build Command**: 不要（静的サイト）
- **Publish Directory**: `.`

### ステップ5: デプロイ開始
1. **「Create Static Site」** をクリック
2. デプロイが開始されます（約2-3分）

### ステップ6: 公開URL取得
デプロイ完了後、以下のような公開URLが表示されます:
```
https://moist-mask-lp.onrender.com
```

---

## 📱 デプロイ後の確認

公開URLにアクセスして、以下を確認してください:

✅ ページが正しく表示される
✅ レスポンシブデザインが動作する（スマホ表示も確認）
✅ スクロールアニメーションが動く
✅ すべてのセクションが表示される
✅ CTAボタンがクリックできる

---

## 🔄 更新方法

LPを更新したい場合:

```bash
# ファイルを編集後
git add .
git commit -m "更新内容"
git push
```

**Renderが自動的に再デプロイします！**（約2-3分で反映）

---

## 💰 料金

**完全無料です！**

- 静的サイトホスティング: 無料
- 帯域幅: 100GB/月（十分すぎる）
- SSL証明書: 自動発行（無料）
- カスタムドメイン: 設定可能（無料）

---

## 🌐 カスタムドメイン設定（オプション）

独自ドメインを使いたい場合:

1. Renderのサイトダッシュボードで **「Settings」** を開く
2. **「Custom Domain」** セクションで **「Add Custom Domain」**
3. ドメイン名を入力（例: `www.moistmask.com`）
4. 表示されるDNS設定を、ドメインレジストラで設定

SSL証明書は自動発行されます！

---

## ❓ トラブルシューティング

### デプロイが失敗する
- GitHubリポジトリに `index.html` があるか確認
- `render.yaml` が正しくプッシュされているか確認

### ページが表示されない
- デプロイが完了しているか確認（Renderのダッシュボードで確認）
- URLが正しいか確認
- ブラウザのキャッシュをクリア

### 更新が反映されない
- GitHubに正しくプッシュされているか確認: https://github.com/bi0407/face-maskLP
- Renderで再デプロイが開始されたか確認

---

## 📊 デプロイステータス

デプロイ状況は、Renderのダッシュボードで確認できます:
- **Building**: ビルド中
- **Live**: 公開中（緑色）
- **Failed**: 失敗（赤色）

---

## 🎉 完了！

以上でデプロイ完了です！

公開されたURLをSNSやメールで共有できます。

何か問題があれば、お気軽にお尋ねください！
