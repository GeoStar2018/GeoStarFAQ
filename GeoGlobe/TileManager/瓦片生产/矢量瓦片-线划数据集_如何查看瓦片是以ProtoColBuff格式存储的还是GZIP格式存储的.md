### 问题描述： ###

如何查看瓦片是以ProtoColBuff格式存储的还是GZIP格式存储的。


### 解决方法： ###
根据实体表中的tiletype字段去判断，11表示ProToColBuff，12表示GZIP；下图以SQLite格式为例。  
![](picture/p13.png)  


