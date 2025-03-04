---
id: Overlayoperation
title: 叠加分析算子介绍
---
SuperMap 目前提供了7种叠加分析的算子。下面分别进行介绍：

## 裁剪

裁剪是用裁剪数据集从被裁剪数据集中提取部分特征集合的运算。裁剪数据集中的多边形集合定义了裁剪区域，被裁剪数据集中凡是落在这些多边形区域外的特征都将被去除，而落在多边形区域内的特征要素都将被输出到结果数据集中。

![](img/clipbuttonoperation.png)  
  
裁剪运算的输出结果的属性表来自于被裁剪数据集的属性表，其属性表结构与被裁剪数据集结构相同，属性值中除了面积、周长、长度等需要重新计算外，其余皆保留被裁剪数据集A的属性值。如下图所示，自动添加数据集A中的所有字段。

![](img/clipbuttonproperty.png)  

合并是求两个数据集并的运算。进行合并运算后，两个面数据集在相交处多边形被分割，重建拓扑关系，且两个数据集的几何和属性信息都被输出到结果数据集中。

![](img/unionbuttonoperation.png)   
  
合并运算的输出结果的属性表来自于两个输入数据集属性表，在进行合并运算的时候，用户可以根据自己的需要在A、B的属性表中选择需要保留的属性字段。

目前叠加分析结果字段名称按照“字段名称_1”和“字段名_2”，如下图所示。

![](img/unionbuttonproperty.png)  
  
## 擦除

擦除是用来擦除掉被擦除数据集中多边形相重合部分的操作。擦除数据集中的多边形集合定义了擦除区域，被擦除数据集中凡是落在这些多边形区域内的特征都将被去除，而落在多边形区域外的特征要素都将被输出到结果数据集中。擦除运算与裁剪运算原理相同，只是对源数据集中保留的内容不同。

![](img/erasebuttonoperation.png)  
  
擦除运算的输出结果的属性表来自于被擦除数据集的属性表，其类型与被擦除数据集类型相同，如下图所示，自动添加数据集A属性表中的所有非系统字段。

![](img/erasebuttonproperty.png)  
  
## 求交

求交运算是求两个数据集的交集的操作。待求交数据集的特征对象在与交数据集中的多边形相交处被分割（点对象除外）。求交运算与裁剪运算得到的结果数据集的空间几何信息是相同的，但是裁剪运算不对属性表做任何处理，而求交运算可以让用户选择需要保留的属性字段。

![](img/intersectTEST2.png)   

  
求交结果数据集属性表除了包括自身的属性字段，还包括待求交数据集和交数据集的所有属性字段，用户可以根据自己的需要从A、B数据集属性表中选择自己需要保留的字段。如下图所示：  
![](img/intersectTEST1.png)  

  
## 同一

同一运算结果图层范围与源数据集图层的范围相同，但是包含来自叠加数据集图层的几何形状和属性数据。同一运算就是源数据集与叠加数据集先求交，然后求交结果再与源数据集求并的一个运算。如果第一个数据集为点数集，则新生成的数据集中保留第一个数据集的所有对象；如果第一个数据集为线数据集，则新生成的数据集中保留第一个数据集的所有对象，但是把与第二个数据集相交的对象在相交的地方打断；如果第一个数据集为面数据集，则结果数据集保留以源数据集为控制边界之内的所有多边形，并且把与第二个数据集相交的对象在相交的地方分割成多个对象。

![](img/identitybuttonoperation.png)   
  
同一运算的输出结果的属性表字段除系统字段外都来自于两个输入数据集的属性字段，用户可以根据自己的需要，从源数据集和叠加数据集的属性字段中选择字段。如下图所示：

![](img/identitybuttonproperty.png)  

## 对称差

对称差运算是两个数据集的异或运算。操作的结果是，对于每一个面对象，去掉其与另一个数据集中的几何对象相交的部分，而保留剩下的部分。

![](img/xorbuttonoperation.png)    
  
对称差运算的输出结果的属性表包含两个输入数据集的非系统属性字段，如下图所示：

![](img/xorbuttonproperty.png)    
  
## 更新

更新运算是用更新数据集替换与被更新数据集重合的部分，是一个先擦除后粘贴的过程。结果数据集中保留了更新数据集的几何形状和属性信息。

![](img/updatebuttonoperation.png)  
  
更新运算输出结果的属性表如下图所示，A、B数据集几何对象重合部分的属性值更新为B的属性值。

![](img/updatebuttonproperty.png)  

