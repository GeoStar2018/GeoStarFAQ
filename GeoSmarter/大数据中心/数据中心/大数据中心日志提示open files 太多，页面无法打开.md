问题现象： 

大数据中心日志提示open files 太多。页面无法打开。

问题原因： 

linux系统默认配置的最大文件句柄数为1024.大数据中心程序调用中可能会调用很多文件。导致报错。 修改系统的句柄数为65535