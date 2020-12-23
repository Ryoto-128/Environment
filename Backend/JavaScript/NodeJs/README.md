# Node.js

>  Node.js はスケーラブルなネットワークアプリケーションを構築するために設計された非同期型のイベント駆動の JavaScript 環境です。  By [Node.js](https://nodejs.org/ja/about/)

## Getting Started / スタートガイド

"nodebrew"でバージョン管理を行い、"node"のインストールを行う。

### Prerequisites / 必要条件

- "Homebrew"のインストール

### Installing / インストール

#### nodebrew

"Homebrew" で"nodebrew"のインストールを行う。

```
brew install nodebrew

echo 'export PATH=$PATH:$HOME/.nodebrew/current/bin' >> ~/.bash_profile
source ~/.bash_profile  #bashの場合
echo 'export PATH=$HOME/.nodebrew/current/bin:$PATH' >> ~/.zprofile
source ~/.zprofile  #zshの場合
```

#### node

"nodebrew"で指定バージョン"node"のインストールを行う。

```
nodebrew ls-remote  #インストール可能リスト
mkdir ~/.nodebrew				#初回のみ
mkdir ~/.nodebrew/src		#初回のみ

nodebrew install-binary <version>		#指定バージョン
or  
nodebrew install-binary stable			#安定バージョン
or
nodebrew install-binary latest			#最新バージョン

nodebrew ls  #インストールしたバージョン・現在のバージョンを確認
nodebrew use <version>  #バージョンを指定
node -v  #バージョンを確認
```



## Reference / 参考サイト

- 不明