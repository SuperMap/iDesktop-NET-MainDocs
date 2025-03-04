---
id: ImportIMG
title: 影像文件的导入  
---  
### ![](../../img/read.gif)使用说明

应用程序支持导入多种影像格式，如 IMG、TIF、BMP、JPG、GIF、SIT 等。

### ![](../../img/read.gif)功能入口

* **开始** 选项卡-> **数据处理** -> **数据导入** 或下拉按钮。
* 在工作空间管理器中选中需导入到的 **数据源** ->单击鼠标右键-> **导入数据集...** 。
* **工具箱** -> **数据导入** -> **影像位图文件** 中的工具。(iDesktopX)

### ![](../../img/read.gif)操作步骤

下面介绍如何导入 IMG 和 TIF 文件。

1. 在“数据导入”对话框中结果设置处的目标数据源、结果数据集、编码类型、导入模式，以及源文件信息的参数说明，请参见[数据导入公共参数](ParameterSettingDia)说明页面。
2. **结果设置：**
* 数据集类型：设置导入数据的类型。导入栅格数据的结果类型有影像数据集和栅格数据集2个选项供用户选择。选择“影像数据集”项，则将数据文件导入为影像数据集；选择“栅格数据集”项，则将数据文件导入为 GRID 数据集。
3. **转换参数：**
* 波段导入模式：用于设置在导入多波段影像数据，如 Erdas Image 文件(*.img)和 TIFF 文件(*.tif)时，影像数据的波段导入模式。系统提供了多波段、多个单波段和合成波段3种方式。 
  *  多个单波段：将多波段数据导入为一个单波段数据集。  
  * 多波段：将多波段数据导入为一个多波段数据集。在多波段数据集的属性窗口中，定位到图像属性项，可以查看其波段表信息。  
  * 合成波段：将多波段数据导入为一个单波段数据集。合成后的数据集只有一个波段。注意：目前此导入模式只适用于将8位多波段的数据导入为一个24位或者32位的单波段数据集。
* 创建影像金字塔：勾选该复选框，在导入影像数据时，将对导入数据创建影像金字塔。
* 坐标参考文件：在导入影像文件（仅对 tif 文件有效）时，可以导入*.tfw 坐标参考文件。有关坐标参考文件的介绍，请参见[影像地理坐标参考文件](ImageReferFiles)。
4. 设置好以上参数后，单击对话框中的“导入”按钮，即可将指定数据导入为影像数据。

### 备注

1. 如果导入单波段栅格数据，则导入模式：“无”和“追加”是同样效果，即若导入的数据与已有数据集存在名称冲突，则导入的数据将自动修改名字并进行导入。
2. 在导入 RAW 影像文件时，结果类型只能导入为 Image 数据集。不支持在 Image 数据集和 Grid 数据集之间选择。
3. 导入*.img、*.tif 或*.tiff 格式的数据时，导入后结果数据集投影坐标系与源文件的投影一致；导入*.bmp、*.png、*.jpg 或*.gif 格式的数据时，导入后结果数据集的投影坐标系与所在数据源投影一致。
4. 导入*.SIT影像时，支持设置波段导入模式，程序提供选择“波段导入模式”，分别是“多个单波段”和“多波段”。

###  注意事项

由于 img 格式的影像数据不支持 SphereMercator 投影方式，该投影方式的数据导出为 img
后，会导致投影信息丢失。建议用户再次使用时，重新设定投影。


