用weblogic部署集群，weblogic启动提示系统找不到指定路径，检查Java_Home的环境变量指定是正确的

![](picture/p4.png)

解决方法：

找不到路径的原因可能是安装路径中间有个空格，这样在weblogic启动时找不到这样的路径，建议安装GeoGlobe Server时安装目录不要有空格
