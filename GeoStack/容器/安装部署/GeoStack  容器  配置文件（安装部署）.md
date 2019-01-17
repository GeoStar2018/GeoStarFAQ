#GeoStack  容器  配置文件 #

问题现象： 程序运行中文编码显示问题


问题原因： lxc容器制作中默认使用的编码为非utf-8的。在容器的etc目录下，添加一个locale.conf文件，内容为LANG="zh_CN.UTF-8"即可。