---
id: SmartStyleTransfer
title: 风格迁移
---
### ![](../../img/read.gif)功能说明

风格迁移功能，是在保留目标图片内容的基础上，将图片风格迁移到到目标图片上的技术。同时，支持调整填充、轮廓、线、标签的色相、亮度、对比度、饱和度等，实现如“PS”般快速美化地图。

**应用场景**

* 适用于当用户已经配好了一幅地图，但是想要换一种显示风格应用到其他场景中，例如用户有一幅亮色系的地图，但是需要适配地图大屏展示为暗色系的地图，或者为适配某个会场风格需要改变地图配色风格。
* 适用于地图个性化展示，例如水墨画风格，古建筑风格等个性化展示。

**功能特点**

* 预定义暗色系、彩色系、水墨画等多套风格图片，同时支持用户导入自定义图片。
* **风格迁移设置** ：在读取图片颜色时，支持设置图片的压缩模式，以及读取颜色数量，使配色能更精细、更贴近用户需求。
* **颜色调整** ：支持对渲染后的文本、线、面图层进行色相、亮度、对比度、饱和度及柔化/锐化等色彩调整，以达到更理想的配图效果。同时支持彩色、灰度、黑白及反色等调整。
* **撤销/重做** ：支持通过“ **撤销** ”/“ **重做** ”按钮对地图迁移操作进行撤销和回退，同时支持通过快捷键 Ctrl+Z /Ctrl+Y 实现撤销和回退操作。

### ![](../../img/read.gif)风格迁移操作说明

用户可通过选择程序提供的模板图片进行迁移，目前预定义了暗色系、彩色系、水墨画等多套风格图片，同时支持用户导入自定义图片。

1. 在地图窗口打开已配置好的地图。
2. **使用模板图片** ：在 **AI配图** 选项卡-> **风格迁移** 组的 Gallery 控件中，单击任一图片，即可基于当前图片渲染地图，地图窗口中显示风格迁移后的地图。 
3. **使用自定义图片** ：在 **AI配图** 选项卡-> **风格迁移** 组的 Gallery 控件中->单击“自定义”按钮，上传自定义图片，即可基于选择图片渲染当前地图，地图窗口中显示风格迁移后的地图。
4. 在地图窗口左下角弹出图片预览对话框，可单击"选择"按钮，更改自定义图片；如若关闭了预览窗口，可在 **风格迁移设置** 对话框中勾选“ **显示预览窗口** ”复选框，开启图片预览窗口。

### ![](../../img/read.gif)风格迁移设置

在指定图片样式前，支持设置提取颜色时图片的压缩模式和颜色数，以提高图片的处理性能。

1.在 **AI配图** 选项卡-> **风格迁移** 组的 Gallery 控件中，单击“迁移设置”按钮，弹出“风格迁移设置”对话框。  

2.**压缩模式** ：提供4种图片的压缩模式，以提升读取图片速度，提升图片处理性能。有关插值的详细描述请参看：[栅格重采样方法介绍](../../DataProcessing/Registration/resamplemethod)。  

* **无** ：不对图像进行压缩，使用图片的原始长宽比。
* **抗锯齿** ：基于采样的抗锯齿算法，能够很好的处理图片中图物边缘出现渲染失真和锯齿的问题，处理后的图像品质最高（损失最小），但相较于其他模式的处理比较耗费资源性能较低。
* **最近邻插值** ：基于K近邻算法，是将目标图像各点的像素值设为源图像中与其最近的点，优点是处理简单、速度快性能快，但相较于其他模式处理后图片的质量较低。
* **线性插值** ：使用简单的线性插值重新采样图像，输出质量低于三次样条插值，但性能较好。
* **三次样条插值** ：该算法使用三次插值来重新采样图像。 输出质量低于抗锯齿，但性能较高于抗锯齿。  

3.**颜色数** ：支持设置提取图片的颜色数，程序默认颜色数范围为50~200，用户可根据当前地图配色，指定合理颜色数。

### ![](../../img/read.gif)颜色调整

支持调整色相、亮度、对比度、饱和度、填充柔化、填充锐化，对渲染后的文本、线、面图层进行色彩调整，以达到更理想的配图效果。同时支持彩色、灰度、黑白、反色等操作进行颜色调整。

* 单击 **AI 配图** 选项卡-> **颜色调整** 组中“ **色相** ”、“ **亮度** ”、“ **对比度** ”、“ **饱和度** ”及“ **柔化/锐化** ”任一按钮，将弹出颜色调整面板，可通过滑块及输入精确数值的方式调整当前地图亮度、对比度、饱和度和色相，对所有图层生效：
* 若需要单独对地图中填充、轮廓、线及标注图层进行调整，可单击输入数值框右侧的“ **＋** ”按钮，弹出分类颜色调整面板，可通过滑块及输入精确数值的方式，对填充、轮廓、线及标注图层的色相、亮度、对比度、饱和度进行调整。

**参数描述** ：

* **色相** ：调整当前地图颜色的色相；色相是色彩的首要特征，任何黑白灰以外的颜色都有色相。
* **亮度** ：调整当前地图颜色的明亮程度。
* **对比度** ：调整当前地图颜色的对比度。
* **饱和度** ：调整当前地图颜色的饱和度，是色彩的纯度，纯度越高，表现越鲜明，纯度较低，表现则较黯淡。
* **柔化/锐化** ：调整填充锐化的数值对地图进行锐化或羽化，正值为锐化，负值为柔化，增加锐化会降低柔和度，反之亦然。
* **彩色** ：将灰色风格的地图改为彩色风格。
* **灰度** ：将地图风格修改为灰色风格。
* **黑白** ：将地图改为黑白风格。
* **反色** ：反转地图的颜色。

### ![](../../img/read.gif)应用实例

现有一幅珠江三角洲政区地图，政府在对外宣传时分为两个专题：珠江三角洲历史发展以及区域环境保护，为适应两种不同的主题，可通过选择古地图和绿色植被两种不同的图片风格，将地图风格适配为对应主题，得到如下图所示的结果：

![](img/StyleTransferexampleresult1.png) |![](img/StyleTransferexampleresult2.png)  
---|---  
历史风格地图 | 环保风格地图  


