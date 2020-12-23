# GithubActions

>  GitHub Actionsを使用すると、ワールドクラスのCI / CDですべてのソフトウェアワークフローを簡単に自動化できます。 GitHubから直接コードをビルド、テスト、デプロイでき、コードレビュー、ブランチ管理、問題のトリアージを希望どおりに機能させます。  By [GitHub](https://github.co.jp/features/actions)

## Getting Started / スタートガイド

リポジトリ内の特定ディレクトリに.yml or .yamlファイルを作成することで実装する。

### Prerequisites / 必要条件

- 事前にリポジトリの作成を行う。

### Installing / インストール

リポジトリ内に特定ディレクトリとファイルを作成する。  "<filename>"は変更する

```
touch /.github/workflows/<filename>.yaml
```

"<filename>.yaml"の編集を行う。例）FTPデプロイ

```
on:
  push:                 # プッシュした時に実行
      branches:           # ブランチを指定
      - main    # mainブランチ
name: Deploy  # アクションの名称
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

- [Github Actionsの使い方メモ](https://qiita.com/HeRo/items/935d5e268208d411ab5a)
