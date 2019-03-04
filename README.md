# 前端基础知识不完全记录

## 目录

1. JS 语言基础
2. 客户端及其内核原理
3. 服务端应用
4. 网络原理
5. 框架使用
6. CSS 布局基础
7. 系统工具和开发效率
8. 算法、计算机基础概念

## 1.JS 语言基础

### DOM 事件绑定的几种方式？常见的 API

### 谈谈 new 操作符

### 关于“闭包”的相关话题

### 原型、原型链、继承等相关话题

### ES6/7的新特性

    - let、const
    - 箭头函数
    - promis
    - for of

    箭头函数和普通 function 的区别？从而课衍生到 `call、apply、bind` 三者的运用问题，更或者涉及到 `this` 的使用。

### 如何理解虚拟DOM? [@zhizhu](https://www.zhihu.com/question/29504639)

- 步骤一：用JS对象模拟DOM树
- 步骤二：比较两棵虚拟DOM树的差异 → 深度优先遍历，标记并记录差异 → 差异类型 → 列表对比算法
- 步骤三：把差异应用到真正的DOM树上

关键技术：batching(批处理)、Diff算法的优化:

    batching(批处理)：将所有DOM的操作搜集打包在js对象中完成，然后一次性的递交给真实DOM（性能上只刷新一次）
    Diff算法的优化：将标准的diff算法的O(n^3)复杂度降低到了O(n)，主要得益于对新旧DOM树进行了一个深度的优先遍历，并对每个节点做唯一标记

优势：结合Node Server层来说，实现服务端与浏览器端的同构更为方便。

类比：CPU 内存(纯JS操作)和硬盘(纯DOM操作)的关系。

## 2.客户端及其内核原理

- 浏览器内核：V8引擎、
- 进程(系统层面)：一个Chome程序，或者一个标签页，操作系统分配资源的最小单位，独立
- 线程(内核层面)：渲染线程/JS引擎/事件触发/定时器触发/异步HTTP请求，程序执行的最小单位，共享

## 3. 服务端应用

- Node
- Koa
- 服务器管理(Linux、Centos等)
- Nginx 的使用

## 4. 网络原理

### 简单讲解一下 HTTP2 的多路复用？

在 HTTP/1 中，每次请求都会建立一次TCP连接，也就是我们常说的3次握手4次挥手，这在一次请求过程中占用了相当长的时间，即使开启了 Keep-Alive ，解决了多次连接的问题，但是依然有两个效率上的问题：

- 第一个：串行的文件传输。当请求a文件时，b文件只能等待，等待a连接到服务器、服务器处理文件、服务器返回文件，这三个步骤。我们假设这三步用时都是1秒，那么a文件用时为3秒，b文件传输完成用时为6秒，依此类推。（注：此项计算有一个前提条件，就是浏览器和服务器是单通道传输）
- 第二个：连接数过多。我们假设Apache设置了最大并发数为300，因为浏览器限制，浏览器发起的最大请求数为6（Chrome），也就是服务器能承载的最高并发为50，当第51个人访问时，就需要等待前面某个请求处理完成。

HTTP2采用二进制格式传输，取代了HTTP1.x的文本格式，二进制格式解析更高效。
多路复用代替了HTTP1.x的序列和阻塞机制，所有的相同域名请求都通过同一个TCP连接并发完成。在HTTP1.x中，并发多个请求需要多个TCP连接，浏览器为了控制资源会有6-8个TCP连接都限制。
HTTP2中

- 同域名下所有通信都在单个连接上完成，消除了因多个 TCP 连接而带来的延时和内存消耗。
- 单个连接上可以并行交错的请求和响应，之间互不干扰

总结：HTTP/2的多路复用就是为了解决上述的两个性能问题。
在 HTTP/2 中，有两个非常重要的概念，分别是帧（frame）和流（stream）。
帧代表着最小的数据单位，每个帧会标识出该帧属于哪个流，流也就是多个帧组成的数据流。
多路复用，就是在一个 TCP 连接中可以存在多条流。换句话说，也就是可以发送多个请求，对端可以通过帧中的标识知道属于哪个请求。通过这个技术，可以避免 HTTP 旧版本中的队头阻塞问题，极大的提高传输性能。

[More...](https://github.com/Advanced-Frontend/Daily-Interview-Question/issues/14)




## 5. 框架使用

### Vue 和 React的一些优点？
    
几个切入点：
- 数据驱动
- 数据单向流
- 虚拟DOM（可减少直接操作DOM）
- Vue 的双向绑定（原理？）
- 无缝结合 webpack 等打包工具，使得开发模式更现代，具有模块化、组件化式的。



## 6. CSS 布局基础

- BOM盒模型 [box-sizing MDN](https://developer.mozilla.org/zh-CN/docs/Web/CSS/box-sizing) 
- 纯 CSS 盒子水平垂直居中的实现方法  [Demo](https://zhuziyi1989.github.io/interview/Code/box-center.html)

### 移动端布局方案

- flex
- css-grid
- rem
- vw和vh
- 媒体查询
- 百分比

问题例子：
- 因使用了标准盒模型，盒子的 border 必然导致盒子挤出去，那么如何实现边框？
  答：用阴影或者outline来画线更加巧妙。
- 
## 7. 系统工具和开发效率

- git
- 代码编辑器
- 项目管理工具、BUG管理工具

## 8. 算法、数据结构、计算机基础等

### 有哪些基本的算法？

## 9. 综合性问题

- 自我介绍

- 介绍印象最深刻的项目

- 高并发高可用的前端架构
    
场景：诸如京东6.18和双十一这类时期，要求采用高并发、高可用的前端架构，

① 利用**缓存**
    浏览器的静态资源缓存、静态资源的 **cdn** 缓存、分布式缓存、服务端缓存。可在 `localStorage` 里所很多优化，充分利用客户端资源，可在客户端储存一些不常改变的静态数据、base64编码形式的图片。

② 升级为 http2 推送

③ **合并压缩**资源

④ 避免高频刷新页面获取数据

⑤ 设置响应头 cache-control 和 last-modified