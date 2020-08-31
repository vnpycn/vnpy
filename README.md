# vnpy-pro



 ![VNPYlogo](http://www.vnpy.cn/comm/assets/uploads/files/1596162847252-48bb2191-376d-42d3-85d0-4e8556587c6f-%E5%9B%BE%E7%89%87.png)
 

 ![Image text](https://pic4.zhimg.com/v2-1fcfaa8fa9f84886bee287fbd1a0414d_1440w.jpg?source=172ae18b)
  
  
VNPY官网： 
http://www.vnpy.cn

入门看这篇 （VNPY知乎官方公众号）：
https://zhuanlan.zhihu.com/p/166244874

VNPY专利技术保护方案（VNPY知乎官方公众号）：
https://zhuanlan.zhihu.com/p/171997958



VNPY扎根于国内合规期货市场和A股市场，为金融机构和量化爱好者提供全系列的量化产品线， 包含了历史行情数据、实时行情数据、仿真回测、商业化软件（资管系统、跟单软件）。


VNPY仿真回测系统解决了第三方回测框架各自一套费标准方法的问题，通过对原生API进行仿真来实现回测，这样做的好处是可以提供和原生API一致的方法，不再依赖于平台，所以VNPY仿真回测系统支持市场上绝大多数的CTP框架。

VNPY仿真回测目前主要提供了基于CTP接口（支持商品期货、股指期货、商品期权、股指期权）的仿真。

 如果要快速理解VNPY仿真柜台做了什么，可以看下面2张图，即原生API典型C++策略和通过VNPY仿真柜台实现回测的架构对比

 ![VNPYlogo](http://www.vnpy.cn/img/d1.gif)
 
 ![VNPYlogo](http://www.vnpy.cn/img/d2.gif)

无论是你自己开发的CTP系统还是CTP框架，甚至是快期V2交易客户端，都可以通过替换dll方式接入VNPY仿真柜台柜台。

VNPY仿真回测系统在现有3类回测方案基础上开创性的提出了第4类回测，并提供了VNPY仿真回测柜台，本产品受国家专利法保护，但可以免费下载和使用。

下面列举现在市场上包括VNPY仿真柜台回测系统在内的四类回测架构：

1.在线回测，这类是基于网站的回测，使用编程语言以Python,javascript为主，可以通过在网站提交代码脚本，在服务商的服务器上进行回测，由此可见这类回测的CPU硬件资源是极其有限的，很难实现基于TICK的高精度回测。而且最为关键的是，代码不是本地运行的，而是依赖第三方平台的方法，而且策略本身没有保密性可言；

2.商业软件实现回测，这里软件开发策略比较容易，也比较完善，但是缺点也很明显，有些策略无法在该平台实现，而且自主设计功能非常有限，比较适合开发能力一般的交易者和对程序化要求较低又愿意付费使用的交易者。

3.各种基于原生API的回测框架，一般提供了第三方方法，而不是原生方法，所以这类回测很难移植到其他框架和平台运行。

4.VNPY开创的仿真回测柜台，主要针对又较强能力的开发者，如果开发者已经基于原生API完成了策列开户，转至VNPY仿真柜台实现回测非常容易，只需2分钟即可将实盘程序化交易代码转为回测程序，无需修改原有实盘策列代码。因为他是对原生API仿真的技术，不采用第三方方法，所以决定了VNPY仿真柜台所采用的基础支持市面上所有基于此api的所有框架。



VNPY仿真回测这项底层仿真回测技术是和编程语言无关的，并且没有第3方平台提供的方法，可以在不修改原有代码的前提下实现回测。

VNPY仿真回测支持各种自编CTP程序，例如C++、Python、JAVA、C#等，同时还支持各种编程语言框架和自编程序。几乎是无所不兼容，这样的产品避免了CTP策略开发者过于依赖平台的窘境。

大多数基于K线的回测都会丢失不少细节的，会产生较大的回测误差，会误导策略开发者。

此外，由于VNPY仿真回测是基于TICK的回测，比大多数第三方软件回测精度高2个数量级以上，实现更精细化的回测。

可以真正帮助策略开发者掉入量化交易回测陷阱。

VNY的优势远远大于第三方期货量化软件回测，可以真正避免了和真实盘口不一致的情况，几乎100%还原了真实的价格变化，是真正面向职业开发者的好产品。

很多量化交易软件回测曲线是这样的

![Image text](http://www.vnpy.cn/comm/assets/uploads/files/1598886338836-000f9971-86c0-4ab0-9619-85ab688606b2-%E5%9B%BE%E7%89%87.png)


而VNPY仿真回测柜台资金曲线是这样的

 ![Image text](http://www.vnpy.cn/comm/assets/uploads/files/1598886349349-bc94ac89-81bd-40af-9998-ce4149b80f07-%E5%9B%BE%E7%89%87.png)

在采用VNPY仿真回测资金曲线和实盘资金曲线分时图取样资金曲线的比较，几乎达到了99.99%的一致。

VNPY仿真回测系统提供了基础免费版本，对所有人免费。

VNPY仿真回测柜台在VNPY开源框架基础以外，真正实现了和平台无关的基于TICK级的精细化回测


VNPY仿真柜台官网是
VNPY承诺只做国内合规市场的服务
http://www.vnpy.cn
而域名后缀为com的那个网站是做数字货币的非合规市场的外援网站，并非VNPY官网。

目前VNPY按照国家的法律法律，对VNPY仿真柜台技术做了专利申请保护，现在已经积累了不少私募基金的客户用这个产品。

而VNPY的数据服务是基于网盘提供的，以后可能会升级为付费客户端同步下载数据的服务，这样可以更好的为大家实现仿真回测数据的的下载。

VNPY仿真柜台支持股指期货仿真回测，支持商品期货仿真回测，可以将VNPY仿真柜台视为本地SIMNOW+快速回放TICK数据

无论您之前是CTP开发的策略，都可以过渡到VNPY仿真柜台来做回测。
VNPY仿真柜台支持多种编程语言，开创了第4类回测。

VNPY仿真柜台的用法快速入门可以参考这篇文章
《VNPY CTP 仿真柜台怎么用来实现CTP 程序TICK级回测》
http://www.vnpy.cn/comm/topic/3401/

VNPY的专利技术可以在VNPY知乎官方专栏查看

https://www.zhihu.com/org/vnpy/posts

基于VNPY仿真回测系统受到了VNPY老用户的欢迎和CTP开发者的欢迎，还包括了私募基金以及个人CTP开发者。

VNPY官方计划在2021年推出VNPY仿真柜台高级版本，高级版本计划提供基于多合约的同步回测，以及套利合约回测，加上批处理回测功能，可以指定参数组合，用多个进程副本来实现回测，最后汇总回测结果，给出清晰图形化展示。

由于VNPY开创的第四类仿真回测优点极其明显，在未来，一定会有前三类回测用户逐渐转向VNPY开创的第四类仿真回测柜台系统上来。




VNPY是一套基于Python的开源量化交易系统开发框架， 在开源社区6年持续不断的贡献下一步步成长为全功能量化交易平台，目前国内外金融机构用户已经超过500家，包括：私募基金、证券自营和资管、期货资管和子公司、高校研究机构、自营交易公司、交易所等。

托管是指数据中心内属于证券交易所的专用空间。它用于获得执行订单的速度（以纳秒为单位），尽可能接近股票交易所的交易引擎。
基于VNPY数据采集工具采集的TICK数据

分7个目录2017.11~2018.11期货全品种TICK数据解压后100Gb（DataCollect格式）百度网盘下载
网盘下载的数据 CSV数据文件字段顺序：
localtime (本机写入TICK的时间),
InstrumentID (合约名),
TradingDay (交易日),
ActionDay (业务日期),
UpdateTime （时间）,
UpdateMillisec（时间毫秒）,
LastPrice （最新价）,
Volume（成交量） ,
HighestPrice （最高价）,
LowestPrice（最低价） ,
OpenPrice（开盘价） ,
ClosePrice（收盘价）,
AveragePrice（均价）,
AskPrice1（申卖价一）,
AskVolume1（申卖量一）,
BidPrice1（申买价一）,
BidVolume1（申买量一）,
UpperLimitPrice（涨停板价）
LowerLimitPrice（跌停板价）
OpenInterest（持仓量）,
Turnover（成交金额）,
PreClosePrice (昨收盘),
PreOpenInterest (昨持仓),
PreSettlementPrice (上次结算价)

 
专利说明

 ![Image text](https://pic3.zhimg.com/v2-424952281b14af2b4f458ccd2792b6aa_1440w.jpg?source=172ae18b)

 ![Image text](https://pic2.zhimg.com/80/v2-7ba2f6fb5a04a2c6b9d99061bb0bfeba_720w.jpg)

 ![Image text](https://pic4.zhimg.com/80/v2-2eb2842578eddbf7e7f37849c4c645bc_720w.jpg)
 
 ![Image text](https://pic1.zhimg.com/80/v2-7dd2cd520a1e972f5cddc9342d64283d_720w.jpg)

 ![Image text](https://picb.zhimg.com/80/v2-c69b341c6a941160bfd04b2d4a287707_720w.jpg)
 
 ![Image text](https://pic1.zhimg.com/80/v2-48231226480933de7b7998519f57071a_720w.jpg)
 
 ![Image text](https://pic4.zhimg.com/80/v2-2e9930d0fbdcf75f41fa0cd7821993f2_720w.jpg)
 
 
 
VNPY Virtualapi CTP仿真回测.支持的操作系统

VNPY底层仿真回测系统支持Windows操作系统,版本要求Windows7、Windows2008及以上。

VNPY CTP仿真回测.支持语言框架

支持各种自编CTP程序和各种编程语言框架，例如C++、Python、JAVA、C#等。 支持海风、VNPY、Quicklib、PyCTP等所有框架和自编程序。 上海期货交易所只提供了 C++原生DLL，对于其他语言均是第三方封装了，只能称为CTP框架。 当然对于各种CTP 编程语言框架，例如Python框架、Java框架、C#框架等，VNPY仿真柜台的实现是一样的，因为这些语言的框架本质上还是调用C++的库文件。


项目捐赠

需强调：VNPY是免费开源项目，不接受任何捐赠！任何打着VNPY旗号索取捐赠的均为利益误导和诈骗。

