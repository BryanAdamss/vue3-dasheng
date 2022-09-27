# 04-Vue 2 项目如何升级到 Vue 3

## 是否要升 vue3

- 是否需要兼容 IE11
  - 是->vue2.7 或 vue2.6+@vue/composition-api
  - 否->vue3

## 升级方式

- `@vue/compat`
  - 一个 Vue 3 的构建版本，提供了兼容 Vue 2 的行为。这个版本默认运行在 Vue 2 下，它的大部分 API 和 Vue 2 保持了一致。当使用那些在 Vue 3 中发生变化或者废弃的特性时，这个版本会提出警告，从而避免兼容性问题的发生，帮助你很好地迁移项目
    - 安装`vue3.x`和`@vue/compat`
    - 将`vue`入口指向`compat`

```js
// package.json
"dependencies": {
  - "vue": "^2.6.12",
  + "vue": "^3.2.19",
  + "@vue/compat": "^3.2.19"
  ...
  },
  "devDependencies": {
    - "vue-template-compiler": "^2.6.12"
    + "@vue/compiler-sfc": "^3.2.19"
  }


// vue.config.js
module.exports = {
  chainWebpack: config => {
    config.resolve.alias.set('vue', '@vue/compat')
    ......
  }
}
```

- 使用[gogocode](https://gogocode.io/zh/docs/vue/vue2-to-vue3)自动化升级
