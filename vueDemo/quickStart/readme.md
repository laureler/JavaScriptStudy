# vue quickStart 快速入门
## vue.js 介绍
------------------
> vue.js是一套构建用户界面的渐进式框架。与其他重量级框架不同的是，Vue 采用自底向上增量开发的设计(//todo向上增量)<br/>    
Vue 的核心库只关注视图层，它不仅易于上手，还便于与第三方库或既有项目整合。 <br>
当与单文件组件和 Vue 生态系统支持的库结合使用时，Vue 也完全能够为复杂的单页应用程序提供驱动。

**Vue.js 不支持 IE8 及其以下版本，因为 Vue.js 使用了 IE8 不能模拟的 ECMAScript 5 特性。Vue.js 支持所有兼容 ECMAScript 5 的浏览器。**
## vue开始使用
    1. <script src="https://unpkg.com/vue"></script>
    2. node.js 使用npm来安装vue并且引入(//todo查看node.js教程)
### 使用
    1. 必须要先有vue.js的引入。无论是什么方式
```ecmascript 6
    var data = {
      message:'yourData',
    }
   var vm = new Vue({
      el:'yourSelector',
      data:data
    })
    // vue中就会存在一个data:{message:'yourData'}的对象实例
```
```html
<span id="app">{{message}}</span>
```
### 属性讲解
vue中声明的vm实例就是一个总的全局的对象，类似于jquery中的$<br/>
data:data其实就是把一个数据的 **引用** 给加到了实例中
```ecmascript 6
    vm.message === data.message
    //修改了data中的定义 vm中的数据也会跟着改变
    vm.message = 'test'
    console.log(data.message); //test
    //反之一样
    data.message = 'test2'
    console.log(vm.message)
```
**若一开始并没有声明对应的数据，则在添加的时候，并不会动态的修改，例如vm.b ='balabala',那么data并不会添加一个b属性**
    
    
    
    
    
    