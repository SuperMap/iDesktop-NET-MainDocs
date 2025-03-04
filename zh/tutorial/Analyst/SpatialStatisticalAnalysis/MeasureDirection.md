---
id: MeasureDirection
title: 方向分布
---
方向分布可以反映要素的分布中心、离散趋势以及扩散方向等空间特征。该方法是由平均中心作为起点对 x 坐标和 y
坐标的标准差进行计算，从而定义椭圆的轴，因此该椭圆被称为标准差椭圆。

### 应用案例

  * 在地图上标示一组犯罪行为的分布趋势可以确定该行为与特定要素（一系列酒吧或餐馆、某条特定街道等）的关系。
  * 在地图上标示地下水井样本的特定污染可以指示毒素的扩散方式，这在部署减灾策略时非常有用。
  * 对各个种族或民族所在区域的椭圆的大小、形状和重叠部分进行比较可以提供与种族隔离或民族隔离相关的深入信息。
  * 绘制一段时间内疾病爆发情况的椭圆可建立疾病传播的模型。

### ![](../../img/read.gif)功能入口

  * 在 **空间分析** 选项卡-> **空间统计分析** -> **度量地理分析** -> **方向分布** ；
  * **工具箱** -> **空间统计分析** 工具-> **度量地理分析** -> **方向分布** ；(iDesktopX)

### ![](../../img/read.gif)主要参数

  * **源数据** ：设置待分析的矢量数据集，支持点、线、面三种类型的数据集。
  * **椭圆大小** ：用于设置结果椭圆的级别，根据结果包含的数据量范围分为三个级别，不同的标准差等级，得到的结果中心点会有差别。 
    * 一个标准差：第一级标准差的结果范围可将约68%的源数据质心包含在内；
    * 两个标准差：第二级标准差的结果范围可将约95%的源数据质心包含在内；
    * 三个标准差：第三级标准差的结果范围可将约98%的源数据质心包含在内；
  * **分组字段** ：将分析要素分类别的字段，分类后每一组的对象分别会有一个椭圆，分组字段可以是整型、日期型或字符串类型。若分组字段中字段值为空，则会将该要素从分析中排除。
  * **权重字段** ：设置一个数值型字段为权重字段，例如：用一个交通事故等级字段作为权重字段，结果椭圆不仅可以反映事故的空间分布，还可以反映交通事故的严重程度。
  * **保留统计字段** ：在字段列表框中设置结果数据的保留字段及字段值的统计类型。
  * **结果设置** ：设置结果数据所要保存在的数据源，及数据集名称。

### 结果输出

输出的结果为面数据集，其中每个椭圆对象中会包含五个属性字段：圆心的X和Y坐标、长半轴、短半轴、椭圆方向。

字段名称 | 属性意义  
---|---  
CircleCenterX | 圆心X坐标  
CircleCenterX | 圆心Y坐标  
SemiMajorAxis | 长半轴  
SemiMinorAxis | 短半轴  
RotationAngle | 椭圆的方向  
  
椭圆方向即长半轴与正北方向的夹角。长半轴反映了离散程度较大的方向，短半轴反映了聚集程度较高的方向。长短半轴的值差距越大（扁率越大），表示数据的方向性越明显。反之，如果长短半轴越接近，表示方向性越不明显。如果长短半轴完全相等，就等于是一个圆了，圆的话就表示没有任何的方向特征。

可以对犯罪事件进行分析，可以发现作案的趋势特征，酒吧或作案场地等；也可以分析污染物扩散的方向特征等等。下图为通过该工具得到的手机流量使用的高、中、低分布走势情况：

![](img/MeasureDirection.png)

###  相关主题

 [中心要素](CentralFeature)

 [平均中心](MeanCenter)

 [中位数中心](MeanCenterResult)

 [线性方向平均值](MeasureLinearDirectional)

 [标准距离](MeasureStandardDistance)

