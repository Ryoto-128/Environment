# Node.js

>  Node.js はスケーラブルなネットワークアプリケーションを構築するために設計された非同期型のイベント駆動の JavaScript 環境です。  By [Node.js](https://nodejs.org/ja/about/)

## Getting Started / スタートガイド

"nodenv"でバージョン管理を行い、"node"のインストールを行う。

### Prerequisites / 必要条件

- "Homebrew"のインストール

### Installing / インストール

#### nodenv

"Homebrew" で"nodenv"のインストールを行う。

```
brew install nodenv

echo 'eval "$(nodenv init -)"' >> ~/.bash_profile
source ~/.bash_profile  #bashの場合
echo 'eval "$(nodenv init -)"' >> ~/.zprofile
source ~/.zprofile  #zshの場合
```

#### node

"nodebrew"で指定バージョン"node"のインストールを行う。

```
nodenv install --list
nodenv install <version>

# globalに設定する場合
nodenv global <version>
nodenv rehash

# localに設定する場合
pyenv local <version>
pyenv rehash

node -v  #バージョンを確認
```



## Reference / 参考サイト

- 不明
