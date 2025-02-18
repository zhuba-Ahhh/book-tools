
# 贯穿小册-Python金融数据分析实战型项目【加推篇】
---

# 贯穿小册：Python金融数据分析实战型项目

## 前言

Python作为一门高级语言是非常好用的，语法简单，通俗易懂，非常容易上手，丰富的第三方库支持使得开发速度非常快，相对于其他编程语言来说，初学者入门并不困难。

大部分从零基础开始学习Python的同学，学完了基础会开始迷茫了……接下来去怎么进阶Python呢？

Python只是一门语言工具，最终还是要将这门工具应用到一个领域中。Python的存在就是为了帮助我们快速解决实际问题，因此选择一个接地气的练手项目比什么都重要。

适合应用Python开发的项目有很多，比如WEB开发、爬虫开发、云计算、自动化运维、游戏开发、桌面软件、人工智能等等。

本小册我给大家推荐的项目是针对于股票的金融数据量化分析，更契合金融领域地称呼是股票量化交易。

## 诠释股票量化交易

我们可以用三个关键词来概括，分别是量化交易、Python 和股票。我们可以围绕着这三部分展开将原本独立的领域有机地融合而展开，如下图所示。

![](https://p1-jj.byteimg.com/tos-cn-i-t2oaga2asx/gold-user-assets/2019/5/1/16a722afb1739d1a~tplv-t2oaga2asx-image.image)

我们简单地诠释下这三个关键词的意义：

**关于量化交易**：量化交易是一种新兴的系统化的金融投资方法，它以计算机强大运算能力为基础，运用数据建模、统计学分析、程序设计等工具从历史数据中得到大概率下获利的交易策略，属于人工智能、大数据分析在金融领域的具体应用。它由金融霸主美国所先行，目前在美国的金融领域已经日趋成熟，国内虽然近几年才开始推广和流行，但是发展势头迅猛，方兴未艾。

**关于Python**：Python 自诞生以来，由于其易上手、丰富的第三方库支持等优点，在各个领域都有广泛应用。在金融行业，美国银行、美林证券的“石英”项目、摩根大通的“雅典娜”项目都战略性地使用了Python进行高效的金融程序开发和金融数据分析。可见Python已经作为一种标准编程语言应用在量化交易领域。

**关于股票**：随着时代的发展，股票投资已经成为全民最主要的理财渠道之一。A 股市场自设立至今经历过波澜壮阔的大牛市，也经历过哀鸿遍野的熊市，下图为上证指数 2003 年至 2019 年的走势图，可以看出 A 股市场至古以来牛短熊长，周期交替。

![A股市场历来牛短熊长，牛熊交替](https://p1-jj.byteimg.com/tos-cn-i-t2oaga2asx/gold-user-assets/2019/3/16/16986e1185bc2d08~tplv-t2oaga2asx-image.image)

如果你学习了Python，同时你对数据分析感兴趣，或是对金融量化交易感兴趣，或是计划开发属于自己的量化交易系统，或是准备从事金融数据分析领域，那么恭喜你，你可以把量化交易作为Python实战项目来练手。

- 一方面可以提高自己的Python实战能力，因为这个项目是一个多技术综合的项目，包括`爬虫`、`数据分析`、`可视化`、`WEB开发`、`统计概率知识`、`人工智能算法`等等。

- 另一方面可以充实自己金融量化交易的思维和方法。不可否认当今社会投资理财已经变得越来越普及和重要了。 其实，量化交易本身是可以应用在很多`投资理财领域`的，确切的说只要涉及到时间序列的价格变动，就可以应用量化交易去分析，像`银行理财产品的选择`、`房地产走势的分析`、`贵金属的价格趋势`等等，`股票投资`只是其中的一部分。

## 从程序员视角理解量化交易

接下来我们用一个简单的市场模型来介绍下量化交易的本质，这个模型是在小册 `《前置基础：从概率角度谈市场中的博弈》`一节中介绍。

假设我们投资的市场是一个具备短线交易特征的市场，可以不分昼夜的不停交易，而且还不需要交手续费。

那么我们的初始资金是1000元，每次随机的买9个股票，如果有一半以上的股票涨了的话，我们暂定赚1元，否则一半以上的股票跌了，我们就亏一元。由于我们是随机买的，那么赢钱的概率为50\%。我们邀请50个人参与1000局看下效果：

![](https://p1-jj.byteimg.com/tos-cn-i-t2oaga2asx/gold-user-assets/2019/4/1/169d8dc90105291f~tplv-t2oaga2asx-image.image)

结果还不错，亏钱的人和赚钱的人基本一半一半，符合零和游戏的特征。不过市场要经营是需要有收入的，那么就需要对交易收取手续费，为了更直观的比较出手续费对交易的影响，我们假定每次交易的手续费为0.1元。我们邀请50个人参与1000局看下效果：

![](https://p1-jj.byteimg.com/tos-cn-i-t2oaga2asx/gold-user-assets/2019/4/1/169d8dd7020d88d3~tplv-t2oaga2asx-image.image)

很不幸的是零和游戏变成了负和游戏，没有一个人是赚钱的，大家都亏钱了，当局数再增大以后的结局一定是血本无归。市场是一定会有手续费的，那我们就这么心甘情愿的当韭菜吗？

如果我们想盈利的话就只能期待每局上涨的概率大于50\%时才参与，否则不参与就不会亏钱了，并且每局赢的钱要比亏的钱多。其实这些需求映射到量化交易之中就是策略回测、仓位管理、止盈止损这些功能。那么我们改变概率这个因子，将它放大到55\%，我们邀请50个人参与1000局看下效果：

![](https://p1-jj.byteimg.com/tos-cn-i-t2oaga2asx/gold-user-assets/2019/4/1/169d8e2ddc031437~tplv-t2oaga2asx-image.image)

看来结果还不错，只要增加盈利的概率，就可以在市场中获得收益。其实股票交易和玩一个游戏、做一个项目理念上是相通的，需要章法、需要制定策略，否则就和抛硬币赌博一样的，用量化交易可以帮助我们管理好概率，更理性的去下单！因此通过量化交易管理亏盈的概率，能够更理性的将股票投资作为理财的一个手段。

也许大家会觉得以上的市场模型每次都是独立事件，概率上没有连续性。股票和期货市场的每次下注的结果是有连续性的，并不是纯随机的独立事件。事实上我们真的不能确定明天的具体价格，不过量化交易的精髓在于，它能从历史数据中得到大概率下获利的策略。

有研究称股票每天的价格变动就像醉汉行走一样不可预知，那么我们假设一名喝醉了酒的醉汉，从一个路灯下开始漫无目的地行走，每一步即可能前进也可能后退也可能拐弯。那么经过一定时间之后，这名醉汉的位置在哪里呢？

为了便于理解，我们将醉汉的移动简化为一维的移动，规定他只能在一条直线上随机前进或者后退。这个模型是在小册 `《前置基础：NumPy模拟随机漫步理论》《前置基础：Matplotlib模拟随机漫步轨迹》`两节中介绍。

绘制出醉汉从0轴开始随机游走2000步的模拟轨迹图形，如图所示：

![](https://p1-jj.byteimg.com/tos-cn-i-t2oaga2asx/gold-user-assets/2020/4/19/171905797b0db7c8~tplv-t2oaga2asx-image.image)

由于醉汉的每一步都是完全随机的，因此他最终准确的位置无法被预测出，就像每天的股票价格变动一样是不可预知的。但是，量化交易会从统计学的角度去分析问题，我们用1000次随机漫步来模拟醉汉从0轴开始1000次随机游走2000步的模拟轨迹图形，如图所示：

![](https://p1-jj.byteimg.com/tos-cn-i-t2oaga2asx/gold-user-assets/2019/6/3/16b1dc2ecb09d4c5~tplv-t2oaga2asx-image.image)

从统计学的角度来看，这名醉汉最终的位置的概率分布却是可以计算出来的。图中我们直观地观察出随机游走的发展情况，每一条淡淡的蓝线就是一次模拟，横轴为行走的步数，纵轴表示离开起始点的位置。蓝色越深，就表示醉汉在对应行走了对应的步数之后，出现在此位置的概率越大，可见随着醉汉可能出现的位置的范围不断变大，但是距离起始点越远的位置概率越小。

于是我们联想到正态分布。正态分布描述的是某件事出现不同结果的概率分布情况，它的概率密度曲线的形状是两头低，中间高，左右对称呈钟型，与我们模拟的随机漫步图很相似。

![](https://p1-jj.byteimg.com/tos-cn-i-t2oaga2asx/gold-user-assets/2019/3/17/1698b58d84ddbdc4~tplv-t2oaga2asx-image.image)

从图中的显示可知醉汉的行走轨迹在一定意义上是符合正态分布的。正态分布现象在现实中意义重大，在自然界、人类社会、心理学等领域的大量现象中都服从或者近似服从正态分布，比如人们能力的高低，身高、体重等身体的状态，学生成绩的好坏，人们的社会态度、行为表现等等。

> 数学的奇妙之处就在于，我们可以把不可预知性变为可预知。量化交易的精髓就是用数学公式来精确计算真实的概率分布，以应对不确定性。

## 如何用Python获取股票数据

既然是金融数据的分析，那么第一步获取数据很重要。目前，获取股票数据的渠道有很多，而且基本上是免费的，比如同花顺、东方财富这些行情软件，新浪财经、腾讯财经、和讯网这些门户网站。

Python也有不少免费的开源API可以获取交易行情数据，比如pandas专门处理金融数据模块pandas-datareader、tushare、baostock等。这样无需使用Python网络爬虫，可以节省不少精力。在小册 `《差异化分析常用股票交易数据接口》`一节中介绍。

这里推荐使用tushare获取股票交易数据，基本上tushare记录了股票自上市之日起所有的日交易数据，而baostock最早记录的数据是2006年，总的来说tushare是目前分析国内A股、期货等比较好用的开源接口。 目前团队推出了Tushare

Pro版本，这个版本相比于旧版本来说数据更加稳定、质量也更好了，使用的话需要先注册获取TOKEN凭证，不过旧版本仍然可以使用，只是团队不再维护数据获取的接口。

下图是使用pro.index\_daily\(\)接口获取上证综指2003年至2018年日交易数据，结合可视化方法对指数走势进行分析。可以看到股指分别在2005-2007年和2014-2015年有两波大牛市，然后又从高峰跌入谷底，目前处于下跌通道，期待下一次大牛市。

![](https://p1-jj.byteimg.com/tos-cn-i-t2oaga2asx/gold-user-assets/2020/4/19/171905b7058ece26~tplv-t2oaga2asx-image.image)

获取到大量的股票数据，可以用数据库来高效地管理。目前流行的数据库有Oracle、MySQL、MongoDB、Redis、SQLite……关于数据库的选型通常取决于性能、数据完整性以及应用方面的需求。

如果我们仅仅是用于本地的数据管理，无需多用户访问，数据容量小于2T，无需海量数据处理，关键是要求移植方便、使用简单、处理迅速的话， SQLite确实是个很不错的选择。

Python 2.5.x 以上版本默认内置SQLite3，无需单独安装和配置，直接使用就行。 建立了本地SQLite数据库，可以进一步查询和操作。比如查询股价日涨幅超过5\%的个股在19年1月至2月的分布。如下所示：

![](https://p1-jj.byteimg.com/tos-cn-i-t2oaga2asx/gold-user-assets/2020/4/19/171905bfd2e47a91~tplv-t2oaga2asx-image.image)

除了获取行情数据，我们也需要寻找宏观经济、行业、公司相关的信息，这些信息是驱动股票涨跌的因素。关于这些信息，我们可以通过爬虫的方式去各大网站和论坛获取。在小册 `《股票数据分析：爬虫方式获取行业板块数据》《股票数据分析：爬虫抓取东方财富网股吧帖子》`两节中介绍。

这里我们列出一部分信息来源：

- 政府网站：国家统计局、工业和信息化部、财政部、中国人民银行……
- 证券官方网站：上海证券交易所、深圳证券交易所、证监会、证券业协会……
- 信息披露网站：东方财富网、巨潮资讯网……
- 股票论坛：点金投资家园、股天下、MACD股票论坛、创幻论坛、和讯股吧、东方财富股吧

## 量化交易的Python库有哪些

量化交易的第三方Python库是为了实现量化交易的需求而封装的，以下是量化交易初级入门所设计到的一些功能和基础工具。

我们对这些第三方库的应用场景简单地做个介绍，后续大家在需要使用的时候，可以有侧重地去查找相关资料：

- Matplotlib——应用于可视化绘图

- Bokeh——应用于Web交互式可视化绘图

- WxPython——应用于创建本地GUI界

- Urllib3——应用于HTTP客户端网络请求

- Numpy——应用于科学计算

- Pandas——应用于金融数据分析

- Statsmodels——应用于统计模型和分析

- TA-Lib——应用于金融技术指标计算

- Tushare——应用于财经数据的获取

- Django——应用于Web框架的搭建

- scrapy——应用于爬虫框架的搭建

初学者入门的话可以先开发一个股票行情界面：`《股票数据可视化：自定义Matplotlib版股票行情界面》`一节中介绍。

![](https://p1-jj.byteimg.com/tos-cn-i-t2oaga2asx/gold-user-assets/2019/4/1/169d88c2465b0336~tplv-t2oaga2asx-image.image)

关于这幅界面的实现，我们简单地介绍下方法，主要包括：

- 使用TuShare、Pandas库来获取金融数据；

- 使用Pandas、Numpy库对原始数据进行规整化的处理；

- 使用Talib库从原始数据计算出均线、MACD、KDJ指标；

- 使用Matplotlib库实现股票技术指标的可视化图形；

当然了，我们也可以使用pyechart绘制出更炫的动态行情界面：

![](https://p1-jj.byteimg.com/tos-cn-i-t2oaga2asx/gold-user-assets/2019/3/30/169cdfc2678cc758~tplv-t2oaga2asx-image.image)

再比如可以使用Urllib3、scrapy库爬取东方财富网的财经数据，作为量化分析的基础数据。

![](https://p1-jj.byteimg.com/tos-cn-i-t2oaga2asx/gold-user-assets/2020/4/19/17190608fe54d6a8~tplv-t2oaga2asx-image.image)

![](https://p1-jj.byteimg.com/tos-cn-i-t2oaga2asx/gold-user-assets/2020/4/19/1719060d6af92823~tplv-t2oaga2asx-image.image)

## 概述量化交易基本过程

最后我们概述下量化交易的基本过程。当然实际上这个过程并没有以下流程图显示的那么简单，这里只是让大家有个整体的概念。

![](https://p1-jj.byteimg.com/tos-cn-i-t2oaga2asx/gold-user-assets/2019/3/17/1698ae6ef334a460~tplv-t2oaga2asx-image.image)

首先是把历史行情、基本面信息、新闻资讯等数据进行初步清洗和处理，而后输入到量化模型中。

量化模型包括了数学建模、编程设计等工具所形成的交易策略，通过分析这些数据最终产生出交易的信号，比如买什么股、什么时候买、买多少、什么时候卖等信息。 我们可以通过远程提醒方式完成下单。

![](https://p1-jj.byteimg.com/tos-cn-i-t2oaga2asx/gold-user-assets/2020/4/19/17191a0777cf3c3a~tplv-t2oaga2asx-image.image)

![](https://p1-jj.byteimg.com/tos-cn-i-t2oaga2asx/gold-user-assets/2020/4/19/17191a09060d0ad4~tplv-t2oaga2asx-image.image)

![](https://p1-jj.byteimg.com/tos-cn-i-t2oaga2asx/gold-user-assets/2020/5/25/1724adb6743c305e~tplv-t2oaga2asx-image.image)

![](https://p1-jj.byteimg.com/tos-cn-i-t2oaga2asx/gold-user-assets/2020/5/25/1724adb9ee54ad49~tplv-t2oaga2asx-image.image)

![](https://p1-jj.byteimg.com/tos-cn-i-t2oaga2asx/gold-user-assets/2020/7/25/17383642614cc56a~tplv-t2oaga2asx-image.image)

分解量化模型可以看到模型是通过各种策略来实现的，常见的策略有均线策略、Alpha策略、布林带策略、海龟策略、动量策略等等，也包括自主开发的策略，不过要良心的声明下凡事公开的、用的人多的策略，基本也就不赚钱了，当然并不影响我们学习这些策略从中借鉴其中的精髓，站在巨人的肩膀上看问题。

课程中涉及以下这些经典的策略。

#### 择时策略——海龟交易N日突破

![](https://p1-jj.byteimg.com/tos-cn-i-t2oaga2asx/gold-user-assets/2019/4/11/16a0a32aea2a4d23~tplv-t2oaga2asx-image.image)

#### 选股策略——线性回归

![](https://p1-jj.byteimg.com/tos-cn-i-t2oaga2asx/gold-user-assets/2019/4/8/169fd421d5f4bd7c~tplv-t2oaga2asx-image.image)

#### 选股策略——欧奈尔RPS选强势股

![](https://p1-jj.byteimg.com/tos-cn-i-t2oaga2asx/gold-user-assets/2020/3/3/170a0b894aa3fcab~tplv-t2oaga2asx-image.image)

![](https://p1-jj.byteimg.com/tos-cn-i-t2oaga2asx/gold-user-assets/2020/3/3/170a0b9601b89c6a~tplv-t2oaga2asx-image.image)

#### 参数优化策略——蒙特卡洛

![](https://p1-jj.byteimg.com/tos-cn-i-t2oaga2asx/gold-user-assets/2019/4/21/16a3fd8d8eff71df~tplv-t2oaga2asx-image.image)

策略层再往下分解则是我们熟悉的Pyhon、Pandas、Matplotlib、Numpy、统计学、数学模型这些基础工具。

关于上图的回测阶段，我们要提一下。当我们制定了一个交易策略后，我们并不能立即将该策略应用于实盘交易之中，原因很简单，我们无法评价该策略的具体效果如何。对此，我们需要将策略基于一段历史股票数据进行模拟的买入和卖出，以验证交易策略的可行性，我们称这个环节为“回测阶段”。`《股票交易策略：收益与风险维度度量策略效果》`一节中介绍。

在回测阶段，策略的收益和风险是度量策略效果非常关键的两个指标，比如我们将N日突破择时策略应用在华胜天成股票上时，可以通过直观的图形分析来了解下策略的执行效果。如下所示：

#### 自定义的回测框架

![](https://p1-jj.byteimg.com/tos-cn-i-t2oaga2asx/gold-user-assets/2019/4/13/16a157ce4c0f945a~tplv-t2oaga2asx-image.image)

#### 基于聚宽的回测平台

![](https://p1-jj.byteimg.com/tos-cn-i-t2oaga2asx/gold-user-assets/2020/5/30/17263759a74e3065~tplv-t2oaga2asx-image.image)

#### 基于BackTrader回测框架

![](https://p1-jj.byteimg.com/tos-cn-i-t2oaga2asx/gold-user-assets/2020/5/11/1720301be90896e3~tplv-t2oaga2asx-image.image)

## 总结

希望本小册的实战项目能够给大家带来一些启发，也希望大家能过找到自己最钟意的项目，从中提升自己Python开发水平。

大家如果想对涉及到的知识点进行更全面、更体系的从0-1方式的介绍，这里推荐给大家我的书籍`《Python股票量化交易从入门到实践》`！天猫、京东、当当全面开售！

![](https://p1-jj.byteimg.com/tos-cn-i-t2oaga2asx/gold-user-assets/2020/6/14/172b02acf22e150c~tplv-t2oaga2asx-image.image)

**同时也欢迎大家关注我的微信公众号【元宵大师带你用Python量化交易】了解更多Python量化交易相关内容**

![](https://p1-jj.byteimg.com/tos-cn-i-t2oaga2asx/gold-user-assets/2020/4/4/1714436c26f09bf3~tplv-t2oaga2asx-image.image)

> 本小册还在持续加推中，敬请期待！！！目前已经加推27节了【上线20节-目前47节】，还会一直加推......！

![](https://p1-jj.byteimg.com/tos-cn-i-t2oaga2asx/gold-user-assets/2020/5/30/17263751f8423bda~tplv-t2oaga2asx-image.image)

**同时我们也在【知识星球】平台开设了Python、AI、数据处理、爬虫、数据库、股票策略、金融知识、GUI开发等各种量化交易相关的衍生内容的交流。**

**欢迎大家在微信公众号中点击【联系我们】加入！**
    