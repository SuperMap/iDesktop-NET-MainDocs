---
id: ConvertPrjCoordSys
title: Projection Transformation
---
provides three types of projection transformation: dataset projection
transformation, batch projection transformation, and coordinate
transformation.

* The dataset projection transformation is applicable to a single dataset. The dataset will be transformed and saved in a new dataset with the target projection. 
* The batch projection transformation is applicable to multiple datasets. The result datasets will be saved in the original datasource. 
* The coordinate transformation is to convert the coordinates of one point in a projection to another one.
* The feature of "Calculate Transformation Parameters" is used for getting the coordinate conversion parameters by a series of operations, then achieves the conversion from Beijing Coordinate System 1954 or Xi'an Coordinate System 1980 to China Geodetic Coordinate System 2000.

###  Contents:

[Dataset Projection Transformation](ConvertPrjCoordSysSingle)

[Batch Projection Transformation](ConvertPrjCoordSysBatch)

[Coordinate Transformation](ConvertPointPrjCoordSys)

[Calculate Transformation Parameters](Coordinatetransformation)
