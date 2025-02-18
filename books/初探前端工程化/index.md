
---
title: 初探前端工程化
---

## 简介
将工程化和前端开发结合，让开发事半功倍

## 说明
## 作者介绍

![作者简介.jpg](https://p9-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/b7bcf5bdd390428ca200c93ae50072ab~tplv-k3u1fbpfcp-watermark.image?)

**sunshine小小倩**，某一线互联网公司**资深前端开发工程师**。平时在工作中除了业务之外，还从事和前端基础建设相关的工作内容，包括团队 SOP 制定、内部组件库的搭建和维护，以及其他为开发提效的工作。同时，也有一些前端性能提升等工程化的实践。

平时热衷于将自己的经验和踩过的坑跟大家分享，希望能给大家带来帮助。

## 小册介绍

![课程介绍.jpg](https://p1-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/18c4c96d344d4e6ab39957c015b2cec6~tplv-k3u1fbpfcp-watermark.image?)

现在的前端开发已经和 5 年前的前端开发有着截然不同的要求。在 5 年前我刚毕业找第一份工作的时候就问了我一个问题：“页面上有一个 button，你能把上面的文案给改了吗？” 相信 5 年后的今天，你只会修改一个 button 的文案是找不到工作的。时至今日，大家在找工作的时候基础问题都是：“Vue 实现双向绑定的原理是什么？Webpack 是怎么进行打包的？plugin 和 loader 的区别是什么？……”

前端开发最开始只是嵌入在模板引擎中对页面样式进行修改再加上一些简单的 DOM 操作，后来慢慢发展为可以处理复杂交互和业务逻辑。特别是随着 Ajax、Node 等新技术的发展，前端开发也逐渐具备了开发中大型业务的能力，这**无疑标志着前端已经步入工程化的阶段**。

这也意味着对我们的要求已经不再是“前端开发”，而是 “**前端工程师**”，`时代要求我们要有工程化的思维和工程化解决问题的能力`。

试想一下，某一天一个线上问题反馈说有的用户出现了白屏，你一通查找，结果发现是一个最新的语法在旧的浏览器上不支持。但是明明你的项目中用了 Babel 呀！打开编辑器，对着 `babel.config.js` 文件看了半天也没看出来个所以然来。于是你又打开 Google 搜索“怎么配置 Babel？”，会搜索到要安装一大堆 npm 包，配置 transform-runtime、babel-polyfill……按照第一篇文章配置之后，发现不生效，又换一篇文章，接着更改配置。终于，在快则 2 个小时，慢则一天的尝试之后，终于解决白屏问题了！此时，虽然你也不知道是改动的哪一行代码生效了，也不知道为什么要这么配置，但是知道要赶紧按下保存按钮，生怕修改了配置又出问题！并且祈祷下次千万不要有类似的问题报过来了！！ 然后又匆匆忙忙重新回到项目中赶工期，至于出问题的原因，下次一定……下次一定……

上面这个场景你是不是很熟悉？估计也戳到了很多技术人的痛处。这可能就是我们某些技术人开发的日常，被繁琐的 webpack 或者其他的 babel 、ts 的配置文件搞得一头雾水。总结来说，就是：

- 不知道怎么做技术选型，盲目从众跟风；
- 不知道如何做好依赖管理和公共库管理；
- 对项目安装的依赖不清楚其目的，别人有我也要有\(〃＞皿＜\)；
- 项目的基础配置基本靠 copy；
- 项目配置出了问题基本靠 Google 和盲试，要不就是重启大法；
- ……

以上的种种现象说明：`你前端工程化的知识欠缺`。

那么本小册将着重就现代前端开发，来详细介绍前端工程化的相关内容，并且带领大家`用专业知识来解决前端工程问题`，包括如何进行模块化、如何设计组件、如何提高代码的复用性、如何提升打包效率、如何做性能优化等。毕竟，现如今，只是会 HTML、CSS、JS 写写静态页面的时代已经过去了。

本小册主要是从开发、构建和部署这三大阶段来构思的，整体的思维导图可参考如下：

![](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/dca9f495c580468b97a3f3271999ba33~tplv-k3u1fbpfcp-zoom-1.image)

## 你会学到什么？

期望大家学习完本小册之后，能够有以下收获：

- 夯实基础，构建前端工程化领域相关知识体系；
- 用工程化的思维助力学习和工作，提升开发效率；
- 学会系统化制定前端基础建设的解决方案；
- 突破“会用 API”，从本质出发，剖析问题的底层原理。

## 适宜人群

本小册适合工作 1～3 年的初级前端工程师。比如，存在以下这些“症状”：

- 对前端工程化知识欠缺，需要查漏补缺；
- 平时大部分时间在开发业务代码，想要从千篇一律的业务需求中抽身出来，提升自己；
- 想要自己从 0 到 1 搭建应用的基础建设、制定系统化解决方案。

## 购买须知

1.  本小册为图文形式内容服务，共计 18 节；
2.  全部文章已更新完成；
3.  购买用户可享有小册永久的阅读权限；
4.  购买用户可进入小册微信群，与作者互动；
5.  掘金小册为虚拟内容服务，一经购买成功概不退款；
6.  掘金小册版权归北京北比信息技术有限公司所有，任何机构、媒体、网站或个人未经本网协议授权不得转载、链接、转贴或以其他方式复制发布/发表，违者将依法追究责任；
7.  在掘金小册阅读过程中，如有任何问题，请邮件联系 <xiaoce@xitu.io>

## 章节
- [开篇词：什么是前端工程？](./开篇词-什么是前端工程？.md)
- [如何从 0 到 1 搭建一个现代前端项目？](<./如何从 0 到 1 搭建一个现代前端项目？.md>)
- [脚手架：提升团队开发利器](./脚手架-提升团队开发利器.md)
- [探索 npm 安装机制](<./探索 npm 安装机制.md>)
- [模块化：分治思想在前端的应用](./模块化-分治思想在前端的应用.md)
- [组件化：为前端开发降本提效](./组件化-为前端开发降本提效.md)
- [团队协作规范（一）：命名规范、UI 设计规范](<./团队协作规范（一）-命名规范、UI 设计规范.md>)
- [团队协作规范（二）：项目结构、workflow、git commit](<./团队协作规范（二）-项目结构、workflow、git commit.md>)
- [常见构建工具及其对比](./常见构建工具及其对比.md)
- [Polyfill 垫片思想在前端的应用](<./Polyfill 垫片思想在前端的应用.md>)
- [下一代 JS 编译器：Babel](<./下一代 JS 编译器-Babel.md>)
- [在 Babel 中使用 Polyfill](<./在 Babel 中使用 Polyfill.md>)
- [优化 webpack 配置（一）：提升开发体验](<./优化 webpack 配置（一）-提升开发体验.md>)
- [优化 webpack 配置（二）：提升构建产物质量](<./优化 webpack 配置（二）-提升构建产物质量.md>)
- [下一代构建方案：no-bundle 构建](<./下一代构建方案-no-bundle 构建.md>)
- [软件开发“最后一公里”：持续集成和持续部署](./软件开发“最后一公里”-持续集成和持续部署.md)
- [容器化部署方案：Docker](<./容器化部署方案-Docker .md>)
- [结束语：未来展望](./结束语-未来展望.md)

    