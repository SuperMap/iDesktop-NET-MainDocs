---
id: DatasetManagement
title: 数据集管理  
---  
### ![](../../img/read.gif)复制数据集

将一个或者多个数据集复制到目标数据源中。当前有选中的数据集时，可以直接将选中的数据集添加复制窗口，快速实现数据集的复制。

同时支持以快捷键 Ctrl+C 和 Ctrl+V 的方式，即在工作空间管理器中选中待复制数据集进行 Ctrl+C（复制）， 再选中目标数据源进行
Ctrl+V（粘贴），完成对数据集进行复制、粘贴，将使数据源之间数据集的迁移更便捷简单。

**功能入口**

在工作空间管理器中，选中要进行复制的数据集，可以配合使用 Shift 键或者 Ctrl 键同时选中多个数据集，可通过以下两种方式进行复制操作：

  * 右键单击选中的数据集，在弹出的右键菜单中选择“复制数据集...”项，弹出“数据集复制”对话框。
  * 也可在工作空间管理器中，将待复制的数据集拖拽到需复制到的数据源结点处，弹出“复制数据集”提示框，单击“确定”按钮即可将将选中数据集复制到指定的数据源中。

**参数说明**

在“数据集复制”对话框中设置复制数据集的所必要的信息，对话框中的每条记录对应一个要复制的数据集的复制信息，包括：将数据集复制到的目标数据源、复制得到的新数据集的名称、复制得到的新数据集采用的编码类型。

“数据集复制”对话框中的每条记录对应一个要复制的数据集的复制信息，每一项的含义如下所示：

  * **源数据集：** 显示被复制的数据集的类型、名称和所在数据源的名称。
  * **源数据源：** 源数据集所在的数据源。
  * **目标数据源：** 目标数据源列用来指定被复制的数据集复制以后要存储在那个数据源中，目标数据源列中的每个单元格有一个下拉按钮，单击下拉按钮弹出下拉列表， 列表中列出了当前工作空间中打开的所有数据源，可以选择某个数据源来存放复制后的数据集。
  * **目标数据集：** 目标数据集列用来指定复制得到的新的数据集的名称，应用系统提供了一个默认的名称，用户可以对其进行修改，设置自己需要的名称。
  * **编码类型：** 编码类型列用来指定复制得到的新的数据集采用的编码类型，编码类型列中的每个单元格有一个下拉按钮，单击下拉按钮弹出下拉列表， 列表中列出了应用程序所支持的所有编码类型。数据集的编码类型就是数据集存储时的压缩编码方式，具体内容请参见：[数据集压缩编码方式](EncodeType)。
  * **字符集：** 设置复制后数据集的字符格式，默认与被复制数据集相同，用户可以选择其它字符集来改变 复制后数据集使用的字符集。有关支持的字符集及其介绍，请参见：[字符集列表](Charset)。
  * **SmID 不变：** 保持源数据集中 SmID 字段属性值不变。

 注意事项

  * 只有工作空间管理器中有选中的数据集，“数据集复制”按钮才可用。
  * 当执行一次操作复制多个数据集时，在选择多个数据集时，只能选中同一个数据源下的多个数据集，不能跨数据源选择多个数据集。
  * 将 UDB 数据源中的数据集复制到 Oracle 或 SQL Server 数据源中时，若数据集中有文本型字段，为了保证 UDB 中文本型字段中的多国语言可正常存储，数据集中的文本型字段会转换为宽字符型字段。

### ![](../../img/read.gif)删除数据集

“删除”按钮，用来删除指定的数据集。可以同时删除选中的多个数据集。

**功能入口**

在工作空间管理器中，选中要删除的数据集，可以配合使用 Shift 键或者 Ctrl 键同时选中多个数据集。

  * 右键单击选中的数据集，在弹出的右键菜单中选择“删除数据集”项，弹出“删除数据集”提示对话框。 
  * 同时支持以快捷键 Delete 键, 快速执行删除数据集操作。

 注意事项

  * 只有工作空间管理器中有选中的数据集时，“删除”按钮才可用。
  * 当选择多个矢量数据集时，只能选择同一个数据源下的多个数据集，不能跨数据源选择多个数据集。

### ![](../../img/read.gif)关闭数据集

“关闭数据集”命令，用来关闭当前工作空间中已打开的一个或多个数据集。

**功能入口**

右键单击选中工作空间管理器中的一个（或多个）需要关闭的数据集结点，在弹出右键菜单中选择“关闭数据集”命令。

在对矢量数据集创建空间索引时，必须先关闭数据集后，才能进行相关操作。

### ![](../../img/read.gif)数据集排序

“数据集排序”命令，用来对该数据源中的数据集进行排序。

为了便于使用，可以对数据源中的数据集进行排序，实质是对工作空间管理器中的数据源结点下的所有数据集所在的结点进行排序。

**功能入口**

右键点击选中工作空间管理器中的一个数据源结点。

数据集的排序方式有四种：

  * **按照名称排序：** 在当前数据源对应的结点下，所有数据集所在的结点将根据其结点显示的名称进行重新排序。
  * **按照类型排序：** 在当前数据源对应的结点下，所有数据集所在的结点将根据其对应的数据集的类型进行排序。
  * **按照创建顺序排序：** 在当前数据源对应的结点下，所有数据集所在的结点将根据其对应的数据集被创建的先后次序进行排序。
  * **按照对象个数顺序排序：** 在当前数据源对应的结点下，所有数据集所在的结点将根据其对应的数据集中的对象个数并分类型进行升序排序。

注意事项

可以在工作空间管理器中先同时选中多个数据集，然后再右键单击鼠标，在弹出的右键菜单（同样是数据源结点的右键菜单）中选择“数据集排序”下的某种排序方式，即可分别对所选中的数据源下的数据集进行相应方式的排序。

### ![](../../img/read.gif)重命名数据集

“重命名”命令，用来修改选中的数据集的名称。

**功能入口**

  * 右键单击选中工作空间管理器中的一个数据集结点，在弹出右键菜单中选择“重命名”命令。
  * 选中要修改名称的数据集，在键盘上按住 **F2** 键，数据集结点的显示名称变为可编辑状态，直接编辑即可。

重命名数据集前先将该数据集关闭，如若该图层处于打开状态，系统将弹出提示框提示必须将数据集关闭之后才能继续处理。

重命名后自动修改关联地图中的图层关联的数据集名称，减少用户手动修改地图的工作量。

### ![](../../img/read.gif)刷新数据集

多端并发对同一个数据集进行编辑、修改时，可通过 **刷新** 功能同步数据集内容。

**功能入口** ：在工作空间管理器中数据集结点处单击右键，在右键菜单中选择“刷新”命令。

### ![](../../img/read.gif)数据集另存为

**数据集另存为** 支持将选中的一个或多个数据集，另存到指定路径下新建文件型数据源中。在另存数据集的同时，新建数据源，简化了操作步骤。

**功能入口**

**工作空间管理器->数据集右键菜单->数据集另存为...**

**参数说明**

  * 目标数据集：支持显示和设置目标数据集名称。
  * SmID 不变：设置另存的数据集是否保持数据集的 SmID 不变，若选择否，则 SmID 会重新排序。
