---
id: AboutCreateGeometry
title: 对象绘制概述
---
地图绘制中最常用的几何对象是点、线、面、文本四种。“对象操作”选项卡提供了在地图上创建各类几何对象的功能，包括：点对象绘制、线对象绘制、面对象绘制和文本对象绘制。

各种几何对象的绘制都在图层可编辑得状态下进行，同时设置多个图层可编辑，但是在创建点、线、面或文本对象时，只针对当前选中的图层进行几何对象绘制。因此，如果想要对某个图层创建新对象，必须首先单击图层管理器中的相应图层，将该图层设置为当前图层。

下面就对象绘制中涉及的一些概念做如下介绍：

### 对象概述

对象（Object）：即几何对象，在 GIS 中对离散空间实体的抽象表示。一个对象具有自己的属性和行为。在 SuperMap
中有些对象可以直接创建，有些则需要通过转换生成。

* 单一对象（Single Object）：即指一个对象，一个简单对象、一个复杂对象、一个复合对象、一个子对象都是单一对象。
* 子对象（part）：是指简单对象和复杂对象的组成单元。简单对象由一个子对象组成，即其本身；复杂对象由两个或两个以上子对象组成。 
* 简单对象（Simple Object）：是指只有一个子对象（即其本身）的对象。
* 复杂对象（Complex Object）：是指具有两个或多个子对象的对象，这些子对象是同类型的。
* 复合对象（Compound Object）：特指在 CAD 图层中由组合运算生成的对象。复合对象没有子对象的概念。
* 参数化对象：通过主要参数来绘制几何对象，是连续的。而普通几何对象是用组成该对象的关键点或者点串的坐标来绘制的。例如参数化圆是通过确定的圆心和半径两个参数来精确绘制的；而普通的圆将组成圆的圆弧离散化去点，然后用这些点连成线形成封闭的圆。

### 对象绘制中的角度说明

* 角度方向：应用程序中涉及到的角度方向均为逆时针方向。
* 起始角度：绘制对象中的起始角度是指以正北方向为起始边，到另一条边之间的夹角。

### 参数化绘制说明

在绘制一些对象过程中，直接输入绘制对象的坐标、长度、角度等参数，可以使绘制过程更加便捷。可在“对象操作”选项卡的“对象绘制”组中，单击“参数化绘制”按钮，也可通过“Shift+P”的快捷方式启用参数化绘制功能。

* 输入坐标值：通过坐标点参数来绘制点、直线、折线、曲线、圆、多边形等，其中包括对象的起点、中点、转折点、终点等坐标。
* 输入长度值：通过输入对象长度参数绘制来绘制直线、折线、多边形、扇形、圆、圆弧等，包括限度长度、边长、半径、直径等。
* 输入角度值：通过输入角度值来绘制对象，可确定绘制对象方向和起始角度。

### Shift 键的使用说明

在绘制一些对象过程中，配合 Shift 键的使用，可以使绘制过程更加便捷。

* 绘制直线：通过输入长度、角度参数绘制直线时，按住 Shift 键只能绘制水平、垂直或者45°方向的直线。
* 绘制矩形（圆角矩形）：通过输入宽度、高度参数绘制矩形时，按住 Shift 键，将得到宽度和高度相等的正方形。
* 绘制椭圆：通过输入外接矩形宽度和高度参数绘制椭圆时，按住 Shift 键，将得到外接矩形的宽度相等的正圆。

### A 键的使用说明

在地图中绘制对象时，即鼠标为绘制状态时，按下键盘中的字母“A”键，可将当前地图窗口中的鼠标切换为绘制漫游状态。

绘制对象过程中切换鼠标为绘制漫游状态后，可通过以下三种方式将鼠标状态切换为绘制状态，继续绘制对象：

* 再次按下“A”键进行切换；
* 单击鼠标右键进行切换；
* 按下键盘中“Esc”键进行切换。

### 注意事项

* 若绘制对象时正在输入绘制对象的坐标、长度、角度等参数，按“A”键不能将鼠标切换到绘制漫游状态。
* 在打开空地图（地理坐标系）的窗口默认范围为可绘制范围，能够有效避免默认窗口范围绘制对象时提示超范围的情况。


