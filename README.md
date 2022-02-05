# Terakoya

初学者向けのプログラミング教材です。

## コンセプト

* 漢字が読める中学生が理解できる
* 作りながら学ぶ
* 終えたらなんか成果物がある

## Run

```shell
# serve with hot reload at localhost:3000
$ npm run dev
```

## Build Setup

```bash
# install dependencies
$ npm install

# build for production and launch server
$ npm run build
$ npm run start

# generate static project
$ npm run generate
```

## Use Library

- [markdown-it](https://github.com/markdown-it/markdown-it)
  npm add @nuxtjs/markdownit npm install highlight.js npm install markdown-it-emoji
- nuxt-buefy
- sass-loader node-sass

## ディレクトリ構造

Nuxt.jsは`pages`配下のvueファイルについて`router`を自動生成します。

そのため以下のルールで進行します。

- `page`配下にページコンポーネントを作成
- `src`に表示する記事と画像を置きます

## 記述ルール

- スペースは半角

## ルーティング

Nuxt.jsは`pages`配下のvueファイルについて`router`を自動生成します。 以下例の場合、下のようなrouterを作成します。 ※スネークケースのファイルはエラーになります。

```html
pages/
--| user/
-----| index.vue
-----| one.vue
--| index.vue
```

```vue
router: {
routes: [
{
name: 'index',
path: '/',
component: 'pages/index.vue'
},
{
name: 'user',
path: '/user',
component: 'pages/user/index.vue'
},
{
name: 'user-one',
path: '/user/one',
component: 'pages/user/one.vue'
}
]
}
```

## 参考

### markdown-it

https://techblog.roxx.co.jp/entry/2019/01/24/190000
