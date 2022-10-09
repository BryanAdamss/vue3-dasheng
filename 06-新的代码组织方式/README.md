# 06-新的代码组织方式

> `Composition API + <script setup>` 到底好在哪里？

## `Composition API`

- 优点
  - 拆分粒度更细，逻辑更加方便复用
- 缺点
  - 灵活性太高，缺少约束，水平层次不齐时，容易写出意大利面条式代码

## `<script setup>`

- 优点
  - 减少了`script`中的嵌套层级
  - 无需注册组件，引入即可使用
- 缺点
  - 无法直接设置`name`、`inhertAttrs`等属性
