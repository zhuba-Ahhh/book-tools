
---
title: 前端性能优化原理与实践
---

## 简介
毫秒必争！深入理解前端性能原理，将晦涩的知识转化为可爱的生产力，建立你自己的优化技能索引目录

## 说明
## 小册介绍

![](https://p1-jj.byteimg.com/tos-cn-i-t2oaga2asx/gold-user-assets/2018/10/23/166a0aede20ef0d4~tplv-t2oaga2asx-image.image)

在当下迭代飞快的互联网环境下，性能优劣至关重要，差的性能足以摧毁一个好的网站。

具体到 Web 站点的性能优化，其实后台优化的技术已经比较成熟——比如数据库的优化、后台代码的优化等等。成熟到什么程度呢？很多 Web 网页，真正花费在 Web 服务器到终端用户的时间其实往往不超过整个响应时间的一两成。

相比之下，工程师们对前端性能优化的研究和重视度还远远不够。

就国内的情况来看，许多站点并不关注前端的性能优化，这方面的研究也相对较少。事实上前端的优化空间非常大，谁能把握住这巨大的优化空间，谁就可以为自己的互联网产品争得用户流量的先机。

大家能够发现自己手上的淘宝、京东等页面越来越快，到大厂面试时性能优化也成了一个绕不过去的弯——前端性能优化终于到了手握一个应用体验质量的生杀大权的时代了！单单掌握 React 或者 Vue 以应对基本的业务开发已经不那么 OK 了。作为前端工程师，性能优化已经进化为了我们的必修课之一。

笔者希望借这本小册，尽可能降低一些大家学习性能优化的成本。

一方面，为没有接触过性能优化的新同学建立起一个正确的前端性能优化的“世界观”，从而使性能优化这件事情有迹可循。另一方面，为在职的工程师们提供一线团队已经实践过的“方法论”，形成一个性能优化思路索引表。

本小册将从网络层面和渲染层面两个大的维度来逐个点亮前端性能优化的技能树。

整个的知识图谱，用思维导图展示如下：

![](https://p1-jj.byteimg.com/tos-cn-i-t2oaga2asx/gold-user-assets/2018/10/23/1669f529d17dcea2~tplv-t2oaga2asx-image.image)

任何技术的掌握，都离不开一定比例的理论基础和实际操作的支撑。具体到前端性能优化这件事情上，笔者认为是 20\% 的理论，加上 80\% 的实践，甚至很多理论本身也都是我们在具体的业务场景中实践出来的。为了强调这一点，读者在阅读小册过程中会不时接收到“提醒”。笔者希望大家阅读本小册时，能够读到一些“书本之外的东西”。

学习性能优化，时不我待！

## 作者介绍

![](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/b44b81562c444d9e927bf3d1246a6228~tplv-k3u1fbpfcp-zoom-1.image) 修言，一线电商集团前端工程师。历任创业团队高级工程师、滴滴出行前端工程师。

始终战斗在前端性能优化的第一线，拥有丰富的研发经验、面试经验和性能死磕经验。

## 你会学到什么？

学原理，学实践，学会学习。  
建立起你自己的前端性能优化知识版图，搞定面试、优化业务。

你将学到的技术知识点：

- 前端性能优化的整体思路与思维方法
- 浏览器背后的运行机制解析
- 理解 DOM 特性及其优化思路
- 深入了解各种图片文件的特性，学会进行图片选型
- 缓存、本地存储等页面存储方案的原理与应用场景
- 服务端渲染相关知识
- webpack 性能调优方案
- 性能监测方案与应用示例
- 搞定面试题：手把手教你写 Lazy-Load、Throttle、Debounce
- 必要的原理知识补充：Gzip、CDN 等

## 适宜人群

- 具备基本的 JavaScript、CSS 知识，对 webpack 等构建工具有所了解。

- 对前端性能优化感兴趣，但没有过深入了解和实践的同学。

## 名人推荐

![](https://p1-jj.byteimg.com/tos-cn-i-t2oaga2asx/gold-user-assets/2018/10/23/166a0ac1c3d67b6d~tplv-t2oaga2asx-image.image)

![](https://p1-jj.byteimg.com/tos-cn-i-t2oaga2asx/gold-user-assets/2018/10/23/166a0ac64aa5964c~tplv-t2oaga2asx-image.image)

## 购买须知

1.  本小册为图文形式内容服务，共计 15 节，上线时间为 2018 年 10 月 24 日；
2.  购买用户可享有小册永久的阅读权限；
3.  购买用户可进入小册微信群，与作者互动；
4.  掘金小册为虚拟内容服务，一经购买成功概不退款；
5.  掘金小册版权归北京北比信息技术有限公司所有，任何机构、媒体、网站或个人未经本网协议授权不得转载、链接、转贴或以其他方式复制发布/发表，违者将依法追究责任；
6.  在掘金小册阅读过程中，如有任何问题，请邮件联系 <xiaoce@xitu.io>。

## 章节
- [开篇：知识体系与小册格局](./开篇-知识体系与小册格局.md)
- [网络篇 1：webpack 性能调优与 Gzip 原理](<./网络篇 1-webpack 性能调优与 Gzip 原理.md>)
- [网络篇 2：图片优化——质量与性能的博弈](<./网络篇 2-图片优化——质量与性能的博弈.md>)
- [存储篇 1：浏览器缓存机制介绍与缓存策略剖析](<./存储篇 1-浏览器缓存机制介绍与缓存策略剖析.md>)
- [存储篇 2：本地存储——从 Cookie 到 Web Storage、IndexedDB](<./存储篇 2-本地存储——从 Cookie 到 Web Storage、IndexedDB.md>)
- [彩蛋篇：CDN 的缓存与回源机制解析](<./彩蛋篇-CDN 的缓存与回源机制解析.md>)
- [渲染篇 1：服务端渲染的探索与实践](<./渲染篇 1-服务端渲染的探索与实践.md>)
- [渲染篇 2：知己知彼——解锁浏览器背后的运行机制](<./渲染篇 2-知己知彼——解锁浏览器背后的运行机制.md>)
- [渲染篇 3：对症下药——DOM 优化原理与基本实践](<./渲染篇 3-对症下药——DOM 优化原理与基本实践.md>)
- [渲染篇 4：千方百计——Event Loop 与异步更新策略](<./渲染篇 4-千方百计——Event Loop 与异步更新策略.md>)
- [渲染篇 5：最后一击——回流（Reflow）与重绘（Repaint）](<./渲染篇 5-最后一击——回流（Reflow）与重绘（Repaint）.md>)
- [应用篇 1：优化首屏体验——Lazy-Load 初探](<./应用篇 1-优化首屏体验——Lazy-Load 初探.md>)
- [应用篇 2：事件的节流（throttle）与防抖（debounce）](<./应用篇 2-事件的节流（throttle）与防抖（debounce）.md>)
- [性能监测篇：Performance、LightHouse 与性能 API](<./性能监测篇-Performance、LightHouse 与性能 API.md>)
- [前方的路：希望以此为你的起点](./前方的路-希望以此为你的起点.md)

    