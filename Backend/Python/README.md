# Python

>  Pythonは汎用的なプログラミング言語の利用度調査などでは、常に高い位置を占めている。システム管理やツール・アプリケーション開発・科学技術計算・Webシステムなどで広く利用されている。  By [Python Japan](https://www.python.jp/pages/about.html)

## Getting Started / スタートガイド

"Pyenv"でバージョン管理を行い、"Python"のインストールを行う。

### Prerequisites / 必要条件

- "Homebrew"のインストール

### Installing / インストール

#### nodebrew

"Homebrew" で"pyenv"のインストールを行う。

```
#pyenv/pipenv
brew install pyenv

echo "eval '$(pyenv init -)'" >> ~/.bash_profile
echo 'export PYENV_ROOT=$HOME/.pyenv' >> ~/.bash_profile
echo 'export PATH=$PATH:$PYENV_ROOT/bin' >> ~/.bash_profile
source ~/.bash_profile #bashの場合

echo "eval '$(pyenv init -)'" >> ~/.zprofile
echo 'export PYENV_ROOT=$HOME/.pyenv' >> ~/.zprofile
echo 'export PATH=$PATH:$PYENV_ROOT/bin' >> ~/.zprofile
source ~/.zprofile #zshの場合
```

#### Python

"pyenv"で指定バージョン"Python"のインストールを行う。

```
pyenv install --list
pyenv install <version>

# globalに設定する場合
pyenv global <version>
pyenv rehash

# localに設定する場合
pyenv local <version>
pyenv rehash
```

### Version確認

```
python --version
```

## Reference / 参考サイト

- [MacでPython使う時の最低限のメモ（pyenv編）](https://qiita.com/zaburo/items/dd1a8323633035614efc)

