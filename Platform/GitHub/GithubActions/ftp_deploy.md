# FTP Deploy / GitHub Actions

GitHubアクションを利用して自動FTPデプロイを行う。

## Getting Started / スタートガイド

### Prerequisites / 必要条件

- READEME.mdを参照

### Code / コード

```
jobs:
  FTP-Deploy-Action:
    name: FTP-Deploy-Action     # JOBの名前
    runs-on: ubuntu-latest      # 仮想環境の種類を指定
    steps:
      - uses: actions/checkout@main   # リポジトリのデータを仮想環境にチェックアウトしてくるアクションを実行する

      - name: FTP-Deploy-Action
        uses: SamKirkland/FTP-Deploy-Action@2.0.0   # FTPを使ってサーバーにDeployするアクションを実行
        env:                                        # FTP環境の設定を行う
          FTP_SERVER: ${{ secrets.FTP_SERVER }}     # FTPサーバーのURLを設定
          FTP_USERNAME: ${{ secrets.FTP_USERNAME }} # FTPのユーザー名を設定
          FTP_PASSWORD: ${{ secrets.FTP_PASSWORD }} # FTPのパスワードを設定
          LOCAL_DIR: ./<dirname>/                   # どのディレクトリのデータをアップロードするか
          REMOTE_DIR: /<dirname>/       # リモートのどのディレクトリにアップロードするか
                                        # rootはサーバー側で設定したFTPアカウントの接続先dir
          ARGS: --delete

```

## Reference / 参考サイト

- [GitHub Actionsを利用してXserverに自動デプロイする](https://qiita.com/ikeyansaza/items/96fcd40b5a6ea616e913)
- [GitHub Actionsを使ったFTPの自動デプロイ](https://qiita.com/chieeeeno/items/6be835c74d6d7f597c6a)

