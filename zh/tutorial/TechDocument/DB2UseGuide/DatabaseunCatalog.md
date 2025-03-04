---
id: DatabaseunCatalog
title: 数据库反编目
---
如果取消数据库在客户端的映射，需要进行数据库的反编目。可以通过命令行执行的方式或界面操作的方式执行数据库反编目的命令，以完成数据库的反编目。

### ![](../../img/read.gif)操作方式

### 命令执行方法

* 模式一：非交互模式“命令窗口” 

在“命令窗口”中，数据库反编目的命令如下：

```db2 uncatalog db db_alias```
  

  * **db_alias** ：需要进行节点反编目的数据库别名。
* 模式二：交互模式“命令行处理器” 

在"命令行处理器"和"命令编辑器"中，节点反编目的命令如下：
  
```uncatalog db db_alias```  
  

### 界面执行方法

在“控制中心”左侧的目录树中，右键单击需要进行数据库反编目的数据库，选择“除去”项即可。

相关主题

 [数据库编目](DatabaseCatalog)


