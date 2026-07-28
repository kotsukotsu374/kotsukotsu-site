# GitHub Pages公開コマンド集

ローカルでのGit管理は完了しています(`git init` 済み、初回コミット済み)。
残りは「GitHubにアカウントで接続する」部分だけです。以下をClaude Code、またはご自身のターミナルで、上から順に実行してください。

## STEP 1. GitHubでリポジトリを作る(ブラウザ操作)

1. https://github.com/new にアクセス(要ログイン)
2. Repository name に `kotsukotsu-site` などお好きな名前を入力
3. Public を選択(GitHub Pagesの無料公開にはPublicが必要)
4. **README、.gitignore、LICENSEは追加しない**(すでにローカルにファイルがあるため)
5. 「Create repository」をクリック

作成すると、以下のような画面にリポジトリのURLが表示されます(例):
```
https://github.com/あなたのユーザー名/kotsukotsu-site.git
```

## STEP 2. ローカルのファイルをGitHubへ送る(ターミナル操作)

このプロジェクトフォルダ(`kotsukotsu-site`)に移動した状態で、以下を実行してください。
`あなたのユーザー名` の部分は実際のGitHubユーザー名に置き換えてください。

```bash
git remote add origin https://github.com/あなたのユーザー名/kotsukotsu-site.git
git push -u origin main
```

初回はGitHubのユーザー名とパスワード(またはトークン)を聞かれることがあります。
パスワードでログインできない場合は、GitHubの案内に従って「Personal Access Token」を発行して、パスワード欄にそれを入力してください。

## STEP 3. GitHub Pagesを有効化する(ブラウザ操作)

1. GitHub上のリポジトリページで「Settings」タブを開く
2. 左メニューの「Pages」をクリック
3. 「Build and deployment」→「Source」を **Deploy from a branch** に設定
4. Branch を **main** / フォルダを **/ (root)** に設定して「Save」

数分待つと、ページ上部に公開URLが表示されます(例):
```
https://あなたのユーザー名.github.io/kotsukotsu-site/
```

これでスマホからもアクセスできる状態になります。

## 困ったときは

- `git push` でエラーが出た場合は、エラーメッセージをそのままClaude Codeに貼り付ければ原因を特定して解決してくれます
- 匿名性のため、GitHubのユーザー名やコミット時の名前(user.name)に本名を使わないよう注意してください(現在は仮の名前 `kotsukotsu` でコミットしてあります)
