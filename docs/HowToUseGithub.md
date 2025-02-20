!!! note

    GitHub では リモートリポジトリ（GitHub上のフォルダ） に ローカルリポジトリ（自分のPC上のフォルダ） をアップロードして管理します。



## ✅ 1. GitHub で新しいリポジトリを作成
- GitHub にログイン
- 右上の「＋」→「New repository」をクリック
- リポジトリ名を入力（例: my-mkdocs-site）
- 「Public（公開）」を選択
- 「Create repository」をクリック
👉 ここで GitHub 上に空のリポジトリが作成されます！ 🎉


## ✅ 2. ローカルに Git をセットアップ
ローカルの test_upload フォルダを Git 管理する

- VS Code のターミナルを開く（ Ctrl + @ ）
- test_upload ディレクトリへ移動 (移動済みのはず_pwdで確認)
```
cd /Users/shambata/my-project/test_upload
```

- Git を初期化
```
git init
```

- GitHub のリモートリポジトリを登録
```
git remote add origin https://github.com/shambata/my-mkdocs-site.git
```

- .gitignore を作成して venv/ を除外
```
echo "venv/" > .gitignore
```

## ✅ 3. MkDocs の静的サイトをアップロード

- MkDocs をビルド
```
mkdocs build
```
(venvが有効になってない場合は、`source venv/bin/activate` をしてから再度ビルドする)

- ファイルを Git に追加
```
git add .
```

- コミット（変更を記録）
```
git commit -m "First commit"
```

- gh-pages ブランチを作成
```
git branch -M gh-pages
```

- GitHub にプッシュ
```
git push -u origin gh-pages
```

## ✅ 4. GitHub Pages を有効化
- GitHub のリポジトリページを開く
- 「Settings」→「Pages」へ移動
- 「Branch」 を gh-pages に設定
- 「Save」ボタンをクリック
- 発行された URL を確認
```
https://あなたのGitHubユーザー名.github.io/my-mkdocs-site/
```

🎉 これで公開完了！

## 📌 次回更新するときは
```
mkdocs build
git add .
git commit -m "Update site"
git push origin gh-pages
```
これだけで 更新したサイトが GitHub Pages に反映 されます！🚀