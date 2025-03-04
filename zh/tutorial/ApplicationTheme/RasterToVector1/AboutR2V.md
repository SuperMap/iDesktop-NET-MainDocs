---
id: AboutR2V
title: 如何进行栅格矢量化
---
再进行栅格矢量化之前，需要了解以下几个问题：

1. 什么是栅格矢量化？ 

将栅格数据转化为矢量数据的过程称为栅格矢量化。

2. 为什么要进行栅格矢量化？ 

矢量数据相对于栅格数据而言具有数据结构紧凑、冗余度低，有利于网络和检索分析，图形显示质量好、精度高等优点，在进行一些应用分析时需要对栅格数据进行矢量化。

3. 栅格矢量化有哪些方法，分别在什么情况下使用？ 

栅格矢量化方法主要有两种：半自动跟踪矢量化和全自动跟踪矢量化。

* 半自动跟踪矢量化是采取人机交互的形式进行的，对光栅图上的线划逐条进行矢量化。如果线图像划的质量较好，系统将自动化跟踪，直到不能跟踪的位置停止，然后通过人机交互，再继续往前跟踪，直到本次跟踪结束。它适用于等高线图、水系图、道路图等一些线元素较多的地图。
* 全自动跟踪矢量化是由系统自行完成全部线划的矢量化工作，无需人员的介入。它适合线条质量高，图形比较简洁的场合。
4. 栅格矢量化的具体流程是什么？ 

目前， 桌面支持半自动栅格矢量化功能。在“ **对象操作** ”选项卡的“ **栅格矢量化** ”组中，提供了栅格矢量化线、面等相关的操作。在进行半自动矢量化过程中，可以辅助用户更好地完成栅格矢量化工作。

在了解了上述4个问题后，相信你对栅格矢量化有了一定的了解，SuperMap同样提供了两种栅格矢量化方法，即半自动跟踪矢量化和全自动跟踪矢量化。本专题将通过对等高线图的矢量化过程来详细介绍SuperMap中这两种栅格矢量化功能的使用。

栅格矢量化功能主要包括以下内容：

 [自动栅格矢量化](AutoR2V)

 [半自动栅格矢量化](Semi-AutoR2V)

