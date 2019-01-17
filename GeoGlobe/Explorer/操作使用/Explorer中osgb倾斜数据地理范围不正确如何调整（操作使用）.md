# 问题：在Explorer中打开osgb数据部分情况下，osgb地理范围不正确导致跳转位置有误 #


解决方法：
打开osgb的*.oindex文件，将
Parameter:Extent=*******，******
一行删除，然后保存。
Explorer会在再次双击跳转的时候重新计算osgb地理范围并保存。