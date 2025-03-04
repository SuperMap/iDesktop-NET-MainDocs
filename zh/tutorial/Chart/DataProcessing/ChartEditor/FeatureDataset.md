---
id: FeatureDataset
title: 特征物标数据集的管理
---
在 SuperMap
海图模块中，一个物标编码（或简称）和一种数据集类型可以唯一确定一个特征物标类型，也就是确定一个特征物标数据集。同一种物标可能有不同的几何对象类型，例如湖岸（LAKSHR）可以是线状的，也可以是面状的，如果两种几何类型的湖岸同时存在于一幅海图中，那么将分别以一个线数据集和一个面数据集来存储。各类型的特征物标存储于对应的特征物标数据集中，所以在绘制某类型物标前，需创建或追加导入相应的特征物标数据集。

提供的特征物标数据集的操作，包括：创建一个新的特征物标数据集、删除一个特征物标数据集、向特征物标数据集追加记录。

### 内容提要：

[创建特征物标数据集](CreateFeatureDataset)  
介绍在可编辑分组中创建特征物标数据集的具体操作。

[追加特征物标数据集](AddToFeatureDataset)  
介绍将已有特征物标数据集信息追加至可编辑分组中的具体操作。