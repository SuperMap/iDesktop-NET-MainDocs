---
id: 10-2FindLocationDia
title: 选址分区
---
### ![](../img/read.gif) 使用说明

选址分区，从多个候选位置中按照指定的参数选择最佳位置。选址分区分析为服务设施的选址提供了参考。有关选址分区的更多介绍内容，请参见[选址分区概述](10-1FindLocation)页面。

### ![](../img/read.gif) 操作步骤

1. 打开需要进行分析的网络数据集。
2. 在“ **交通分析** ”选项卡的“ **路网分析** ”组中，选中“ **环境设置** ”复选框，弹出“ **环境设置** ”窗口。在此窗口中设置网络分析的基本参数（如权重字段、结点/弧段标识字段等）、分析结果参数以及追踪分析的参数（仅在进行追踪分析时需要进行设置）。关于环境设置窗口的介绍，请参见[网络分析环境设置窗口](NetAnalystEnvironmentWIN)。
3. 新建选址分区分析的实例。在“ **交通分析** ”选项卡的“ **路网分析** ”组中，单击gallery下拉按钮，在弹出的下拉框中选择“ **选址分区** ”项。成功创建后，会自动弹出实例管理窗口。且地图窗口中的鼠标状态变为绘制状态，用来添加中心点。
4. 在当前网络图层中添加中心点。中心点又叫资源中心供给点，是提供资源和服务的设施点。添加中心点有两种方式，一种是在网络图层中通过鼠标绘制的方式完成中心点的添加；另外一种是在中心点管理窗口中，将点数据集导入作为中心点。 
  * **鼠标添加中心点**：在实例管理窗口的工具条中，单击“鼠标添加”按钮，此时地图窗口中鼠标变为绘制状态，可在地图窗口中合适的位置单击鼠标添加站点。每添加一次中心点，该点会自动添加到实例管理窗口的中心点信息中。添加完成后，单击鼠标右键结束操作。<br/>**注意** ：需要设置合适的结点捕捉容限。如果鼠标点击位置超出结点捕捉容限，则可能导致站点添加失败。
    * **导入中心点**<br/>将当前工作空间中的点数据集导入作为中心点。在“实例管理”窗口中的目录树中，选择“中心点”结点，在右键菜单中选择“中心点管理”项，打开“中心点管理”窗口。在该对话框中通过导入命令，导入中心点，并进行参数设置。关于“中心点管理”窗口的介绍内容，请参见[中心点管理](CentersManagement)窗口。<br/>注意：若需要删除某个中心点，可选中该中心点，在弹出的右键菜单中选择“移除”或者选中要删除的中心点按住 Delete 键即可。
5. 在网络分析实例管理窗口中，单击“参数设置”按钮，弹出“ **选址分区参数设置** ”，对选址分区参数进行设置。 
  * **参数设置**
    * **期望中心点数**：用户希望的分析结果中给出的最优的选址位置个数，做到最大范围的覆盖。当存在固定中心点时，期望中心点数必须不大于固定中心点数目。注意：此种模式下需要保证网络是全连通的。
    * **最少中心点模式**：选中该复选框，表示使用最少中心点模式进行分析，此时期望中心点数目设置无效，应用程序会计算最少的中心数目，以覆盖更多的区域，也就是说，使用最少的中心点对全网络做到覆盖，不能全覆盖就会分析失败。<br/>分析失败可能的原因有两方面：一方面，如果网络不是全连通的（例如存在孤立点或者孤岛情况），就会分析失败。可以通过流向来检查网络是否全连通：任意选择一个点作为源点构建流向，流向为3的就是不连通的位置；另一方面，可选中心点要够多，权值（服务范围）要足够大，保证能对全网络全部覆盖。
    * **从中心点开始分配** ：选中该复选框，表示在选址分区是从中心点到请求点进行分配，否则表示从相反方向进行分配。
  * **结果设置**
    * **数据源** ：选择选址分区结果要保存的数据源。
    * **分配点数据集**：选中该对话框，会将分析得到的分配中心点保存为点数据集，并为其命名。该属性表数据集中保存了新的中心点的信息，包括中心点的类型、需求量、权重信息等。下表1对分配点中心属性表中的字段进行了说明。
    - **需求点数据集**：选中该复选框，将分析得到的需求点保存为属性表数据集，并为其命名。该属性表中会存储所有需求点的信息，一般会包含当前网络图层中的所有网络结点。下表2对需求点属性表中的字段分别进行了说明：

**表1：分配点中心字段说明**

字段名称 | 说明  
---|---  
**CenterID** | 分配点结点标识。  
**SupplyCenterType** | 分配点类型，1表示可选中心点；2表示固定中心点。  
**DemandCount** | 分配点的资源量。  
**TotalWeights** | 总花费，表示该分配中心点到其所有服务的结点花费之和。  
**AverageWeight** | 平均花费，表示分配中心点到其所有服务的每个结点的平均花费。  
**MaxWeight** | 分配中心点的最大阻力值。  
  
**表2：需求点字段说明**

字段名称 | 说明  
---|---  
**CenterID** | 需求点结点标识，值为-1时，表示该点不是需求点。  
**Cost** | 需求点到中心点的耗费路径，当值为-1时，表示该点不是需求点。  
  
6.参数设置完毕后，单击“确定”按钮，退出选址分区参数设置对话框。

7.有参数设置完毕后，在“ **路网分析** ”组中或者实例管理窗口中“ **执行** ”按钮，进行分析。分析结果会即时显示在地图窗口中。分析结果可以保存为数据集，以便在其他地方使用。 

### 注意事项

* 选址中心点类型必须为可选中心点或固定中心，否则分析失败。
* 用于选址分区的中心点必须位于网络中的结点上，否则没有办法添加到网络图层中。
* 如果在网络分析图层中设置了障碍点，则障碍点信息在网络分析管理窗口中显示，并可以在该窗口中对障碍点进行管理。关于如何添加障碍点请参阅[障碍点管理](BarrierManagement)。

### 相关主题

[选址分区概述](10-1FindLocation)