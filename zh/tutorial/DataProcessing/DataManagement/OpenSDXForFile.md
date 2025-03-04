---
id: OpenSDXForFile
title: 打开外部矢量文件
---
### ![](../../img/read.gif)使用说明

SDX For Files
文件引擎提供了一种打开外部矢量文件的快捷方式，如用户不想通过导入数据方式导入外部矢量文件，可以采用打开数据源的方式直接打开外部矢量文件。

每一个数据打开为一个数据源，打开的外部矢量文件以矢量数据集的格式添加到该数据源中。

### ![](../../img/read.gif)操作步骤

打开外部矢量文件的操作步骤类似于打开文件型数据源。

1. 在“ **开始** ”选项卡的“ **数据源** ”组中，单击“ **文件型...** ”下拉按钮按钮，在弹出的下拉菜单中选择“打开文件型...”。
2. 在弹出的“打开数据源”对话框，设置打开数据源的必要信息，然后单击“打开”按钮即可打开相应的外部矢量文件。
* **文件名：** 输入要打开的外部矢量文件的文件名。
  * SDX For Files：*.shp、*.mif、*.tab、*.dwg、*.dxf、*.dgn、*.kml、*.kmz、*.gml、*.wal、*.wan、*.wap、*.wat、*.csv、*.e00。
  * Image Plugin Data Engine：*.sit、*.bmp、*.jpg、*.jpeg、*.*.png、*.tif、*.tiff、*.img、*.sci、*.gif、*.gci、*.sct、*.xml、*.ecw、*.sid、*.bil、*.jp2、*.j2k。
* 通过该方式打开有助于用户更便捷快速地打开数据。工作空间对于作为数据源打开的外部矢量文件的管理方式为，在工作空间中建立一个与外部矢量文件同名的数据源，外部矢量文件则为该数据源中的CAD数据集。因此，当将外部矢量文件作为数据源打开后，工作空间管理器中将增加一个数据源结点，结点的显示名称与外部矢量文件的文件名称相同，打开的矢量文件作为 CAD 数据集添加到这个数据源结点下。
3. **打开方式：** 以只读方式打开数据源，数据源的相关信息以及其中的数据都不可修改。

###  注意事项

打开 *.e00、*.gdb、*.gml 和*.dgn 格式，需要 FME 许可和相关的 Bin 包。


