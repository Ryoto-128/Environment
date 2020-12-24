# Scrapy

>  Scrapyは、Webサイトをクロールし、構造化されたデータを抽出するためのアプリケーション・フレームワークです。データ・フレームワークは、データ・マイニング、情報処理、履歴アーカイブなど、さまざまな有用なアプリケーションに使用できます。
>
>  Scrapyは元々「ウェブ・スクレイピング([web scraping](https://en.wikipedia.org/wiki/Web_scraping))」用に設計されていましたが、API([Amazon Associates Web Services](https://affiliate-program.amazon.com/gp/advertising/api/detail/main.html) など)を使用してデータを抽出したり、汎用のWebクローラーとして使用することもできます。  By [doc-ja-scrapy](https://doc-ja-scrapy.readthedocs.io/ja/latest/intro/overview.html)

## Getting Started / スタートガイド

"pip"もしくは"pipenv"で、"scrapy"のインストールを行う。

### Prerequisites / 必要条件

- "Python"のインストール

### Installing / インストール

"pip"で、"scrapy"のインストールを行う。

```
pip install scrapy
```

### version / version確認

```
scrapy version
```

### Project start / 開発開始

#### Construction of Project environment / Project環境の構築

```
scrapy startproject <project name>　# Scrapyプロジェクトを作成
scrapy genspider <spider name> <target domain>	# spidersフォルダーに新しいスパイダーを作成
```

#### Run / 実行

```
scrapy crawl <spider name>	# スパイダーを使用してクロールを開始
```



## Reference / 参考サイト

- [Scrapy 1.7 文書](https://doc-ja-scrapy.readthedocs.io/ja/latest/topics/commands.html#std:command-crawl)

