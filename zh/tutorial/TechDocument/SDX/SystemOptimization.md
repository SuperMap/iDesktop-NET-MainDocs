---
id: SystemOptimization
title: GIS系统性能优化策略
---
### 一、硬件配置

  * **内存**

一般不要小于1G，但内存并非越大性能越优，需要合理的配置和管理，才能最大发挥内存给性能带来的优势。  
目前有一种能极大发挥大内存优势的方案，即建立内存数据库，速度会提升2个数量级，约100倍左右。  
性能优化的两大关键因素是：减少磁盘读写，即I/O；减少网络传输。相比于内存、CPU来说，硬盘增长的速度最缓慢，因此将数据存放到内存中是一个很好的方案。  
32位操作系统理论上最多只能使用4G的RAM，实际上最多只能达到3.7G或者更低（对于一般的配置，不加任何优化情况下，可能只能利用到1.7G）。  
对于4G以上RAM的服务器，建议安装64位操作系统和64位的Oracle。

  * **CPU**

建议尽量使用多核、可插多路主板的服务器，其性能肯定优于只安装了单核CPU的服务器。

  * **硬盘**

硬盘目前仍然是一个性能提升的瓶颈，比如IDE7200转与SCSI10000转，虽然只提高了20%的转速，但性能却差异相当大，会提升2～3倍之多。

目前不少服务器采用Raid（Redundant Array of Inexpensive
Disks）技术，即硬盘集群技术，该项技术会带来很多优势，比如高可用性，安全性，性能的提升。但Raid技术也需要合理使用，否则不会达到理想的效果。

Raid0，Raid1和Raid5，目前使用较多。另外，还有软Raid与硬Raid，后者成本较高，但性能优于软Raid，可查阅相关资料，了解更多关于磁盘集群技术的特性与使用。

  * **网络**

网络同样是一个影响性能的瓶颈，但也是性价比最高的一个环节，同时也最容易被忽视。GIS数据的特点决定了其比一般数据对网络的压力更大，在网络上投入相对高的成本是非常值得的。

  * **品牌机与兼容机的选择**

知名品牌机的优势是稳定性好，售后服务好，一旦出现问题，可以找厂商来帮助解决。但品牌机往往成本较高，尤其在服务器领域，比兼容机的成本高不止一倍以上。  
兼容机的优势是价格相对低廉，性能好，如果优化配置，性能往往会优于品牌机。其不足之处是，稳定性不能保证，一旦出现问题，不好解决。  
在品牌机与兼容机的选择上，应综合考量，政府部门等投入的大项目，一般推荐选择品牌机，一些小项目，在预算比较少的情况下，建议选择兼容机。

### 二、操作系统与数据库的选择

  * **操作系统**

主要衡量Windows，Linux与Solaris这三大操作系统。  
Windows
OS，其优势在于易用性强，不需很高级的系统管理员；但Windows的稳定性相对差一些，性能方面也远逊于Linux与Unix，在安全性方面更是存在很多自身的漏洞与后门，易被病毒和黑客侵袭。  
Linux OS，其优势在于操作系统是开源的，可节省项目成本，性能优异，安全性也远高于Windows，稳定性方面也不错。一般Linux＋兼容机
往往可媲美价格达几十万的品牌机。但Linux
OS易用性方面与Windows相比稍差，不过近几年大有超过Windows之势，Linux在界面上也逐渐向美观华丽走近，这在一定程度上对其性能会产生影响。若只安装Linux内核，无图形界面，用命令行的方式会取得最优的性能。此外，由于Linux操作系统大多是免费的，背后无知名大厂商提供技术支持保障，一旦系统出现问题，往往很棘手。  
Solaris OS，其优势在于稳定性、兼容性、性能俱佳，和品牌机搭配，如IBM Power
搭配AIX，Sun搭配Solaris，更加完整、优化。但此类操作系统往往很依赖个人的技术水平。且Solaris与品牌服务器的组合更适用于政府企业级的大项目。对于一些预算较低的中小型项目，也可以考虑选择Windows
Server。  
经测试，对于单客户端访问Windows，其性能会优于默认配置的Linux操作系统，其原因可能是默认配置的Linux并非最佳，一些不需要的服务和图形界面会占用资源。根据上文所述，采用无图形界面纯Linux内核的操作系统，性能肯定会优于Windows。在高并发访问上，并发数在20个以下时，Linux上的优势同样不明显，一般多于50个时，其优势会逐渐显现。

  * **数据库软件**

当前流行的数据库软件是Microsoft SQL
Server与Oracle。大多数用户对前者更熟悉，因其简单易用，但从长远角度，我们还是推荐您使用Oracle，一旦掌握了Oracle相关技术后，其可控制范围更广。

### 三、服务器的优化

以下为几个服务器优化的原则，供参考：

  * **只安装必要的选件**
  * **关闭界面美化选项**

如在Windows操作系统，系统属性里，有一个性能选项（Performance
Options），一般选择性能优先，而不是显示优先。如应用系统中不做三维图形显示，可将操作系统中的显示属性/Settings/Advanced/Troubleshoot中，硬件加速（Hardware
acceleration）调到None。

  * 设后台服务优先 

在“系统属性”的“性能选项”中，“高级”页面，调整Processor Scheduling为后台服务优先（Background services）。

  * **关闭不必要的服务和端口**

检查您操作系统中所有的服务和端口，对于一些用不到的服务和端口，可将其停止或关闭。

  * **尽量将数据库服务器与IS服务器分开**

多数情况下，针对数据库服务器和IS服务器的优化是有冲突的，而且若这两者在同一台设备上，也会产生资源争用的情形，IS服务器对内存的消耗也是非常大。另外，有一点值得注意，最好不要将这两类服务器分到两个子网中，即中间最好不要有路由器。

  * **其他高级优化**

除上述的一些优化建议措施之外，还有很多在服务器方面的高级优化方法，需要一些经验的积累和实际的案例支持。总之，大家需要形成一个概念，一台服务器并非在默认安装情况下就可用。

  * **关于杀毒软件**

一些杀毒软件在运行查毒时，非常消耗资源，服务器尽量不要安装杀毒软件，在一些优化措施已实施的情况下，比如关掉不必要的服务和端口，病毒一般也不会感染服务器。在Windows
Server 2003下若要安装杀毒软件，也尽量将查毒时间放在系统闲时；而在Solaris，AIX或Linux下，最好不要安装杀毒软件。

### 四、数据库的优化

  * **只安装必需的软件包**
  * **建库只选必需的选件**
  * **分配合适的内存**
  * **设置合理的参数**
  * **对数据文件进行合理的分配**

对访问量最大的表空间放在剩余空间最大最优的磁盘上。

  * **必要时使用RAC（Real Application Cluster）选项**

早期的“双机热备”，防止断线而设，一台备用，往往造成很大的闲置与空能耗。后期出现RAC概念，实际上是共享磁盘，与GRID网格计算关系密切。磁盘与机器节点之间通过光纤传输，每个节点都在运行，可以共享内存。其好处在于，极大地满足了高可用性，某个节点出现故障时，客户端几乎感觉不到与服务器断开，是真正的并行，建议企业使用RAC，但RAC的管理和安装比较复杂。

### 五、矢量数据的优化

  * **编码技术**

数据编码是一个压缩的概念，类似于ZIP，RAR等，数据量的减少可以大大提高磁盘读写和网络传输的效率，显著提高性能。若一个数据集原无编码，可以通过复制数据集的方式来指定，矢量数据集有多种编码方式，详见SuperMap
Objects的联机帮助中常量seEncodedType中所述。典型的有SDC和SWC两种。  
SWC，WORD编码类型，应用于矢量数据集（线、面类型）的一种编码方式，对点数据集不起作用。压缩比为4倍。精度损失为1/216。数据集中对象大小比较平均的情况下，推荐使用此种编码方式。  
SDC，DWORD编码类型，应用于矢量数据集（线、面类型）的一种编码方式，对点数据集不起作用。压缩比为2倍。精度损失为1/232，按照全球大小的对象估计，精度损失在毫米级。总结其优势：压缩速度快，损失小，原图和编码后的图对比浏览时，基本看不到差别。可以说SDC是几乎接近无损的一种编码方式，一般的数据推荐使用SDC。  
对一些在空间上相邻，有公共边的面状数据，用SDC编码完全没有问题，但用SWC，在放大很大时会有缝隙显现。而对一些在空间上零散分布的矢量数据，比如房地产的图斑，用SWC完全没有问题，几乎看不到精度损失。  
理论上，压缩之后的数据，占用空间更小，查询浏览速度更快。  
数据压缩的代价：压缩之后的数据不可逆，即不可以返回数据压缩之前的状态，此外在精度上有一定的损失，对查询和分析有影响，如果进行非常精确的查询和空间分析等，SWC会导致一些结果上的误差，但SDC不会有影响，其产生的精度损失在空间分析的容限范围之内。

  * **空间索引**

目前提供主要有四类空间索引：R树、四叉树、动态索引和图库索引。在实际的应用中，应根据具体的情况和各种索引的特点，选择合适的索引类型。  
简单概括各种索引的特点和不足:  

    * R树索引  
优点：通用情况下，查询性能最高。但对于一些特殊组织的数据，用图库索引＋本地缓存，速度是最快的。  
缺点：并发支持差，因此一般只用于独占的文件型数据源，而不常用于需要经常并发编辑的数据库型数据源；维护代价大，索引建立时间长。  
总之，对于静态数据，R树优势明显。

    * 四叉树索引  
优点：并发支持较好，建索引速度也较快。  
缺点：查询性能低于R树。  

    * 动态索引  
优点：并发支持好，建索引速度快，支持大数据量。可定制每一级格网的大小，不受数据集范围的限制。适合于数据库型数据源，在大数据量且只读情况下，性能比图库索引稍低。

    * 图库索引  
在下一小节中单独介绍。

  * **图库索引**

针对某些应用，图库索引是最快的一种，最适合规则分幅的数据，如按标准图幅编号的1：25万或1：10万的国家基本比例尺地形图。对于普通数据，如果采用图库索引，也会带来性能的提升。  
图库索引是针对数据库数据源的。根据范围或者某一字段对矢量数据集创建图库索引。用表示对象所属区域的字段来创建图库索引，或者按范围创建时，每一块里的记录数尽量平均，比如每块范围内有2000～20000个对象，范围不要太大或太小，这样的效果都很好。一般推荐范围：30×30即900个格子，这样的推荐值适合10万条记录的数据集。如果实际数据与此不同，则需要修改范围的长和宽。

  * **缓存**

图库索引结合本地文件缓存，对于静态数据，速度最快，效果最好。缓存可以通过数据集属性来设置，本地缓存的位置，则可以通过位于Bin目录下的配置文件supermap.xml来指定或修改。  
大数据量的数据在建立了图库索引，且经过第一次的全幅浏览（此时，服务器端的数据将全部被缓存到本地，通常第一次全幅速度稍慢，但也快于ArcSDE），在本地做过缓存之后，再次进行浏览、漫游的地图操作，将会明显感觉到速度的提升。  

### 六、栅格数据的优化

  * **将分幅影像拼接起来**

一般获得的卫星遥感影像，都是以景为单位的，在对这些分幅的影像数据进行操作之前，最好将其拼接起来，这样有利于充分发挥影像金字塔和数据编码的作用。

  * **编码**

DCT即离散余弦变换，是最适合于遥感影像的一种编码方式，压缩比一般为20倍。其他的编码方式，比如SPC、SGL和LZW都是针对Grid或者DEM数据集的，不过前两种已经不再维护，LZW是一种无损压缩，压缩比与具体的数据有关。

  * **影像金字塔**

针对影像数据，创建一系列分辨率逐渐降低的图层，当显示某一比例尺下某个范围内的影像时，自动调用最接近的那一层影像，以提高整体的浏览速度，对于大数据量的影像，非常有必要建立金字塔。

  * **SIT**

SIT即SuperMap Image Tower，是目前为止最快的一种影像文件格式。经过ECW与MrSID压缩的影像，与SIT相比，性能相差有十倍以上。  
SIT内部采用的是DCT编码，不含金字塔的情况下有20倍的压缩率，即数据量相比原始可减少20倍左右，一般影像都会建立金字塔，而存储金字塔也会占用一定的空间，因此影像数据集经压缩成SIT之后，往往要小于20倍。
影像数据集导出为SIT格式之后，还可以再导入，不过因为DCT是有损压缩，再导入后，与原始影像并不完全一样。

### 七、配图的优化

  * **设置合理的可见比例尺**

一幅地图中，当显示到某一比例尺时，并非所有的图层都有必要显示，因此根据实际需要，对各个图层设置合理的最大最小可见比例尺，将大大提高地图浏览的速度。

  * **简化数据**

如对数据进行重采样，或者对于显示区域比较大的数据，尽量采用小比例尺替代大比例尺。

  * **尽量使用简单的线型**

线型的设置也会对显示效率产生影响，如不必要，尽量使用简单的线型。

  * **尽量减少一幅地图所包含数据集的数目**

如果图层对应的数据集已经不存在，尽量将该图层Remove掉，地图中有不显示的图层，也建议Remove掉，空的图层仍会占用游标的资源。

  * **将不需要编辑的图层的可捕捉、可选择选项去掉**

默认情况下，图层的可捕捉和可选择选项是开启的，当鼠标在地图上移动时，仍会占用一定的资源，建议将不需要编辑图层的此类选项关闭。

  * **使用地图固定比例尺缓存**

需要使用iServer来发布的地图，可先使用iDesktop生成地图缓存，这样可以提高iServer客户端浏览地图的速度。

### 八、业务优化

  * **为业务字段建立索引**

查询语句的Where条件里，或者分组子句里要用到的字段，建议对其创建字段索引。

  * **统计时使用数据库的分组、关联等功能**
  * **数据库性能监控及分析工具**


