---
id: DatasetButton
title: 输出属性表
---
支持将属性表另存为数据集或保存为 Excel 文件。

### ![](../../img/read.gif)另存为数据集

**另存为数据集**
是以记录行为操作单位将矢量数据集属性表存储的全部或部分空间信息或属性信息输出为新的数据集或者纯属性数据集，或者将纯属性表的全部或部分属性信息输出为新的纯属性数据集。

**功能入口**

在打开的属性表中，选择需要输出的记录行（只要记录行中有一个单元格被选中，即选中了该记录行），可配合使用 Ctrl 或 Shift 键进行选择。

* 在“ **属性表** ”选项卡的“ **输出** ”组中，单击“另存为数据集”按钮，弹出的“另存为数据集”对话框。
* 单击右键，选择“另存为数据集”，弹出的“另存为数据集”对话框。

**参数描述**

* **字段信息** ：将选中字段值保存在另存数据集中。
* **数据源** ：输出的结果数据集所保存的数据源。
* **数据集** ：输出的结果数据集的名称。
* **结果数据集类型** ：设置将矢量数据集的属性表输出为新的数据集还是输出为纯属性数据集。如果当前属性表为矢量数据集的属性表，将其输出为新的数据集时，数据集的类型与该数据集的类型相同；如果当前属性表为纯属性数据集的属性表，则只能将其输出为纯属性数据集。
* **编码方式** ：将矢量数据集的属性表输出为新的数据集时，可以重新设置数据集的编码方式。

在将矢量数据集（除了点数据集）的属性表输出为新的数据集时，系统提供了四种矢量数据压缩编码方式供用户选择：单字节、双字节、三字节、四字节，分别指的是使用1个、2个、3个、4个字节存储为一个坐标值。用户可根据实际需要选择一种矢量数据压缩方式。

生成的结果数据集将显示在工作空间管理器中其所保存的数据源的结点下。

### 注意事项

* 在默认没有选中单元格时，应用程序将输出属性表的所有记录。
* 如果用户在“另存为数据集”对话框中输入的结果数据集的名称不合法，则系统会提示用户修改结果数据集名称。
* 用户可以同时打开几个数据集的属性表或纯属性数据集，但是只能对当前属性表窗口中显示的属性表或纯属性数据集进行输出操作。

### ![](../../img/read.gif)保存为Excel

“保存为Excel”是来将矢量数据集或者纯属性表数据集属性表保存为 Excel。将数据集保存为 Excel 时，可将整个属性表保存为
Excel，也可只保存选中的记录。

**功能入口**

在打开的属性表中，选择需要输出的记录行（只要记录行中有一个单元格被选中，即选中了该记录行），可配合使用 Ctrl 或 Shift 键进行选择。

* 在“ **属性表** ”选项卡的“ **输出** ”组中，单击“保存为Excel”按钮，弹出的“保存为Excel”对话框。
* 单击右键，选择“保存为Excel”，弹出的“保存为Excel”对话框。

**参数描述**

* **字段列表** ：在字段列表中勾选要输出的字段，可通过工具栏中的全选、反选、选择系统字段、选择非系统字段功能进行选择。默认勾选非系统字段。
* **文件名** ：输出结果 Excel 的名称。
* **路径** ：输出结果所保存的路径。
* **仅保存选中记录** ：选中该复选框表示，仅将选中记录保存为 Excel；若不勾选则将全部记录保存为 Excel。

###  注意事项

* 若没有选中属性表单元格，应用程序将保存属性表的所有记录。
* 用户可以同时打开几个数据集的属性表或纯属性数据集，但是只能对当前属性表窗口中显示的属性表或纯属性数据集进行保存为 Excel 操作。




