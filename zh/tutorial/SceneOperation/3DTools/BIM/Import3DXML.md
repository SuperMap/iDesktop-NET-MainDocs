---
id: Import3DXML
title: 导入3DXML  
---  
### ![](../../img/read.gif)使用说明

“导入3DXML”命令，用来导入达索3DXML格式的BIM数据，并在数据源中新增模型数据集结点。

### ![](../../img/read.gif)操作步骤

  1. 在工作空间管理器中选中需导入到的数据源或者新建数据源并选中。
  2. 单击“ **三维数据** ”选项卡中“ **模型** ”组内的“ **BIM** ”下拉菜单中的“ **导入3DXML**”按钮，弹出“数据导入”对话框。
  3. 通过"添加数据"按钮，在弹出的“打开”对话框选择需要导入的3DXML数据。
  4. 文件列表：文件列表显示了当前打开的文件，可选择某一具体3DXML文件进行导入。
  5. 基本信息设置
      * 目标数据源：通过右键下拉按钮选择导入的数据源。
      * 目标数据集：打开的模型数据集的名称。
      * 导入模式：默认为无。提供无、追加和强制覆盖三种模式。
  6. 参数设置：
      * 模型参考点（模型中心点位置）：模型导入时的位置，用一个三维点对象表示。默认定位点为（0,0,0），可自定义输入数值。 
      * 投影设置：支持投影设置和导入投影文件两种方式设置投影坐标系，详细操作步骤请参见“[设置投影坐标系](../../DataProcessing/Projection/PrjCoordSysDia)”。
  7. 单击“导入 ”按钮，打开3DXML文件。同时工作空间管理器中的数据源下新增一个3DXML数据结点。将导入的3DXML格式数据添加到场景中，如下图所示：          
  ![](img/Open3DXML.png)  


### 注意事项

  1. 小体量3DXML数据建议使用“打开3DXML”功能，因为该功能一次只能打开一个文件；大体量3DXML数据建议使用“导入3DXML“功能，因为该功能一次可以导入多个文件。

###  相关主题

 [打开BIM数据](OpenBIM)

 [导入RVT](ImportRVT)

 [导入IFC](./ImportIFC)



