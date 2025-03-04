---
id: DTgroupDiaGrid
title: 栅格数据集属性窗口  
---  
如果数据集属性窗口--显示栅格数据集信息显示的是一个或者多个栅格数据集的信息，则“属性”窗口有三个模块信息：
数据集、坐标系、栅格，每一个面板都显示对应的信息内容。下面详细介绍各类信息的具体内容：

### ![](../../img/read.gif)数据集信息

单击“属性”窗口中的“数据集”面板，即可显示该栅格数据集的属性信息。

**基本信息：**

  * **数据集名称：** 显示栅格数据集的名称。
  * **数据集类型：** 显示数据集的类型。
  * **数据表名：** 显示数据集的属性表的名称。 
  * **编码方式：** 显示栅格数据集的编码方式，即数据集存储时的压缩编码方式，有关数据集的编码方式的详细内容，请参见：[数据集压缩编码方式](EncodeType)。

**数据集范围：**

  * 上、下的值为沿 Y 轴方向（即‘Y=’）的两个边界；左、右的值为沿 X 轴（即‘X=’）方向的两个边界，数值的单位与数据集的单位相同。可直接输入数值进行修改，单击属性窗口右下角的“应用”按钮即可生效。
  * **复制粘贴** ：单击“ **复制** ”按钮可复制当前数据集范围，也可单击“ **粘贴** ”按钮，即可将复制范围的左、下、右、上值设置到当前范围。

**数据集描述：**

  * **数据集描述：** 显示栅格数据集的描述信息，用户可以编辑数据集的描述信息。

### ![](../../img/read.gif)坐标系

单击“属性”窗口中的“坐标系”结点，面板将显示该栅格数据集的坐标系信息。

  * **坐标系名称：** 显示栅格数据集的坐标系信息。
  * **单位：** 显示栅格数据集的距离单位。
  * **坐标系信息：** 显示栅格数据集投影的详细描述信息。

坐标系信息显示区域下方的按钮功能说明：

  * **重设：** 单击此按钮，弹出“投影设置”对话框，重新设置该数据集的坐标投影信息。具体设置方法，参见[“投影设置”窗口](../projection/PrjCoordSysSettingWin)。 
  * **复制：** 点击该按钮，弹出“复制坐标系”对话框，可复制坐标系信息作为当前数据集的投影信息。系统提供了3种复制坐标系的方式：复制当前工作空间中已有数据源坐标投影信息、复制当前工作空间中已有数据集的坐标投影信息、从本地复制指定的投影信息文件。系统支持7种投影信息文件，分别是：TIFF文件（*.TIF）、SIT文件（*.SIT）、Erdas Image文件（*.IMG）、ArcView shape 文件（*.SHP）、MapInfo交换格式（*.MIF）、MapInfo TA文件（*.TAB）、投影信息文件（*.XML）。 
  * **导出/导出坐标系：** 支持导入/导出投影信息文件（*.xml。 
  * **转换：** 单击此按钮，弹出“投影转换”对话框，转换选中数据集的当前投影信息。具体设置方法，参见[投影转换](../projection/ConvertPrjCoordSys)中关于“投影转换”对话框的操作说明。

### ![](../../img/read.gif)栅格

单击“属性”窗口中的“栅格”结点，面板将显示该栅格数据集的信息。

**属性：**

  * **像素格式：** 显示栅格数据存储的像素格式，即每个像素值采用多少字节来表示。
  * **X 分辨率：** 显示栅格数据集 X 方向上的分辨率。
  * **Y 分辨率：** 显示栅格数据集 Y 方向上的分辨率。
  * **空值：** 显示栅格数据集中没有数据的像元的栅格值。
  * **行数：** 显示栅格数据集像元阵列的行数。
  * **列数：** 显示栅格数据集像元阵列的列数。
  * **颜色方案：** 用于设置所选栅格数据集中像元的显示颜色。该设置是针对栅格数据集本身的颜色表进行修改，若只想对当前地图中栅格数据集的颜色表进行修改，请参见[设置栅格图层的颜色表](../../Visualization/VisualSetting/ColorTableDia)。设置后的颜色方案可在新打开的地图窗口中看到。
  * **栅格分块：** 显示了当前栅格数据集栅格分块的大小，例如显示为256*256时，表示每256*256个象素会存储为一个栅格块，进行数据处理时一个栅格块一起处理。

**极值：**

  * **最大值：** 显示栅格数据集中栅格值的最大值。
  * **最小值：** 显示栅格数据集中栅格值的最小值。

**其它：**

  * **金字塔：** 显示栅格数据集是否已创建金字塔。
  * **显示范围：** 用于设置栅格数据集在地图中的显示范围。对选中的栅格数据集设置显示范围后，该栅格数据集将仅显示所设范围内的信息，而其余部分是不可见的。 

单击右侧的“设置”按钮，会弹出“设置显示范围”对话框，可以将当前工作空间的某一面数据集作为所选栅格数据集的显示范围；也可以单击过滤表达式右侧按钮，则弹出
SQL
表达式对话框，在该对话框中设置过滤表达式，以此控制栅格数据集的显示范围，具体内容请参见[SQL语句查询](../../Query/SQLQueryDia)。

单击“重置”按钮，可将数据集显示范围重置为完整显示数据集。

###  注意事项

栅格数据集“属性”对话框中的“投影转换”按钮为灰显，栅格数据集只支持通过“开始”选项卡“数据”组的“投影转换”，或者右键菜单中的“投影转换”功能进行投影转换，具体操作方法，请参见[投影转换](../Projection/ConvertPrjCoordSys)。

