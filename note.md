# Vue

## 简介

- Vue是一套渐进式框架，其基础是组件，属于MVVM(Model-View-ViewModel)框架

- 渐进式

参考：[尤雨溪-前端渐进式开发](https://mp.weixin.qq.com/s?__biz=MjM5MDE0Mjc4MA%3D%3D&mid=2650994529&idx=1&sn=953bf1d92cc2a7b278d0761d3e433803&chksm=bdbf0f328ac886245652735e4dfa1b39b1357b9f36ccf1b337714ac81810f8441d189ce89615)

- 框架

框架具有一定的规范性 需按照规定的方式书写代码，在开发者规定的地方书写代码，框架会主动调用这些代码

- 两个核心特点

1. 响应式的数据绑定<br>
<br>视图与数据会类似于绑定式操作，框架会以最小的代价更新变化过的数据所对应的视图。

2. 可组合的组件<br>
<br>组件系统是Vue的另一个重要概念，因为它是一种抽象，允许使用小型独立和通常可服用的组件

### 第一日学习

- Vue中的data以及methods

1. data：其中放入Vue的属性
2. methods：其中放入Vue的方法

data和methods中的所有属性都是挂载在Vue的实例化对象中

```
<div v-if="true">显示</div>
<div v-if="false">不显示</div>
```
v-if可以控制元素显示与否，但是是通过移除添加DOM元素实现，所以如果控制显示隐藏的元素较多 不建议使用

```
<div v-if="true">显示</div>
<div v-else if="2">显示另一个</div>
<div v-else>显示另一个</div>
```
v-if有类似于原生js的if判断，同时具有if、else、和else if三种判断，像if判断中一样，只要先前语句成立，则不向下继续执行。

```
<div v-for="item in list">循环列表</div>
```
v-for可以将列表循环，可根据列表中的项数循环生成相应数量的DOM元素，item就为list中的每一项

```
<div v-for="val,key in obj">循环列表</div>
```
v-for还可以循环对象，val存储对应键值，key为对应键名

```
<div v-bind:class="{className: true||false}">循环列表</div>
```
在行间动态的绑定数据
<br>语法：v-bind:行间自动以属性名='表达式'

```
<div v-on:click="function">循环列表</div>
```
v-on是用来触发对应事件，on:后面写对应事件名（click、mouseover....），对应事件触发后，执行后面写的函数，如果函数代码较少，可以直接写在后面，否则写一个具名函数放在后面，具名函数可以传参，参数顺序与对应传参顺序一样，如果需要事件对象，则传入$event参数，此参数就为事件对象。