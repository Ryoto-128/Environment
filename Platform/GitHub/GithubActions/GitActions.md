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

"<filename>.yaml"の編集を行う。

```
until finished
終わるまでのコマンドの例を繰り返します
```

End with an example of getting some data out of the system or using it for a little demo
このシステムが出力するデータの例とか、あるいはちょっとしたデモを示して終わります

## Running the tests / テストの実行

Explain how to run the automated tests for this system
自動テストをどのように実行するかをここで説明します

### Break down into end to end tests / e2e テストまで詳解する場合

Explain what these tests test and why
何のためのテストでどうしてそれを行うのかを説明します

```
Give an example
コマンドで例を示します
```

### And coding style tests / それからコーディングスタイルのテスト

Explain what these tests test and why
何のためのテストでどうしてそれを行うのかを説明します

```
Give an example
コマンドで例を示します
```

## Deployment / デプロイ

Add additional notes about how to deploy this on a live system
実際のシステムにデプロイするための補足的な説明を行います