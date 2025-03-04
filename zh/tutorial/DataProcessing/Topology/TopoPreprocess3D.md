---
id: TopoPreprocess3D
title: 三维拓扑预处理  
---  
### ![](../../img/read.gif)使用说明




在使用拓扑数据集对关联数据集进行拓扑检查前，需要对待拓扑检查数据进行拓扑预处理操作，通过预处理将那些在容限范围内的问题数据进行调整。不进行拓扑预处理，可能会导致拓扑检查的结果出现错误。三维拓扑预处理提供了节点捕捉处理方式，目前该功能只支持三维线数据集。



### ![](../../img/read.gif) 功能入口



在“ **数据** ”选项卡的“ **拓扑** ”组中，单击“ **拓扑预处理**”下拉按钮，选择“三维拓扑预处理”项。

### ![](../../img/read.gif) 参数说明

* **容限值**
：用于进行拓扑预处理的容限值，它是一个距离值，指的是在这个值的范围内，所有的节点或（和）线被认为是重合的、同一的。例如，若一个线对象的节点与另一个线对象的节点距离在容限范围内，则认为这两个节点重合；若一个线对象的节点与一个点对象的距离在容限范围内，则认为点在线上。
节点或（和）线之间的距离小于容限值时，将进行拓扑预处理。



容限默认值与数据集的坐标系有关，具体说明请参见[容限说明](../Tolerance)。



* **节点捕捉**：将容限范围内的节点捕捉在一起（即将捕捉在一起的节点修改为同样的二维坐标），其中“节点”的含义是指点对象以及线对象和面对象的所有控制节点。




勾选“节点捕捉”复选框后，可在“参考数据集”处选择一个数据集，以该数据集的节点位置为参照进行捕捉。在捕捉后会将线对象和面对象在容限范围内的临近点去除，节点捕捉处理效果如下图所示。



![](img/TopoPreprocess1.png) | ![](img/TopoPreprocess2.png)  
---|---  
![](img/TopoPreprocess3.png) | ![](img/TopoPreprocess4.png)  
拓扑预处理前 | 拓扑预处理后  





### 注意事项



三维拓扑预处理会改变源数据集中的空间位置，用户若不想修改原始数据，请在拓扑预处理之前进行数据的备份工作。



