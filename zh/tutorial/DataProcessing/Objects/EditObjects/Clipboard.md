---
id: Clipboard
title: 基本编辑操作  
---  
在“ **对象操作** ”选项卡上的“ **对象操作**
”组用于在地图上编辑各类几何对象，应用程序提供了以下几何对象编辑操作，这些操作只有在当前的矢量图层为可编辑的状态才能进行。

  * **“粘贴”按钮：** 用于将剪贴板上的内容复制到同类型的可编辑的矢量图层上。 

在当前图层为可编辑状态下，单击“粘贴”按钮（或使用快捷键
Ctrl+V），即可将当前保存在剪贴板上的几何对象保存在当前图层，同时被粘贴的对象的属性记录也会追加到粘贴到的数据集的属性表的最后。注意：剪贴板上必须有可粘贴的内容。

复制的对象只能粘贴到能够支持它的数据集中。点、线、面对象分别支持粘贴的数据集说明如下：

  * 点对象支持粘贴到点和 CAD 数据集，或布局窗口中。
  * 线对象支持粘贴到点、线、面、CAD 数据集或布局窗口中，当线对象粘贴到点数据集中时，线对象会自动转换为点对象，即线对象的节点直接转换为点对象；当线对象粘贴到面数据集中时，非直线的线对象会自动转换为面对象，若线对象闭合，则线为面对象的边界，若线对象不闭合，则线对象首尾相连之后转换为面对象。
  * 面对象支持粘贴到线、面、CAD 数据集或布局窗口中，当面对象粘贴到线数据集中时，面对象的边界线会自动转换为线对象。  
    
<table class="normaltable" width="85%">
<thead bgcolor="#6B82B2">
<tr class="normaltableTitle">
<td rowspan="2" width="15%"><div align="center"><strong>复制的对象</strong></div></td>
<td colspan="6" width="85%"><div align="center"><strong>粘贴到的数据集类型</strong></div></td>
</tr>
<tr class="normaltableTitle" >
<td><div align="center"><strong>点数据集</strong></div></td>
<td><div align="center"><strong>线数据集</strong></div></td>
<td><div align="center"><strong>面数据集</strong></div></td>
<td><div align="center"><strong>文本数据集</strong></div></td>
<td><div align="center"><strong>CAD数据集</strong></div></td>
<td><div align="center"><strong>布局窗口</strong></div></td>
</tr>
</thead>
<tr class="normaltablecontent1">
<td><div align="center">点对象</td>
<td><div align="center">支持</td>
<td><div align="center">不支持</div></td>
<td><div align="center">不支持</div></td>
<td><div align="center">不支持</div></td>
<td><div align="center">支持</div></td>
<td><div align="center">支持</div></td>
</tr>
<tr class="normaltablecontent2">
<td><div align="center">线对象</td>
<td><div align="center">支持</td>
<td><div align="center">支持</div></td>
<td><div align="center">支持</div></td>
<td><div align="center">不支持</div></td>
<td><div align="center">支持</div></td>
<td><div align="center">支持</div></td>
</tr>
<tr class="normaltablecontent1">
<td><div align="center">面对象</td>
<td><div align="center">不支持</td>
<td><div align="center">支持</div></td>
<td><div align="center">支持</div></td>
<td><div align="center">不支持</div></td>
<td><div align="center">支持</div></td>
<td><div align="center">支持</div></td>
</tr>
<tr class="normaltablecontent2">
<td><div align="center">文本对象</td>
<td><div align="center">不支持</td>
<td><div align="center">不支持</div></td>
<td><div align="center">不支持</div></td>
<td><div align="center">支持</div></td>
<td><div align="center">支持</div></td>
<td><div align="center">支持</div></td>
</tr>
</table>  

* **“剪贴”按钮：** 用于把选中的几何对象剪贴下来，保存到剪贴板。 

在当前图层为可编辑状态下，选择一个或多个几何对象（辅助 Shift 键），单击"剪贴"按钮（或使用快捷键
Ctrl+X），即可将选中的几何对象从原数据集剪贴下来，保存到剪贴板。

* **“复制”按钮：** 用于对选中的几何对象进行复制，保存到剪贴板。 

在当前图层为可编辑状态下，选择一个或多个几何对象（辅助 Shift 键），单击“复制”按钮（或使用快捷键
Ctrl+C），即可将选中的几何对象复制下来，保存到剪贴板。

* **“多图层编辑”按钮：** 用来控制当前地图窗口中的多图层的可编辑状态。更多相关内容，请参见[开启图层编辑](../CreateObjects/DTv2_Editable)。
* **“撤销”按钮：** 用于撤销上一次的编辑操作。 

在当前图层为可编辑状态下，单击“撤销”按钮（或使用快捷键 Ctrl+Z），即可撤销上一次的编辑操作。

只有在对几何对象进行过编辑操作后，“撤销”操作才为可用状态。

* **“重做”按钮：** 用于重新恢复前一次操作。 

在当前图层为可编辑状态下，单击“重做”按钮（或使用快捷键 Ctrl+Y），即可恢复到前一次撤销操作前的状态。

只有在进行过撤销操作后，“重做”按钮才为可用状态。

* **“风格刷”按钮：** 用于将一个对象的风格赋给其他对象。有关风格刷的更多内容，请参见[风格刷](StyleBrush)。
* **“属性刷”按钮：** 用于将一个对象的部分或全部可编辑字段及其值赋给其他对象。有关属性刷的更多内容，请参见[属性刷](PropertyBrush)。

