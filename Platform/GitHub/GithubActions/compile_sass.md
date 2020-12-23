# Compile Sass / GitHub Actions

GitHubアクションを利用して自動コンパイルを行う。

## Getting Started / スタートガイド

### Prerequisites / 必要条件

- READEME.mdを参照

### Code / コード

```
jobs:
  Compile-Sass:
    name: Compile-Sass
    runs-on: ubuntu-latest 
    steps:
      - uses: actions/checkout@main
      
      # Sassのbuild
      - name: Make destination directory for compiled CSS
        run: mkdir -vp ./public_html/assets/css/  # 出力先dirの作成

      - name: Compile CSS from SCSS files
        uses: gha-utilities/sass-build@v0.2.9
        with:
          source: ./public_html/assets/sass/app.scss    # 入力先Fileの設定
          destination: ./public_html/assets/css/app.css   # 出力先Fileの設定

```

## Reference / 参考サイト

- [Sass Build](https://github.com/marketplace/actions/sass-build)

