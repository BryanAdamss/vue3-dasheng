# 07-深入理解 Vue 3 的响应式机制

## vue2

- 发布订阅+数据劫持
- 基于`Object.defineProperty`实现
- 缺点
  - 深层递归，性能问题
  - 无法对象监听属性的增/删，需借助`$set`和`$delete`
  - 特殊数据结构无法监听，如`set`、`map`
  - 无法监测数组`length`变化
  - 无法监测数组通过索引设置值的变化

## vue3

- 原生代理实现
- 基于`Proxy`实现
- 缺点
  - 无法兼容 IE

## 对比

![https://static001.geekbang.org/resource/image/b5/11/b5344de85923a2ba8bea60283b491711.png?wh=1336x650](https://static001.geekbang.org/resource/image/b5/11/b5344de85923a2ba8bea60283b491711.png?wh=1336x650)
