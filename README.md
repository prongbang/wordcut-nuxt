# wordcut-nuxt

> My top-notch Nuxt.js project

## Build Setup

``` bash
# install dependencies
$ yarn install

# serve with hot reload at localhost:3000
$ yarn dev

# build for production and launch server
$ yarn build
$ yarn start

# generate static project
$ yarn generate
```

For detailed explanation on how things work, check out [Nuxt.js docs](https://nuxtjs.org).

## Step Config `Wordcut` on Nuxt 

1. Rename `require` to `required` in `wordcut.min.js`

2. Add `wordcut.min.js` to `static/js/` directory

3. Add script in `nuxt.config.js` under ``

```js
head: {
    script: [
        { src: "/js/wordcut.min.js" }
    ]
}
```

4. How to use

```js
let wordcut = required("wordcut");
wordcut.init();
let result = wordcut.cut(this.words).split("|");
console.log("result", result);
```
