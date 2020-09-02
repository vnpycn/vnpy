# vnpy-pro

 ![VNPYlogo](http://www.vnpy.cn/comm/assets/uploads/files/1596162847252-48bb2191-376d-42d3-85d0-4e8556587c6f-%E5%9B%BE%E7%89%87.png)
 
## VNPY官网 ：
http://www.vnpy.cn

## 入门篇《VNPY CTP 仿真柜台怎么用来实现CTP 程序TICK级回测》 ：
（来自VNPY知乎官方公众号）
https://zhuanlan.zhihu.com/p/166244874 

## VNPY专利技术保护方案（VNPY知乎官方公众号）：
https://zhuanlan.zhihu.com/p/171997958

VNPY官方扎根于国内合规期货市场和A股市场，为金融机构和量化爱好者提供全系列的量化产品线， 包含了历史行情数据、实时行情数据、仿真回测、商业化软件（资管系统、跟单软件）。
其中推出的VNPY For  CTP接口仿真柜台是VNPY官方的主打产品，这款产品的设计理念是“精细化回测”，自2018年推出以来受到了广大量化交易爱好者的喜爱，尤其是职业量化交易团队和量化私募基金的青睐。

VNPY仿真回测系统在现有3类回测方案基础上开创性的提出了第4类回测，并提供了VNPY仿真回测柜台，本产品受国家专利法保护，但可以免费下载和使用。

##  量化交易从哪个市场做起
对刚开始接触量化交易的爱好者来说，关于选择哪个市场进行量化交易做起，我们给出的结论是：以上市场中，符合中国金融环境并且最适合学习量化的市场是中国国内期货市场。理由如下：

(1)符合国内金融环境，有能力就有机会在期货市场发自己的CTA相关基金产品。

(2)有了期货交易经验和资金管理经验，很容易就可以过渡到管理A股市场的相关资金或产品。

(3)期货市场和国外很多成熟市场一样是T+0制度。

(4)国内程序化支持最完善，例如上海期货交易所的CTP接口，郑州商品交易所和大连商品交易所也从推出了自己的API，这些交易所官方提供的API免费、公开、合法，并且有众多的开源框架可以使用，更不像证监会对A股程序化接口做了诸多限制而难以实施。

(5)A股市场由于行情持续时间较长，周期过大，导致容易蒙对行情而无法领悟真正的量化规律。而期货市场瞬息万变，在期货这样的市场里进行量化交易的学习更容易真正发现交易的真谛。

(6)鉴于期货市场存在主力品种投机性强、流动性好、套利机会多等特点，期货市场更适合做量化交易。

有了上述理由，VNPY仿真柜台回测系统以国内期货CTP接口进行仿真，提供基于CTP仿真得VNPY仿真回测系统版本。


 ![Image text](https://pic4.zhimg.com/v2-1fcfaa8fa9f84886bee287fbd1a0414d_1440w.jpg?source=172ae18b)
 
目前期货的量化交易环境是比较完善的，上海期货交易所推出了免费的CTP API接口多年，也是影响最大和使用最广泛的期货API接口，也使得一大批期货交易爱好者从接触CTP的那一刻起就义无反顾的开始了自己的量化交易之路。

## 从CTP小白到实盘3个步骤

（1）通过SIMNOW模拟账户开发测试，这一个阶段主要是功能测试；
（2）通过VNY仿真回测柜台做功能测试，这一个阶段主要是策略验证；
（3）实盘交易；


如果需要先开发和测试，不用实盘交易的话，可以采用上期CTP的模拟账户进行测试和开发，相关网址链接如下：
上海期货交易所SIMNOW  CTP模拟账户注册地址

http://www.simnow.com.cn/

CTP最新的原生API和说明文档也可以从这个网站下载

http://www.simnow.com.cn/static/softwareDownload.action/

模拟账户对应的客户端软件从这里下载，包含了Window API和Linux API

http://www.simnow.com.cn/static/softwareOthersDownload.action/



## CTP实盘、SINOW模拟账户、VNPY CTP仿真柜台 三者成交机制的异同

CTP同时支持期货实盘账户和simnow模拟账户，采用simnow模拟账户和期货实盘账户开发出的程序是通用的，但simnow模拟账户和实盘账户成交和结算机制还有几点不同：
（1）成交机制不同
模拟账户采用对手价成交，实盘在盘中撮合成交。
（2）模拟行情比实盘行情慢几十秒，因采用模拟行情同时采用模拟交易，所以对信号和盈亏不会产生实质影响。
（3）资金容量对滑点的影响
    模拟账户成交不需要考虑资金容量导致的滑点，实盘账户在交易时因为会影响盘口，可能会导致滑点产生。
（4）模拟行情除了和实盘一致的行情服务以外，还提供了24小时服务器进行测试，但不提供结算，适合用作CTP开发时的功能测试。
如果需要实盘账户，请去各大期货公司开户。获得几项信息即可接入CTP进行交易
	. brokeid
 . 投资者账户
 . 投资者密码
	. 期货公司交易服务器IP和端口号
 . 期货公司行情服务器IP和端口号


VNPY CTP仿真柜台和SIMNOW是类似的，但VNPY CTP 仿真柜台可以通过修改setting.ini来自由设置滑点和手续费，对于账户接入信息（brokeid、投资者账户、投资者密码、期货公司交易服务器IP和端口号、期货公司行情服务器IP和端口号）随便填写就可，回测流程中只按此返回，并无其他实际意义。
 
 
## 支持的操作系统

VNPY底层仿真回测系统支持Windows操作系统,版本要求Windows7、Windows2008及以上。

## 支持语言和CTP框架

对于各种CTP 编程语言框架，例如Python框架、Java框架、C#框架等，VNPY仿真柜台的实现是一样的，因为这些语言的框架本质上还是调用C++的库文件。
支持各种自编CTP程序和各种编程语言框架，例如C++、Python、JAVA、C#等。 支持 VN.PY、 PyCTP等所有框架和自编程序。 上海期货交易所只提供了 C++原生DLL，对于其他语言均是第三方封装了，只能称为CTP框架。  
 
 
## 列举当前市场上包括VNPY仿真柜台回测系统在内的四类回测架构：

（1）在线回测平台
  这类是基于网站的回测，使用编程语言以Python,javascript为主，可以通过在网站提交代码脚本，在服务商的服务器上进行回测，由此可见这类回测的CPU硬件资源是极其有限的，很难实现基于TICK的高精度回测。 
  由于开发的策略使用的方法依赖于平台提供的函数方法。所以在不同平台的函数方法并不是一致的。
  而且最为关键的是，代码不是本地运行的，而是依赖第三方平台的方法，而且策略本身没有保密性可言；
（2）商业软件实现回测，这里软件开发策略比较容易，也比较完善，但是缺点也很明显，有些策略无法在该平台实现，而且自主设计功能非常有限，比较适合开发能力一般的交易者和对程序化要求较低又愿意付费使用的交易者。
  这类平台的策略内容本质是文本内容，客户端加载策略后，将文本字符串进行分词处理，将不同的单词映射到程序相应的函数模块进行分析，所以执行效率较低。
（3）各种基于原生API的回测框架，一般提供了第三方方法，而不是原生方法，所以这类回测很难移植到其他框架和平台运行。
（4）为了克服上述三里回测技术存在的不足，VNPY的VirtualApi仿真API的回测技术出现了， 通过模拟原生API来实现仿真回测。例如通过模拟原生交易API和行情API，例如通过模拟头文件的定义、模拟原生API的库方法的定义，使得回测和实盘交易代码，只需简单的将实盘代码替换为仿真API，对底层代码可不作改动或改动较少即可实现回测和参数优化。
VNPY开创的仿真回测柜台，主要针对又较强能力的开发者，如果开发者已经基于原生API完成了策略开发，想转到VNPY仿真柜台实现回测则非常容易，只需2分钟即可将实盘程序化交易代码转为回测程序，无需修改原有实盘策列代码。因为他是对原生API仿真的技术，不采用第三方方法，所以决定了VNPY仿真柜台所采用的基础支持市面上所有基于此api的所有框架。

 长远来看，建议选用基于CTP 的API这类 自主开发程序化交易系统，有利于实现更复杂的策略、更灵活的交易操作。即可选用C++、Python、JAVA、C#等编程语言。
 此外，如果选用C++这样的编译性语言，相比脚本语言，可以直接把程序编译成机器可读的二进制代码，因此效率和安全性都更高。


## 如何理解VNPY官方倡导的“精细化回测”？


VNPY官方认为，量化交易回测不仅要测试参数，更要测试策略逻辑和子方案组合。

所谓精细化回测，就是可以追溯到每一笔交易记录的信号触发变量值和逻辑分支，这一点对于CTP开发者通过日志功能尤为容易实现，而且VNPY的仿真柜台文件自带交易记录写入功能，至于资金曲线图形化显示功能则考虑到需要尽可能比较不同策略子方案资金曲线的不同你，则尽量不要显示文字，而对于K线图表对精细化回测而言是不太重要的。


对精细化回测的基础条件则必须是VNPY的TICK级回测，而这一点在下文提到的前3类回测类型中基于数据量庞大和带宽成本的原因都很难实现，而VNPY提出的仿真柜台方案开创性的完美的解决了这个问题。

VNPY仿真回测柜台的这种现实方式也许对一些喜欢K线显示交易信号的开发者不习惯 ，但实际上只有VNPY倡导的这种资金曲线显示方式才能更好的表达出量化交易方案微调子方案之间的优劣的异同。

VNPY仿真回测系统解决了第三方回测框架各自一套费标准方法的问题，通过对原生API进行仿真来实现回测，这样做的好处是可以提供和原生API一致的方法，不再依赖于平台，所以VNPY仿真回测系统支持市场上绝大多数的CTP框架。

VNPY并没有采用市场上各种量化交易框架常用的架构，由于VNPY仿真回测柜台是定位于TICK级的仿真回测，还考虑兼容市面上接口下的各种框架，最终VNPY开创的独特的回测方式成为一种全新的量化交易回测方式。

VNPY仿真回测目前主要提供了基于CTP接口（支持商品期货、股指期货、商品期权、股指期权）的仿真。

VNPY仿真柜台实现量化回测对比前三类量化软件回测具备极大的优势，使得量化交易真正实现的精细化回测的付诸于实施，可以真正避免了和真实盘口不一致的情况，几乎100%还原了真实的价格变化，是真正面向职业开发者的好产品。

很多量化交易软件回测曲线是这样的

![Image text](http://www.vnpy.cn/comm/assets/uploads/files/1598886338836-000f9971-86c0-4ab0-9619-85ab688606b2-%E5%9B%BE%E7%89%87.png)


而VNPY仿真回测柜台资金曲线是这样的

 ![Image text](http://www.vnpy.cn/F0.png)
 
在采用VNPY仿真回测资金曲线和实盘资金曲线分时图取样资金曲线的比较，几乎达到了99.99%的一致。


##  采用VNPY CTP仿真回测柜台测试策略逻辑和子方案组合实施例：

下面以一个策略模板基础上开发的2个子策略做资金曲线对比
回测3分钟(4小时TICK数据)，趋势策略采用了A,B2套不同的止损方案对比
合约上海期货交易所 ni2003   2019年11月4日~2019年12月17日这段时间的TICK数据进行回测，资金曲线图如下所示：

数据回放4小时TICK
 ![VNPYlogo](http://www.vnpy.cn/f1.png?t=1)
 ![VNPYlogo](http://www.vnpy.cn/f2.png?t=1)
数据回放至2019年11月7日
 ![VNPYlogo](http://www.vnpy.cn/f3.png?t=1)
 ![VNPYlogo](http://www.vnpy.cn/f4.png?t=1)

数据回放至2019年12月17日
 ![VNPYlogo](http://www.vnpy.cn/f5.png?t=2)
 ![VNPYlogo](http://www.vnpy.cn/f6.png?t=2)
 
 该大类趋势策略，通过30组子方案得测试优化，获得效果最好得7个子策略，可完美用于实盘
 ![VNPYlogo](http://www.vnpy.cn/f7.png?t=3)
 
 如果要快速理解VNPY仿真柜台做了什么，可以看下面2张图，即原生API典型C++策略和通过VNPY仿真柜台实现回测的架构对比

 ![VNPYlogo](http://www.vnpy.cn/img/d1.gif)
 
 ![VNPYlogo](http://www.vnpy.cn/img/d2.gif)

无论是你自己开发的CTP系统还是CTP框架，甚至是快期V2交易客户端，都可以通过替换dll方式接入VNPY仿真柜台柜台。


## VNPY仿真柜台具备以下优点：

（1）回测精度高，比第二类回测精度高出2个数量级，也就是100倍左右；
（2）性能好，可非常容易通过提升硬件来加快回测速度；
（3）兼容性高，不依赖第三方方方法，原有策略转回测极容易，功能开发的自由度高；
（4）用户覆盖面广，支持C++框架，Python框架，JAVA框架，C#框架在内的所有API框架。支持多种语言。不管你是C++程序员，还是Python程序员，JAVA程序员都能很好满足您的代码回测要求；
（5）策略保密性好，比如C++开发的策略，可以采用加密壳进行保护，策略在指定的本地计算机或托管服务器运行，可做IP绑定、硬件绑定、账户绑定，所以安全性极高。


VNPY仿真回测这项底层仿真回测技术是和编程语言无关的，并且没有第3方平台提供的方法，可以在不修改原有代码的前提下实现回测。

VNPY仿真回测支持各种自编CTP程序，例如C++、Python、JAVA、C#等，同时还支持各种编程语言框架和自编程序。几乎是无所不兼容，这样的产品避免了CTP策略开发者过于依赖平台的窘境。

大多数基于K线的回测都会丢失不少细节的，会产生较大的回测误差，会误导策略开发者。

此外，由于VNPY仿真回测是基于TICK的回测，比大多数第三方软件回测精度高2个数量级以上，实现更精细化的回测。

可以真正帮助策略开发者掉入量化交易回测陷阱。

VNPY仿真回测系统提供了基础免费版本，对所有人免费。

VNPY仿真回测柜台在VNPY开源框架基础以外，真正实现了和平台无关的基于TICK级的精细化回测


VNPY仿真柜台官网是，承诺只做国内合规市场的服务
http://www.vnpy.cn
而域名后缀为com的那个网站是做数字货币的非合规市场的外援网站，并非VNPY官网。

目前VNPY按照国家的法律法律，对VNPY仿真柜台技术做了专利申请保护，现在已经积累了不少私募基金的客户用这个产品。

而VNPY的数据服务是基于网盘提供的，以后可能会升级为付费客户端同步下载数据的服务，这样可以更好的为大家实现仿真回测数据的的下载。

VNPY仿真柜台支持股指期货仿真回测，支持商品期货仿真回测，可以将VNPY仿真柜台视为本地SIMNOW+快速回放TICK数据

无论您之前是CTP开发的策略，都可以过渡到VNPY仿真柜台来做回测。
VNPY仿真柜台支持多种编程语言，开创了第4类回测。

VNPY仿真柜台的用法快速入门可以参考这篇文章


## VNPY的专利技术可以在VNPY知乎官方专栏查看

https://www.zhihu.com/org/vnpy/posts

基于VNPY仿真回测系统受到了VNPY老用户的欢迎和CTP开发者的欢迎，还包括了私募基金以及个人CTP开发者。

VNPY官方计划在2021年推出VNPY仿真柜台高级版本，高级版本计划提供基于多合约的同步回测，以及套利合约回测，加上批处理回测功能，可以指定参数组合，用多个进程副本来实现回测，最后汇总回测结果，给出清晰图形化展示。

由于VNPY开创的第四类仿真回测优点极其明显，在未来，一定会有前三类回测用户逐渐转向VNPY开创的第四类仿真回测柜台系统上来。

## TICK数据获取
 
量化投资的关键要素首先是数据，数据是第一要位，尤其是高质量的数据，假如没有数据就无从做回测，没有好的数据就无法得到正确的结果。
量化投资关键步骤
(1)做数据采集和整理，主要包括数据规划、采集、清洗处理、结构化、API化。因为从各个源头去采集数据的话，需要做很多工作，这部分占了量化模型实现百分之六十左右的工作量。
(2)策略开发和调优，这部分主要包括设计策略模型，编码实现模型，通过数据进行回测，根据结果进行优化改进，这部分主要占据大约百分之三十的工作量。
(3)模拟和交易，策略实盘之前要进行模拟测试，根据实际的行情进行模拟交易跟踪，模拟通过之后进行实盘交易，资金量级的大小会影响策略的效果，不同的阶段要进行很谨慎的测试和模拟。

VNPY是一套基于Python的开源量化交易系统开发框架， 在开源社区6年持续不断的贡献下一步步成长为全功能量化交易平台，目前国内外金融机构用户已经超过500家，包括：私募基金、证券自营和资管、期货资管和子公司、高校研究机构、自营交易公司、交易所等。

托管是指数据中心内属于证券交易所的专用空间。它用于获得执行订单的速度（以纳秒为单位），尽可能接近股票交易所的交易引擎。
基于VNPY数据采集工具采集的TICK数据

 ![Image text](http://www.vnpy.cn/img/pic_datacollect.jpg)
 
 ![Image text](http://www.vnpy.cn/img/pic_history.jpg)
 
通过VNPY提供得数据采集工具和数据下载，可以完美解决VNPY仿真回测系统得回测数据得问题。
 
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
    UpperLimitPrice（涨停板价）,
    LowerLimitPrice（跌停板价）,
    OpenInterest（持仓量）,
    Turnover（成交金额）,
    PreClosePrice (昨收盘),
    PreOpenInterest (昨持仓),
    PreSettlementPrice (上次结算价)


## 知识产权

专利：

 ![Image text](https://pic3.zhimg.com/v2-424952281b14af2b4f458ccd2792b6aa_1440w.jpg?source=172ae18b)

 ![Image text](https://pic2.zhimg.com/80/v2-7ba2f6fb5a04a2c6b9d99061bb0bfeba_720w.jpg)

 ![Image text](https://pic4.zhimg.com/80/v2-2eb2842578eddbf7e7f37849c4c645bc_720w.jpg)
 
 ![Image text](https://pic1.zhimg.com/80/v2-7dd2cd520a1e972f5cddc9342d64283d_720w.jpg)

 ![Image text](https://picb.zhimg.com/80/v2-c69b341c6a941160bfd04b2d4a287707_720w.jpg)
 
 ![Image text](https://pic1.zhimg.com/80/v2-48231226480933de7b7998519f57071a_720w.jpg)
 
 ![Image text](https://pic4.zhimg.com/80/v2-2e9930d0fbdcf75f41fa0cd7821993f2_720w.jpg)
 



## 商业版本请访问
http://www.vnpy.cn

关于商业版本和免费版本的区别如下图：

 ![Image text](http://www.vnpy.cn/vnpy.png)
 
 

## 附加课程1：《C++ ctp策略程序接入VNPY仿真柜台实现回测步骤》
1.下载VNPY仿真柜台

（1）从VNPY官网下载

 http://www.vnpy.cn 
 
 ![VNPYlogo](https://pic4.zhimg.com/80/v2-7a6f0bd21f35fad7c4e52837c7f5a463_720w.jpg)

（2）从Github 下载

https://github.com/vnpycn/vnpy-pro

![VNPYlogo](http://www.vnpy.cn/v1.png?t=1)

2. 下载后解压

![VNPYlogo](https://pic4.zhimg.com/80/v2-90ba6b1dc5ae7001994bde9824c33296_720w.png)

 解压后有如下2个目录：
 
![VNPYlogo](http://www.vnpy.cn/v3.png?t=1)

 打开第一个目录
 这是一个Visual Studio2015 CTP C++  Demo项目
 

 ![VNPYlogo](https://pic3.zhimg.com/80/v2-7f75997c22354b98ffc0d30cb55fd5c7_720w.jpg)

双击 .sln文件打开项目

红圈圈出的是期货账户信息

 ![VNPYlogo](https://pic2.zhimg.com/80/v2-44b4ec32559fcc2640bb88b8183e98dc_720w.jpg)
 
 在项目上右键“重新生成”即可编译为exe程序

 ![VNPYlogo](https://picb.zhimg.com/80/v2-7ce865f35e63aefaf7d2f16e70ff8e48_720w.jpg)
 
 根据下图类似路径可以找到编译好程序的路径位置
 
 ![VNPYlogo](https://picb.zhimg.com/80/v2-c25184b613b388d275254876851c4d00_720w.jpg)

 ![VNPYlogo](https://picb.zhimg.com/80/v2-c39142f1a28a785b549331270a973306_720w.jpg)
 
 
 这样编译好的策略程序就可以运行实盘了
 ![VNPYlogo](https://pic4.zhimg.com/80/v2-8f32d9bd07d5e1cd3e93eb16cbd7682a_720w.jpg)

 下面来讲解一下这个实盘CTP策略程序 如何结合通过VNPY CTP仿真柜台实现TICK级回测
 典型的，CTP的原生API为下图部分
 
  ![VNPYlogo](https://pic3.zhimg.com/80/v2-2a547ad4f1ca97c3f5abd8fe14b199b2_720w.jpg)

 
  VNPY仿真柜台的API如下图
  
  ![VNPYlogo](https://pic4.zhimg.com/80/v2-7e7318f1a682a599c82877692e1cd495_720w.jpg)

 
 其中.lib文件和.h文件是编译中使用的，.dll文件是编译好后倍AutoTrade.exe调用的，我们要实现实盘转回测只要将.dll文件替换即可。
 
如下图，其中圈红色部门的文件为替换文件，蓝色圈出的文件为VNPY仿真柜台API特有文件，拷贝到该目录下即可。
（1）setting.ini 手续费和滑点设置文件；
（2）list.csv 数据文件路径设置文件；
（3）Graph.exe  资金曲线分时图绘制程序，在运行AutoTrade.exe时会自动打开；
也可以待回测完成，打开Graph.exe，再将资金曲线数据文件qy.csv拖入Graph.exe窗口，即可绘制资金曲线分时图；
 
 ![VNPYlogo](https://pic4.zhimg.com/80/v2-df5b7d2358c4de051b43324b79ff287b_720w.jpg)

 
其中list.csv打开如图所示

特别注意：
（1）list.csv数据文件里的合约代码，必须和订阅的合约要一致；
（2）list.csv的数据文件，必须是同一个合约；
（3）暂时不支持多合约测试，计划未来版本支持；
（4）暂时不支持套利测试，计划未来版本支持；

比如图中是./Data/20200627/rb2011.csv
就必须在C++代码订阅的是rb2011这个合约，目前Virtualapi不支持订阅多合约和套利合约，。

 ![VNPYlogo](https://pic4.zhimg.com/80/v2-c616569b33f16b7d4edc2b16b11664e3_720w.jpg)
 
VNPY For CTP目录和CTP API目录，这2个目录下的DEMO，代码完全一样， 将CTP API中的thostmduserapi.lib、thostmduserapi.dll、thosttraderapi.lib、thosttraderapi.dll 这4个文件替换为VNPY CTP仿真柜台文件后，重新编译，将编译好的exe程序目录放入Graph.exe、price.exe、list.csv这3个文件，再次运行AutoTrade.exe 就开始回测了。

实际操作中 ，还可以简化，由于VNPY for  CTP库文件中，.h、.lib和CTP的一致，只要替换dll接口，这样就意味着连策略程序只需替换thostmduserapi.dll、thosttraderapi.dll这2个文件即可实现回测，当然setting.ini 、list.csv、Graph.exe 、price.exe也要放到程序目录下，即转为了仿真回测柜台。

list.csv保存的是依次读取的tick数据文件的路径。
通过直接替换CTP的api，同时将list.csv、Graph.exe、price.exe放到程序编译的目录下面。
直接运行，直接进行回测。


qy.csv保存资金曲线数据
md.csv保存回测期间的分时数据
clean.bat 运行清理历史数据文件。
初始资金为50万，暂时不支持修改初始资金。

VNPY仿真柜台设计的原则就是无需在原实盘策略代码做任何修改就可以实现量化交易回测。
 


## 附加课程2：《快期接入VNPY仿真柜台原理实现》

快期是期货行业使用最广的一款客户端软件，快期也是基于CTP接口的客户端。

我们在这里以快期为例，举例说明来理解VNPY CTP仿真柜台的架构。

快期几乎支持所有期货公司，目前各个期货公司网站都有快期的V2或V3版本，该软件定位是人工下单交易端。


 ![VNPYlogo](http://www.vnpy.cn/v8.png)

 ![VNPYlogo](http://www.vnpy.cn/v9.png)
 
 下载后安装完毕，桌面出现图标
 ![VNPYlogo](http://www.vnpy.cn/v10.png)
 
 我们看下快期安装目录，但这并不是CTP核心文件目录
 
 我们进入到C盘用户的目录下寻找AppData目录，快期真正的核心程序保存在这个目录下，但AppData默认是隐藏的，我们需要开启文件选项
  ![VNPYlogo](http://www.vnpy.cn/v11.png)
 
 
 再进入AppData目录，可以看到多个快期的安装目录，
 其中
 Q72_dfqh_2_standard   表示东方期货的快期V2版本
 Q72_ebfcn_1_standard  表示光大期货的快期V2版本
 Q73_gfqh_2_standard   表示广发期货的快期V2版本
 Q72_hongyuanqh_1_standard  表示宏源期货的快期V2版本

我你们以宏源期货的快期为例，进入到 Q72_hongyuanqh_1_standard 目录下
 

 
 ![VNPYlogo](http://www.vnpy.cn/v12.png)
 
 
 进入快期目录，寻找CTP 二代的库文件 thosttraderapi_se.dll、thostmduserapi_se.dll
 ![VNPYlogo](http://www.vnpy.cn/v13.png)
 ![VNPYlogo](http://www.vnpy.cn/v14.png)
 
 将这2个文件替换为VNPY仿真柜台的版本，然后登录快期
 
 输入任意账户和密码，快期登录成功，这样就骗过了了快期程序登录到了VNPY仿真柜台。
 


## 附加课程3：《VNPY CTP  Python框架接入VNPY仿真柜台实现回测步骤》

VNPY 开源框架是针对Python封装的框架，而VNPY仿真柜台不仅限于Python，他支持各种编程语言的框架。
如何实现VNPY开源框架通过VNPY仿真柜台实现回测呢？

很简单，只要把VNPY CTP开源框架下的所有CTP文件thostmduserapi_se.dll、thosttraderapi_se.dll替换为VNPY仿真柜台提供的同名DLL文件，并将setting.ini、list.csv、Graph.exe这3个文件复制到程序目录，再以运行即可实现接入仿真柜台进行回测。

只需花1分钟时间，就可以将VNPY开源框架的实盘策略转换为TICK级回测。


 

## 版权说明
VNPY仿真柜台版权归http://www.vnpy.cn 经营者所有

对于免费版本，任何个人和组织可自由使用，对收费的版本需通过http://www.vnpy.cn 官网提示购买授权。


## 合作
对于具有自营API的券商、期货公司、交易所、第三方软件服务商等其他公司和企业，可通过VNPY官网的联系方式洽谈合作。


## 项目捐赠

需强调，这是VNPY For 上期CTP接口仿真回测柜台的免费版本，不接受任何捐赠！任何打着VNPY旗号索取捐赠的均为误导。






