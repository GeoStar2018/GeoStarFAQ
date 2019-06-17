问题现象： 

C#二次开发中没有默认地形的解决办法


问题解决：

如果在同目录下能启动Explorer，可以直接在Explorer中设置

文件->选项->通用->勾选“加载默认地形”

或者到Temp临时文件目录中，例如：C:\Users\Administrator\AppData\Roaming\GeoStar\GeoGlobe Explorer\userconfig.xml
修改SceneGraph/DrawContext/DefaultTerrain 为true