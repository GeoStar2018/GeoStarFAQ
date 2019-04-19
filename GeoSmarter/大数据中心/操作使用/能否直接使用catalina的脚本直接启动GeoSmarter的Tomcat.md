问题描述：

启动GeoSmarter的Tomcat，启动/GeoSmarter/bin/Tomcat.sh(或Tomcat.bat)和启动/GeoSmarter/server/bin/catalina.sh(或catalina.bat)有什么不同？


回答：

首先这两个都能启动GeoSmarter的Tomcat，而且启动/GeoSmarter/bin/Tomcat.sh(或Tomcat.bat)的时候，脚本最后一步调用的也是catalina.sh(或catalina.bat)，但是不同是Tomcat.sh(或Tomcat.bat)中定义了一些GeoSmarter必须要使用的JDK等环境变量，如果直接起catalina的脚本，可能直接调用系统的JDK，导致系统功能部分不正常。

建议使用/GeoSmarter/bin/Tomcat.sh(或Tomcat.bat)启动GeoSmarter程序。
