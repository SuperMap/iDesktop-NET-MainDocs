---
id: CreateDatasource
title: 新建数据源  
---  
### ![](../../img/read.gif)使用说明

支持新建数据源类型分文件型数据源、数据库型数据源、内存数据源三类。新建数据源的默认坐标系为 China
2000。有关各类型数据源的特点和适用场景，请参看[数据源及数据引擎类型](EngineType)。

提供三种方式新建数据源：

  * “文件”菜单中单击“新建”按钮提供选择新建数据源类型。
  * “开始”选项卡“数据源”组提供“文件”和“数据库”两个按钮以创建不同类型的数据源。
  * 在工作空间管理器中数据源节点单击右键，可在右键菜单中选择打开各类型数据源选项。 

### ![](../../img/read.gif)新建文件型数据源

以上述任一方式执行新建文件型数据源操作，选择“新建文件型数据”选项，在“新建文件型数据源”对话框中，设置新建数据源的保存路径、文件名即可创建相应类型的文件型数据源，该文件型数据源将保存到
*.udb 或*.udbx 文件中。

**![](../../img/read.gif)新建数据库型数据源**

目前支持新建 Oracle Plus、Oracle Spatial、SQL
Plus、PostgreSQL、DB2、KingBase、MySQL、BeyonDB、HighGoDB、KDB、SinoDB、PostGIS 和
MongoDB 等十余种数据库型数据源。

其中部分数据源类型的创建需要本地配置客户端。且创建不同数据库类型参数设置各有不同，参数描述、参数设置及注意事项同“打开数据库型数据源”，详细信息请参看”[打开数据库型数据源](OpenDatasource#1)”。

### 注意事项

  * 创建 PostGIS 数据库型数据源时，既可指定一个已有的 PostgreSQL 数据库名称，创建数据源；也可以指定一个新的数据库名称，创建数据源时，将先创建对应的 PostgreSQL 数据库，再创建数据源。一个 PostgreSQL 数据库只能创建一个 PostGIS 数据库型数据源。

### ![](../../img/read.gif)基于模板创建数据源

基于模板创建一个与模板数据源相同的数据源，即相当于复制一个模板数据源，其数据源中的数据集个数、名称、类型与模板数据源中的一致，只不过数据集只保留了相同的属性表结构，但是记录数为0
，即不包含任何对象空数据集。

目前应用程序提供了 **地理国情普查** 和 **基础地理信息地形要素分类** 两套模板，用户也可以指定工作空间中的其他数据源作为模板。
