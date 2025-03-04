---
id: SettingLayout
title: 布局属性
---
在“ **布局** ”选项卡的“ **布局属性** ”功能控件，打开的“布局属性”界面中组织了在布局窗口进行各种布局设置的功能。

### ![](../img/read.gif)布局网格

“ **布局属性** ”界面中，包含了网格相关的设置，包括：是否显示网格、是否支持网格捕捉以及网格间隔的设置等。

**显示网格** ：用于获取和设置网格的显示效果。

  * 勾选该复选框，则当前布局页面中显示网格。
  * 若不勾选该复选框，则不显示网格。

**网格捕捉** ：用于获取和设置是否支持网格的自动捕捉。

  * 勾选该复选框，则当前布局页面支持网格自动捕捉。当在布局页面绘制地图元素时，地图元素可以迅速定位到网格交点的精确位置。
  * 若不勾选该复选框，则不支持网格自动捕捉。

**网格间隔设置**

  * **水平间隔：** “水平间隔:”右侧的数字显示框用于显示和设置布局页面中网格的水平间隔大小。单位：0.1毫米。
  * **垂直间隔：** “垂直间隔:”右侧的数字显示框用于显示和设置布局页面中网格的垂直间隔大小。单位：0.1毫米。

### ![](../img/read.gif)布局标尺线

布局页面中与标尺线相关的设置，包括：是否显示刻度尺、标尺线，以及标尺线的管理等。

**显示刻度尺** ：用于获取和设置布局窗口中的刻度尺是否显示。

  * 勾选该复选框，则在布局窗口的左边和顶部显示刻度尺，便于用户定位、设置大小和对齐布局元素。 
  * 若不勾选该复选框，则不显示布局窗口中的刻度尺。

**显示标尺线** ：用于获取和设置布局窗口中的标尺线是否显示。

  * 勾选该复选框，则显示在布局窗口中已创建的标尺线，便于用户标识精确的位置，精确确定布局对象的放置或对齐布局对象 。 
  * 若不勾选该复选框，则不显示布局窗口中已创建的标尺线。

**标尺线管理** ：用于管理当前布局窗口中已经存在的标尺线，也可以对当前布局窗口增加或删除标尺线。

  1. 单击“标尺”组的“标尺线管理”按钮，弹出“标尺线管理”对话框。
  2. 修改标尺线属性：该窗口中显示了当前布局窗口中已经创建的标尺线，用户可以修改已存在标尺线的位置（具体数值可从标尺线上读取），或类型（水平/垂直），修改已存在的标尺线。
  3. 创建标尺线： 
  * 用户可在该窗口中上方工具区单击“添加”按钮创建一个标尺线，也可以在窗口的任意位置单击鼠标右键，选择右键菜单的“添加”项，即可添加一个系统默认的标尺线（标尺线位置：100，类型：水平方向）。用户可修改默认生成的标尺线的位置和类型，获得符合需求的标尺线。
  * 用户也可直接在该窗口中，所有标尺线列表的下一行中直接在“位置”和“类型”对应项中，输入待创建标尺线的相应属性，即可新建标尺线。
  * 用户也可以直接从布局窗口左边和顶部的标尺中拖出垂直和水平的标尺线，创建的标尺线都会在“标尺线管理”窗口中进行统一管理。
  4. 删除标尺线：在“标尺线管理”窗口中选中要删除的一条或多条标尺线，单击窗口上方的“删除”按钮，或者单击鼠标右键，在右键菜单中选择“删除”项，即可删除所选标尺线。
  5. 关闭“标尺线管理”窗口：完成窗口中的各项操作后，单击“确定”按钮，即可保存设置，关闭该窗口。或者直接单击“关闭”按钮，也可以退出当前窗口。

### ![](../img/read.gif)滚动条设置

“ **布局属性** ”界面中，包含了设置和控制当前布局窗口显示效果的功能控件。

**水平滚动条** ：用于控制布局窗口水平滚动条的显示/隐藏效果。

勾选该复选框，则在浏览布局的过程中，显示布局窗口的水平滚动条，用户可以使用水平滚动条在水平方向平移浏览布局。

**垂直滚动条** ：用于控制布局窗口水平滚动条的显示/隐藏效果。

勾选该复选框，则在浏览布局的过程中，显示布局窗口的垂直滚动条，用户可以使用垂直滚动条在垂直方向平移浏览布局。

### ![](../img/read.gif)显示比例尺

“ **布局属性** ”界面中，包含了设置和控制当前布局窗口显示效果的功能控件。

  * **最小显示比例**

布局窗口的最小显示比例是指当布局窗口缩小到整幅图大小的某一设置比例值时，布局窗口不再缩小显示。

“最小显示比例:”标签右侧组合框用于设置当前布局窗口的最小显示比例。用户可以点击该组合框的下拉按钮，在弹出的下拉列表中，选择一个比例数值，或者在文本框中直接输入一个数值，作为当前布局窗口的最小显示比例。系统默认的布局窗口缩放的最小比例是10%，布局最小显示比例可设置的最小值为1%。

  * **最大显示比例**

布局窗口的最大显示比例是指当布局窗口放大到整幅图大小的某一设置比例值时，布局窗口不再放大显示。

“最大显示比例:”标签右侧组合框用于设置当前布局窗口最大显示比例。用户可以点击该组合框的下拉按钮，在弹出的下拉列表中，选择一个比例数值，或者在文本框中直接输入一个数值，作为当前布局窗口的最大显示比例。系统默认的布局窗口缩放的最大比例是400%，布局最大显示比例可设置的最大值为1000%。

### ![](../img/read.gif)布局背景

“ **布局属性** ”界面中“ **背景色** ”标签选项用于设置布局窗口和纸张页面的背景色。

**操作步骤**

  1. 单击“背景色”右侧的下拉按钮，弹出颜色面板。
  2. 用户可以在颜色面板中选取默认颜色设为布局窗口和纸张页面的背景颜色，或点击颜色面板底部的 “颜色库”按钮，获取更多自定义颜色。 

**注意事项** ：对布局窗口的背景色设置会作用于布局窗口和纸张的背景区域，会随着打印输出。

### ![](../img/read.gif)控制布局对象显示效果

“ **布局属性** ”界面中，包含了设置和控制当前布局窗口文本对象压盖显示、文本反走样、线型反走样等显示效果的功能控件。

**文本对象压盖显示**

当布局窗口中的文本对象较多时，可能会出现相互压盖现象。“文本对象压盖显示”复选框用于控制是否显示布局窗口中压盖的文本对象，默认为不勾选该复选框。若不勾选“文本对象压盖显示”复选框，则系统会根据文本对象在布局窗口中的压盖情况，自动过滤掉后输入的文本对象，从而避免压盖现象出现。若勾选“文本对象压盖显示”复选框，则当布局窗口中文本对象出现压盖现象时，不进行过滤，显示全部文本对象。

**文本对象反走样**

“文本对象压盖显示”复选框用于设置布局窗口中文本显示笔画平滑，消除锯齿的效果。

**线型反走样**

线型反走样是指使布局窗口中矢量数据集的线条平滑，消除锯齿的显示效果。

### ![](../img/read.gif)偏移设置

“ **布局** ”选项卡中“ **布局设置** ”组的“ **偏移设置** ”按钮用于设置当前布局浏览的偏移效果。

**操作步骤**

  1. 单击“偏移设置”按钮，或者单击“布局设置”组的组对话框按钮，弹出“布局设置”对话框。
  2. “布局设置”对话框的“偏移设置”选项卡的偏移设置区域，提供了显示并设置当前布局浏览偏移效果的两种方式。（默认为中心点方式）
  * **中心点：** 以X、Y坐标值显示或设置当前布局窗口的中心点坐标值。用户可勾选“中心点”复选框，“X坐标:”和“Y坐标:”标签右侧的数字显示框为可用状态，显示了当前布局窗口的中心点的坐标值，用户可以在这两个数字显示框中重新输入数据，确定新的布局窗口中心点。单位为像素。
  * **偏移量：** 以当前布局窗口中心点为基准，通过横向或纵向的偏移量设置布局窗口的中心点。用户可勾选“偏移量”复选框，“横向:”和“纵向:”标签右侧的数字显示框为可用状态，初始显示都为0，即无偏移。用户可以在这两个数字显示框中输入横向或纵向偏移值，确定新的布局窗口中心点。单位为像素。
  3. 用户可在“布局设置”对话框的“偏移设置”选项卡下方的预览区域实时预览布局窗口偏移的效果。点击“确认”按钮后，当前布局窗口即可根据设置实时应用布局窗口的偏移设置。
