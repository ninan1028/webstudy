## 1 **vue介绍**

Vue.js（读音 /vjuː/, 类似于 view） 是一套构建用户界面的 渐进式框架。与其他重量级框架不同的是，Vue 采用自底向上增量开发的设计。Vue 的核心库只关注视图层，并且非常容易学习，非常容易与其它库或已有项目整合。另一方面，Vue 完全有能力驱动采用单文件组件和 Vue 生态系统支持的库开发的复杂单页应用。

Vue.js 的目标是通过尽可能简单的 API 实现响应的数据绑定和组合的视图组件。

### 1.1 **兼容性**
vue只能支持ie8+的浏览器.因为Vue.js使用了ie8不能模拟的es5属性(Object.defineProperty),Vue.js 支持所有兼容 ECMAScript 5 的浏览器。

## 2 **基础部分**

### 组件使用

 组件也是vue的实例

```javascript
var MyComponent = Vue.extend({
  // 选项...
});
```
### 条件渲染
2.1.0 之后添加
#### 1 v-else-if 可以链式调用
应用场景
当数据需要异步加载 在返回期间 页面可以显示空白,而不会出现切换的跳动 默认值为一个不同的值
v-if
v-else-if
默认值为空
#### 2 template
如果有多个语句 使用template来进行包裹判断

~~~~javascript
<template v-if="obj">
  <div></div>
  <p></p>
</template>
~~~~



####　3 filter

   1  Vue.filter(id,[definition])

​     注册或获取全局过滤器

   ~~~~javascript
// 注册
Vue.filter('my-filter', function (value) {
  // 返回处理后的值
})
// getter，返回已注册的过滤器
var myFilter = Vue.filter('my-filter')
   ~~~~



   2 在实例中注册  包含实例可用过滤器的哈希表

  ~~~~
new Vue({
  el:'',
  filters:{
    
  }
})
  ~~~~

