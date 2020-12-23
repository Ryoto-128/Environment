# pipenv

>  Pythonで開発するときに，プロジェクト毎のパッケージ管理や仮想環境の構築を簡単に自動で行ってくれるツールです．  By [Pipenvを使ったPython開発まとめ](https://qiita.com/y-tsutsu/items/54c10e0b2c6b565c887a)

### pip

> pipは、The Python Package Indexに公開されているPythonパッケージのインストールなどを行うユーティリティで、Python 3.4以降には、標準で付属しています。  By [Python Japan](https://www.python.jp/install/windows/pip.html)

## Getting Started / スタートガイド

"pip"で使用し、"pipenv"のインストールを行う。

### Prerequisites / 必要条件

- "Python"のインストール

### Installing / インストール

"pip"は"Python"インストール時に自動でインストール済み。  "pip"で"pyenv"のインストールを行う。

```
pip install pipenv
```

### How to / 使用方法

#### Flow / 流れ

```
pipenv --python <version>	# 初回時	# 初期化
or
pipenv install						# クローン時	# Pipfileから使用パッケージのインストール
or
pipenv sync								# クローン時	# Pipfile.lockから使用パッケージのインストール

pipenv install <package_name>

pipenv shell	# 仮想環境に入る
or
pipenv run python <filename>.py # その場で実行
```

#### Cheatsheet / チートシート

```

```

## Reference / 参考サイト

- [Pipenvを使ったPython開発まとめ](https://qiita.com/y-tsutsu/items/54c10e0b2c6b565c887a)