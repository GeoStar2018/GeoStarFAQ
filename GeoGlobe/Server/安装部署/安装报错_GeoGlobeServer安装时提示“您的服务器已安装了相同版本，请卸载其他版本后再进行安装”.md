### 问题描述： ###

GeoGlobeServer安装时提示“您的服务器已安装了相同版本，请卸载其他版本后再进行安装”。


### 解决方法： ###
1)删除如下注册表节点："/HKEY_LOCAL_MACHINE/SOFTWARE/Wow6432Node/GeoGlobe"；   
2)删除对应的环境变量  
3)重新运行程序
