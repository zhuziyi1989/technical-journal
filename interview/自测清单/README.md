# 自测清单

<img src="https://cdn.jsdelivr.net/gh/ninishare/page@master/images/2020/11/20/hr91ZR.png" alt="png" style="zoom:50%;" />



### 第一步修改简历

首先，学习过程注重理解而不是记忆。

其次，一个知识点，通过多篇资料对比学习，反复查阅加深理解，并用自己的话进行讲解。

最后，加强语言组织的能力，有意地引导话题到自身熟悉的领域。

- 切忌简历中出现不熟悉的词汇。

- 集中注意力，制定详细规划。

- 切忌三天打鱼两天晒网，忌零散阅读，宜系统复习。
- 注重考点的理解，不要死记硬背



### html/css 基础

- BFC
- [Flex](https://zhuanlan.zhihu.com/p/25303493) [@MDN](https://developer.mozilla.org/zh-CN/docs/Web/CSS/CSS_Flexible_Box_Layout/Basic_Concepts_of_Flexbox) [flex-direction](https://css-tricks.com/wp-content/uploads/2018/10/flex-direction.svg):row/column/row-reverse/column-reverse 起始线和终止线 [justify-content](https://css-tricks.com/wp-content/uploads/2018/10/justify-content.svg)
- 盒子模型
- 动画 animation
- 常规布局（position/float + margin/translate + calc 动态计算 + flex）
- 水平/垂直居中的多种方案
- position
- z-index
- background
- 移动端 1px 问题
- viewport
- em/rem  [vh/vw](https://juejin.cn/post/6844904029898670088)
- 逻辑像素、设备像素、物理像素 dpr

### js 基础

- [闭包](https://github.com/mqyqingfeng/Blog/issues/9)
- [原型(链)](https://github.com/mqyqingfeng/Blog/issues/2)
- [继承](https://github.com/mqyqingfeng/Blog/issues/16)（继承模式）
- [作用域](https://github.com/mqyqingfeng/Blog/issues/6)
- [变量提升](https://github.com/mqyqingfeng/Blog/issues/5)
- [立即执行函数](https://segmentfault.com/a/1190000003985390)
- DOM事件和事件流
- 事件循环(宏任务和微任务、Node和浏览器的事件循环区别)
- ES6/7/8新特性
- 箭头函数和普通函数的区别
- map & set 数据结构
- 遍历 map/forEach/fliter/some/one...
- 遍历对象
- new 过程发生了什么？
- generator/yield
- Promise原理(手写Promise.all方法)
- async/await
- [聊聊this](https://github.com/mqyqingfeng/Blog/issues/7)，延伸call、apply、bind 区别、手写实现
- 前端性能优化
  - 首屏加载优化
  - 防抖和节流（手写）
  - 回流和重绘，如何避免？
- 跨域形成原因以及解决方案
- 深拷贝和浅拷贝(JSON.stringify、JSON.parse这种方案的弊端)
- ES6模块和 CommonJS 的区别
- service worker 、 web worker
- 函数式编程
- 浮点数精度（进制转换问题）

### 工具

- Webpack的实现原理
- webpack Tree shaking
- Git rebase 和 merge 的区别？
- JSBridge 的通信原理
  - JavaScript 调用 Native，主要通过注入 API 和 拦截 URL SCHEME，iframe.src

### 客户端

- 回流和重绘
- V8引擎（JS 引擎、GUI 渲染引擎、延时引擎、异步）

### 设计模式

- MVVM
- MVC
- MVP
- 重构
- 常用设计模式

### 算法

| 清单目录                                                     |
| ------------------------------------------------------------ |
| [斐波那契数列](https://leetcode-cn.com/problems/fibonacci-number/) |
| [合并二维有序数组成一维有序数组](https://leetcode-cn.com/problems/he-bing-liang-ge-pai-xu-de-lian-biao-lcof/) |
| [链表：反转链表](https://leetcode-cn.com/problems/fan-zhuan-lian-biao-lcof/) |
| [链表：链表有环](https://leetcode-cn.com/problems/linked-list-cycle/) |
| [堆栈队列：判断括号字符串是否有效](https://leetcode-cn.com/problems/valid-parenthesis-string/) |
| [返回数组中第k个最大元素](https://leetcode-cn.com/problems/kth-largest-element-in-an-array/) |
| [找出数组中和为sum的n个数](https://wizardforcel.gitbooks.io/the-art-of-programming-by-july/content/02.03.html) |
| [贪心：具有给定数值的最小字符串](https://leetcode-cn.com/problems/smallest-string-with-a-given-numeric-value/) |
| [二叉树：最大深度](https://leetcode-cn.com/problems/er-cha-shu-de-shen-du-lcof/) |
| [二叉树：层次遍历](https://leetcode-cn.com/problems/binary-tree-level-order-traversal/) |
| [剪枝：判断数独是否有效](https://leetcode-cn.com/problems/valid-sudoku/) |
| [二分查找：求解平方根](https://leetcode-cn.com/problems/sqrtx/) |
| [字典树：实现一个字典树](https://leetcode-cn.com/problems/implement-trie-prefix-tree/) |
| [爬楼梯问题](https://leetcode-cn.com/problems/climbing-stairs/) |
| [最短距离](https://leetcode-cn.com/problems/shortest-distance-to-a-character/) |
| [LRU缓存](https://leetcode-cn.com/problems/lru-cache/)       |
| [翻转二叉树](https://leetcode-cn.com/problems/invert-binary-tree/) |

### 操作系统

- 进程和线程
- 进程通信
- 进程调度策略
- 锁死
- IO 多路复用

### 网络

- 综合：从输入url到获得页面经历的
- HTTP2/3版本做了哪些改进？
- [HTTP 缓存](https://juejin.cn/post/6944891188826603528)（强缓存、协商缓存） 
  - cache-control:max-age，Expires，Pragma，Etag(hash/MD5/SHA128/SHA256)，Last-Modified(GMT) 
  - 不同http版本差异
  - ETag:W/"50b1c1d4f775c61:df3" （W/前缀代表使用弱类型验证）
- HTTPS 实现的过程
- 请求头、响应头、常见状态码
- 七层网络协议
- GET & POST...
- CSRF & XSS
- TCP/UDP
- websocket

### vue 不做重点发展

- vue响应式原理
- vue虚拟dom & diff算法
- vue3 解决了什么问题？
- vue 为什么不能检测数组和对象的变化,怎么处理(为什么通过索引操作数组不能触发响应式)
- vue-router原理
- v-model实现原理
- vue.nexttick
- computed的实现原理
- Watch的运行原理
- slot 插槽

### react

- 虚拟 DOM（对象）
- Diff 算法（key）
- Props（只读、参数） 和 State（状态）
- PropTypes(类型检查，联想typescript)
- Hooks（破解函数组件无状态化 useState，useEffect，useContext，useReducer）
- Rers
- 高阶组件(纯函数)
- 有状态组件和无状态组件
- MVVM模型
- 生命周期
- 数据绑定
- 状态管理
- 组件之间的通信 Context、Props、redux
- 组件抽象
- [redux](https://tech.meituan.com/2017/07/14/redux-design-code.html) 状态管理  action(dispatch)→reducer→store
- react-router-dom（BrowserRouter和HashRoauter） Link 
- 错误边界  发生错误，优雅降级，退回UI
- Fragments 多个组件包裹问题

- 适当地使用`shouldComponentUpdate`生命周期方法。 它避免了子组件的不必要的渲染。
- 如何在重新加载页面时保留数据 localstorage 多表单应用优化 [示意图](https://image.fundebug.com/2019-05-31-10.png)



### Node.js

| NodeJS 相关知识                                              |
| :----------------------------------------------------------- |
| [模块机制](https://juejin.cn/post/6844904030905303054) es6(静态加载 编译时执行)   common.js(动态加载 运行时执行 require缓存) |
| [require原理](http://www.ruanyifeng.com/blog/2015/05/require.html) |
| [事件循环](https://learnku.com/articles/38802)               |
| [cluster原理](https://www.cnblogs.com/dashnowords/p/10958457.html) |
| [流机制](https://www.barretlee.com/blog/2017/06/06/dive-to-nodejs-at-stream-module/) |
| [pipe原理](https://cloud.tencent.com/developer/article/1630068) |
| [守护进程](https://juejin.cn/post/6844903444839399438)       |
| [进程通信](http://www.ayqy.net/blog/nodejs进程间通信/)       |
| [异常处理](http://www.alloyteam.com/2013/12/node-js-series-exception-caught/) |

### 性能优化

- 缓存入手 localstorage 做 Nginx 做相应配置
- 资源打包压缩 webpack 设置问题，未切换到生产环境
- 静态资源的处理：图片压缩、CSS 压缩、雪碧图
- 使用字体图标、svg格式图标
- 尝试WebP图片格式
- CDN 加速，内存级或SSD硬盘
- GPU渲染着手，避免重绘、重排代码
- JS 引擎阻塞
- pm2 实现 Node 中间的多线程
- Nginx 做反向代理和缓存层

### 面试总结分享

- [面试分享：两年工作经验成功面试阿里P6总结](https://juejin.im/post/6844903928442667015#heading-36)
- [2021年字节跳动前端面试手册](https://bytedance.feishu.cn/base/app8Ok6k9qafpMkgyRbfgxeEnet?table=tblEnSV2PNAajtWE&view=vewJHSwJVd)
- 本人优缺点分析： 我觉得我有时候会过分在意别人的感受， 比方说，不愿意直接表达不同意见，因为觉得会让对方丢面子， 其实这样做很不利于快速有效地开展工作。我希望自己能够逐渐学会更加爽快， 对人对事更加直接。


