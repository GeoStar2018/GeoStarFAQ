# 问题原因：测试人员提供数据在Explorer中一部分矢量数据放大到第五级后无法再瓦片上显示，后来通过调试程序发现featureclass的地理范围无法包含所有数据，初步判断为数据问题，此时可以通过desktop对矢量数据地理范围重新计算。 #

解决方法：
右键featureclass->属性，点击空间索引即可重建索引修改地理范围，修改后的地理范围包含文件中所有数据。

![](https://i.imgur.com/vE0vFY8.png)