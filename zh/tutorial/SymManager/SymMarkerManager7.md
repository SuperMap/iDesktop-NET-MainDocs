---
id: SymMarkerManager7
title: 新建点符号
---
通过新建一个点符号库，可以扩充点符号库中的点符号，新建点符号，既可以新建一个二维点符号，又可以新建一个三维点符号。二维点符号用来符号化地图中的点对象；三维点符号用来符号化场景中的点对象，同时也可符号化地图中的点对象。下面具体介绍如何完成新建点符号的过程。

## 新建一个二维点符号

1. 通过符号分组结构树，定位新建的点符号所在的符号分组，新建的符号默认添加到符号选择器中当前显示的符号路径下；
2. 在符号选择器中，单击“编辑”按钮，选择“新建符号”->“新建二维点符号”，此时将打开点符号编辑器，在点符号编辑器中可以制作新的点符号； 

这里，必须指定新符号编号、符号名称，同时，新的符号必须包含至少一个笔划，即新建的符号不能为空，这样，在单击点符号编辑器中的“确定”按钮，才可以成功创建一个新的点符号，新建的点符号将出现在点符号选择器中的当前点符号列表中。

3. 设置新的点符号的属性信息，必须指定的符号属性为：符号编号和符号名称； 
    * 符号编号：符号编号用来在符号库中唯一标识该符号，在同一个符号库中，新建的符号编号不能同符号库中已有的符号的编号相同。
    * 符号名称：符号在符号库中的显示名称，在同一个符号库中，符号的名称可以同名。
    * 符号原点：用来设置符号的原点在符号编辑区域的位置，另外，符号的原点也是符号的锚点，在对点对象符号化时，描点的位置将位于点对象的坐标点上。
    * 默认大小：设置点符号的默认大小，当用户通过点符号选择器设置点符号的大小时，如果指定的大小值为0时，点符号的大小将取默认大小的数值。点符号默认大小的数值范围为0到25.5之间，单位为：毫米。
4. 在符号编辑区域，绘制新的点符号所包含的图形内容，有关点符号的制作这里不作详细介绍，这里仅绘制一个点几何对象； 

具体操作：单击绘制点几何对象的按钮，然后在符号编辑区域的任意位置单击鼠标，即可在新的点符号中添加一个点几何对象。

5. 设置好符号的属性信息，并且绘制了至少一个几何对象（笔划）点符号的制作，单击符号编辑器中的“确定”按钮，完成点符号的新建，新建的点符号将出现在当前点符号库中。 

新建的点符号可以再次编辑，进一步完善点符号，只需在点符号选择器中，选中该点符号，然后单击“编辑”按钮，即可在点符号编辑器中打开该点符号，进行进一步的编辑操作。

在符号库中新建的点符号，最终要保存到符号库中，还需要通过以下途径进行：  

* 如果当前符号库是工作空间的资源集合中的点符号库，可以通过保存该工作空间，将新建的符号保存到点符号库中；
* 通过将点符号选择器中当前的点符号库导出为点符号库文件，可以将新建的点符号保存到点符号库文件中，后续，可以通过加载该点符号库文件获得新建的点符号。

## 新建一个三维点符号

1. 通过符号分组结构树，定位新建的三维点符号所在的符号分组，新建的符号默认添加到符号选择器中当前显示的符号路径下；
2. 在符号选择器中，单击“编辑”按钮，选择“新建符号”->“新建三维符号”； 
3. 打开三维点符号编辑器，如下（左图）所示，在三维点符号编辑器中，可以设置三维点符号对应的三维模型、设置三维模型的显示风格等。单击三维点符号编辑器中的“设置模型”按钮，弹出“打开”对话框，选择一个模型文件（*.sgm 或 3ds 文件），并打开。 

三维点符号的创建过程是，首先，制作要作为三维点符号的三维模型，可支持作为三维点符号的三维模型包括 SGM 模型和 3D Max 模型，分别以 *.sgm 和
3ds 文件存储；然后，通过点符号库的新建三维符号的功能，将三维模型加载到符号库中作为一个三维点符号。

**注意：** 在导入三维模型时，所导入的 3ds 文件的大小不能超过 60KB 大小。

4. 选择模型文件并打开后，在三维点符号编辑器中，可以预览所选择的模型文件中的三维模型，同时，可以设置新建的三维点符号的属性信息，以及对该三维模型进行风格的调整已制作满足需要的三维模型。 

这里，必须指定新建的三维点符号的符号编号、符号名称，这样，在单击三维点符号编辑器中的“确定”按钮，才可以成功创建一个新的三维符号，新建的三维符号将出现在点符号选择器中的当前点符号列表中。

* 符号编号：符号编号用来在符号库中唯一标识该符号，在同一个符号库中，新建的符号编号不能同符号库中已有的符号的编号相同。
* 符号名称：符号在符号库中的显示名称，在同一个符号库中，符号的名称可以同名。
* 缩放比例：用来对三维模型进行 X、Y、Z 三个坐标方向拉伸。在设置数值时，既可以直接在数值框中输入数值；也可以单击右侧的箭头弹出滑块，通过调节滑块的位置，或者单击放大或缩小按钮的方式，设置数值。
* 旋转角度：用来对三维模型进行 X、Y、Z 三个坐标方向的旋转。在设置数值时，既可以直接在数值框中输入数值；也可以单击右侧的箭头弹出滑块，通过调节滑块的位置，或者单击放大或缩小按钮的方式，设置数值。
* 快照设置：用来对预览区所显示的三维模型建立一个快照，即获取一个图片，快照的效果将显示在快照设置区域。快照的作用是： 

新建的三维点符号在点符号选择器的符号列表中所显示的点符号缩略图，即为设置的快照；

如果在对地图中的点对象进行符号化时，选中了三维点符号作为点符号风格，那么在地图上所显示的点符号即为所设置的快照。

5. 在三维点符号编辑器中完成必要的设置后，单击编辑器上的“确定”按钮，所创建的三维点符号就添加到当前点符号选择器中的点符号列表中。



三维点符号编辑器的预览区，提供了丰富的鼠标和键盘操作，从不同角度、不同方位对三维模型进行预览，有关三维点符号编辑器的预览操作，请参见：[三维线型符号编辑器界面简介](SymLine3DEditor2)
中的 **“预览区的浏览操作”** 内容。

