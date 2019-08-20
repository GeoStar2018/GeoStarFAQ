问题描述：

Geoglobe desktop或者瓦片生产工具连接MySQL数据库，新建瓦片数据集失败 

解决方法：

1、	需要检查安装的MySQL版本，不能低于MySQL 5.6版本
2、	连接数据库，检查下数据库用户权限，是否有创建视图的权限，如下图：
![](picture/4.png)


![](picture/5.png)