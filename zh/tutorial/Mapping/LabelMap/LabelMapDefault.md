---
id: LabelMapDefault
title: 新建标签专题图
---
### ![](../../img/read.gif)使用说明

在图层管理器中选中一个矢量图层，右键单击，在弹出的右键菜单中选择“ **制作专题图...**
”，在弹出的对话框中单击“标签专题图”，在右侧列表框中选择某种类型的标签专题图项，即可基于当前矢量图层制作一幅由应用系统采用默认风格制作的标签专题图。

### 统一风格标签专题图

统一风格标签专题图是指标签专题图基于专题变量（属性字段或字段的数学表达式）对用来制作标签专题图的矢量图层中的对象进行文本标注，标注的内容为该对象对应的专题值，并且所有对象的标注内容都采用统一的文本风格，即标签专题图中的所有文本对象都采用指定的一种显示风格。

 [如何制作统一风格标签专题图？](UniformLabelMap)

### 分段风格标签专题图

分段风格标签专题图是指标签专题图基于专题变量（属性字段或字段的数学表达式）对用来制作标签专题图的矢量图层中的对象进行
文本标注，标注的内容为该对象对应的专题值；同时，标签专题图又基于另一个指定的专题变量（属性字段或字段的数学表达式），对用来制作标签专题图的矢量图层中的对象所对应的所有专题值进行分段，产生多个范围段，对象专题值在同一个范围段中的对象，其对应的标签专题图中的标注文本对象采用
一种文本风格显示，而不同范围段中对象对应的标注文本风格不同，因此，分段风格标签专题图中的文本对象的文本风格不统一，具有多样性，从而反映不同类别对象的说明信息。

 [如何制作分段风格标签专题图？](RangesLabelMap)

### 复合风格标签专题图

复合风格标签专题图是指基于专题变量（属性字段或字段的数学表达式）对用来制作标签专题图的矢量图层中的对象进行
文本标注，标注的内容为该对象对应的专题值，同时，可以使标签专题图中的每个文本对象的文本内容通过一定的规则进行分割，
将文本对象中的文本内容分为多个段，每个段中的文字采用一种文本风格显示，不同段中的文本风格不同。

 [如何制作复合风格标签专题图？](MixedLabelMap)

### 标签矩阵专题图

标签矩阵专题图即矩阵式标签专题图，指在标签专题图中采用矩阵式格式来组织用于标注的内容，因此，对用来制作标签专题图的矢量图层中的每一个对象采用一个矩阵式标签进行标注。标签矩阵可以承载丰富的标注内容，可以将符号、图片、文本集于一个标签矩阵中，然后来标注相应的对象。矩阵式格式，是指类似于一个
n 行 m
列的表格，表格中每一个单元格对应一个专题变量，在标签专题图中，该位置的单元格最终显示对象对应的专题值。单元格可以显示图片、符号、和文本信息，并且单元格可以嵌套另一个
n 行 m 列的表格，形成复杂的矩阵式标签专题图。

 [如何制作标签矩阵专题图？](LabelMatrixMap)

