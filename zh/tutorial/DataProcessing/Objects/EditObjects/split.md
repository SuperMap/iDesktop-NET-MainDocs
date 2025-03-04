---
id: split
title: 打断  
---  
打断功能用来将线对象打断为新的对象。
### 使用说明

* 打断功能用来在鼠标点击的任意位置打断线对象。
* 适用于打断的图层可以是线图层的对象或者 CAD 图层的线对象。同时要求要打断的对象所在的图层可编辑。
* 在进行打断操作时，可以开启捕捉功能，方便快速、精确的定位到想要打断的点，例如在打断线对象的交叉处时，可以开启捕捉功能。
* 若选择的断点是多个对象的交点，则会弹出“选择打断对象”对话框，支持选择参与打断的对象，并且地图中会高亮显示列表中的选中对象。
* 封闭对象打断的说明。
在 SuperMap 中，封闭的线对象被看成是起点和终点重合在一起的对象。而这个重合的起点和终点，我们称之为端点。
对于封闭线对象，例如圆、矩形等，执行单次打断操作后，系统会自动将封闭对象的端点同时打断，从而生成两个线对象。

* 打断操作后，新生成的两个线对象以不同的颜色临时显示出来，以示区别。
### 操作步骤
1. 在“ **对象操作** ”选项卡的“ **对象编辑** ”组的 Gallery 控件中，单击“ **打断** ”按钮，执行打断操作。
2. 地图窗口中鼠标提示：请点击要打断的线段。在要打断对象的相应位置上点击一下，即可打断该对象。新生成的两个线对象以不同的颜色（红色和蓝色）临时显示出来，以示区别。
  
  该操作可以在选中的线对象上连续的打断。在完成操作后，原来的线对象被删除，新生成多（打断次数＋1）个线对象，它们的系统字段由系统赋值，非系统字段属性保留原来线对象的非系统字段属性。



3. 执行打断对象操作时，若选择的断点是多个对象的交点，支持设置参与打断的对象，在“选择打断对象”对话框中，可勾选列表中的打断对象，选中的对象会在地图中会高亮显示。

### 注意事项



当打断对象为参数对象时，如圆弧、三点弧、样条曲线等，打断功能将失效。CAD 数据集中存在参数化对象。




