---
id: AboutAccessbility
title: 通达性分析概述
---
### ![](../img/read.gif)使用说明

在现实生活中，网络可能不是完全连通的。如果需要确定哪些点或者弧段之间是连通的，哪些点或弧段之间不连通，可以使用邻接要素分析或者通达要素分析功能。网络连通性分析的最大特点是不需要考虑网络网络阻力（既不考虑转向权值，也不考虑禁止通行的情况），网络上的要素只有连通和不连通的区别。

**连通性分析参数设置**

在进行连通性分析之前，需要设置连通性分析参数。需要设置的参数包括：

* **查找方向** ：与网络中弧段的方向有关。查找不同，分析的结果会有所不同。 
  * **向前查找** :沿着网络中弧段的方向向前进行查找。
  * **向后查找** :沿着网络中弧段的方向向后查找。
  * **双向查找** :沿着网络中弧段的两个方向查找，即向前和向后进行查找。

* **查找等级** ：进行连通性分析时，查找弧段的级数，可以理解为网络的深度。与事件点直接相连通的弧段（或结点）为第一级通达边（通达点）。沿分析方向与第一级结点直接相连通的弧段（结点）为第二级通达边（通达点）。由此类推同样可以得到第三级、第四级......的所有通达边（通达点）。当与事件点连接的级数超过设置的参数将不再往下查找。邻接要素分析中，查找等级为1，即仅查找与事件点相邻接的要素。通达要素分析中，可以查找多个等级，默认查找等级数为2。

SuperMap 应用程序提供的连通性分析主要包括以下功能：

<table width="90%">
<thead bgcolor="#6B82B2">
<tr>
<td rowspan="2" width="15%"><div align="center"><strong>连通性分析</strong></div></td>
<td rowspan="2" width="30%"><div align="center"><strong>功能描述</strong></div></td>
<td rowspan="2" width="10%"><div align="center"><strong>设置障碍点</strong></div></td>
<td colspan="4" width="50%"><div align="center"><strong>参数设置</strong></div></td>
</tr>
<tr >
<td><div align="center"><strong>向前查找</strong></div></td>
<td><div align="center"><strong>向后查找</strong></div></td>
<td><div align="center"><strong>双向查找</strong></div></td>
<td><div align="center"><strong>查找等级</strong></div></td>
</tr>
</thead>
<tr>
<td><a href="AdjoinAnalyst"><strong>邻接要素分析</strong></a></td>
<td><div>查找与添加的事件点相邻接的所有要素（结点或者弧段）。</div></td>
<td><div align="center">无影响</div></td>
<td><div align="center">有效</div></td>
<td><div align="center">有效</div></td>
<td><div align="center">有效</div></td>
<td><div align="center">默认为1，不可以修改。</div></td>
</tr>
<tr>
<td><a href="AccessibilityAnalyst"><strong>通达要素分析</strong></a></td>
<td><div>按照查找等级，查找与添加的事件点相连通的结点或弧段。</div></td>
<td><div align="center">无影响</div></td>
<td><div align="center">有效</div></td>
<td><div align="center">有效</div></td>
<td><div align="center">有效</div></td>
<td><div align="center">默认为2，可以设置。</div></td>
</tr>
<tr>
<td><a href="CriticalAnalyst"><strong>关键要素分析</strong></a></td>
<td><div>查找出两个指定结点之间必须经过的结点和弧段。</div></td>
<td><div align="center">无影响</div></td>
<td><div align="center">无效</div></td>
<td><div align="center">必须</div></td>
<td><div align="center">必须</div></td>
<td><div align="center">无效</div></td>
</tr>
<tr>
<td><a href="ConnectedAnalyst"><strong>两点连通性分析</strong></a></td>
<td><div>判断指定的两结点是否相通。</div></td>
<td><div align="center">有影响</div></td>
<td><div align="center">无效</div></td>
<td><div align="center">无效</div></td>
<td><div align="center">无效</div></td>
<td><div align="center">无效</div></td>
</tr>
</table>
