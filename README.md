# GatsbyJS

## 開発環境の構築

- バージョン確認

  ```sh
  $ node -v
  v16.14.2
  $ npm -v
  8.7.0
  ```

- GatsbyJS グローバルインストール

  ```sh
  $ npm install -g gatsby-cli
  $ gatsby -v
  Gatsby CLI version: 4.18.1
  ```

- GatsbyJS テンプレート（gatsby-starter-hello-world）のインストール

  ```sh
  $ gatsby new gatsbyjs-site https://github.com/gatsbyjs/gatsby-starter-hello-world
  ```

- 開発環境動作確認

  ```sh
  $ cd gatsbyjs-site
  $ gatsby develop
  ```

  http://localhost:8000/

## 追加ライブラリ導入

- プラグインのインストール

  ```sh
  ローカルファイルシステムへのアクセス用プラグイン導入
  $ npm install gatsby-source-filesystem

  マークダウンファイルのHTML変換するGraphQL用プラグイン導入
  $ npm install gatsby-transformer-remark
  ```

- gatsby-config.js にプラグイン設定

  ```js
  module.exports = {
    ...
    plugins: [
      {
        resolve: `gatsby-source-filesystem`,
        options: {
          name: `src`,
          path: `${__dirname}/src/`,
        },
      },
      "gatsby-transformer-remark",
    ],
  }
  ```

## 参考文献

- [REFFECT ｜基礎から始める GatsbyJS 入門](https://reffect.co.jp/react/gatsby-basic-tutorial-for-beginners#Blog_Starter)
- [YouTube ｜マイケル｜ Gatsby 入門](https://bit.ly/3PytG4m)
- [GatsbyJS 公式サイト｜ How to use gatsby-cli](https://www.gatsbyjs.com/docs/reference/gatsby-cli/)
- [GatsbyJS テンプレート｜ gatsby-starter-blog](https://www.gatsbyjs.com/starters/gatsbyjs/gatsby-starter-blog)
