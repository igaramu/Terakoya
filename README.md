# 匠コード

初学者向けのプログラミング教材(ドキュメント)です。

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

- マークダウンのプラグイン
  - [markdown-it](https://github.com/markdown-it/markdown-it)
    `npm add @nuxtjs/markdownit npm install highlight.js npm install markdown-it-emoji`
  - https://techblog.roxx.co.jp/entry/2019/01/24/190000
- デザイン
  - nuxt-buefy
- SCSSのプラグイン
  - sass-loader node-sass
- SVGのプラグイン
  - [vue-svg-loader](https://github.com/visualfanatic/vue-svg-loader)

## ディレクトリ構造

Nuxt.jsは`pages`配下のvueファイルについて`router`を自動生成します。そのため以下のルールで進行しています。

- ページ基礎 -> `pages`下にページコンポーネント(vueファイル)を作成し、本文は以下のmdファイルを読み込む
- 記事内容 -> `src`に記事(mdファイル)と画像を置く

### 例）mdファイルの表示方法

名前を`typescript`側で定義します。
```typescript
import Docs from '/src/main/docs.md';

Vue.extend({
  data() {
    return {
      model: HTML_1
    }
  }
})
```

renderで表示させます。
```vue
<div v-html="$md.render(model)"></div>

```

### ルーティング例

以下例の場合、下のような`router`が自動生成されます。

※スネークケースのファイルはエラーになります。

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

## md記述ルール

- スペースは半角
- 文中の`()`は全角
- 見出し3まで頭にNoをつける
- h1（記事タイトル）はvueファイルに記載する


## color
- BFA486
- F5EAD3
- 95A797
- 637B85
![](C:/Users/igara/Downloads/i-am-sorry-by-schemecolor.png)
