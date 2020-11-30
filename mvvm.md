#### 1. [dom-diff解析](https://vue-js.com/learn-vue/virtualDOM/patch.html)

> Vue中的DOM-Diff算法：patch过程，了解了整个patch过程干了三件事，分别是：创建节点，删除节点，更新节点。

#### 2. vue如何实现数据驱动视图

[变化侦测篇](https://vue-js.com/learn-vue/reactive/#_1-%E5%89%8D%E8%A8%80)

* **Object的变化侦测**，通过Object.defineProperty方法实现了对object数据的可观测，流程如下：
    1. Data通过observer转换成了getter/setter的形式来追踪变化。
    2. 当外界通过Watcher读取数据时，会触发getter从而将Watcher添加到依赖中。
    3. 当数据发生了变化时，会触发setter，从而向Dep中的依赖（即Watcher）发送通知。
    4. Watcher接收到通知后，会向外界发送通知，变化通知到外界后可能会触发视图更新，也有可能触发用户的某个回调函数等。

* **Array的变化侦测**，流程如下：
    1. 对于Array型数据也在getter中进行依赖收集
    2. 创建数组方法拦截器，从而成功的将数组数据变的可观测
    3. 对数组的依赖收集及数据变化通知依赖


#### 3. vue3.0种proxy和defineProperty

[初探 Vue3.0 中的一大亮点——Proxy !](https://www.jianshu.com/p/2a8ec76e0090)

> 1. 消除之前Vue2.x中基于Object.defineProperty的实现所存在的很多限制：无法监听属性的添加和删除、数组索引和长度的变更，并可以支持Map、Set、WeakMap和WeakSet！
> 2. MDN 上是这么描述的——Proxy对象用于定义基本操作的自定义行为（如属性查找，赋值，枚举，函数调用等） 

#### 4. MVVM流程图


#### 5. vuex的mutation
