### 问题描述： ###

大数据中心支持哪些存储方式SDE直连数据源。    


### 解决方法： ###
支持ST_GEOMETRY和SDO_GEOMETRY两种存储方式的数据源，其中ST_GEOMETRY的直接注册为SDE直连数据源，SDO_GEOMETRY的注册为Oracle Spatial数据源，大数据中心不支持SDEBINARY的SDE直连。

