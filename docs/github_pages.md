
# 🌍 GitHub Pagesで MkDocsサイトを公開する


## ✅ 1. `gh-pages` ブランチを作成＆プッシュ
まず、MkDocs の静的サイトを GitHub Pages 用の `gh-pages` ブランチにアップロードします。

### ① MkDocs をビルド
```
mkdocs build
```

### ② Git の初期化（最初だけ）
```
git init
git add .
git commit -m "First commit"
```

### ③ gh-pages ブランチを作成＆切り替え
```
git branch -M gh-pages
```

### ④ GitHub リポジトリを追加
```
git remote add origin https://github.com/あなたのGitHubユーザー名/リポジトリ名.git
```

### ⑤ `gh-pages` ブランチにプッシュ
```
git push -u origin gh-pages
```