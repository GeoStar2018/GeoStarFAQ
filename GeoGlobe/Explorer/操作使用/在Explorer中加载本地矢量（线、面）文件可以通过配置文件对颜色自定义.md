问题现象： 

在Explorer中加载本地矢量（线、面）文件可以通过配置文件对颜色自定义


问题解决：

在Explorer安装路径下的appconfig.xml文件中，搜索“PolygonFillColorARGB”"PolygonOutLineColorARGB""PolylineColorARGB"
分别对应面 填充颜色、面边线颜色、线颜色

在Value中修改rgba(0,0,0,0)值
前面三项分别对应的为R/G/B，范围为0~255；最后一项为透明度，范围0~1