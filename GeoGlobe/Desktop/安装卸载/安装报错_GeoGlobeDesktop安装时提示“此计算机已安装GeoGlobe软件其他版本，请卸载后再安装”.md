### 问题描述： ###

GeoGlobeDesktop安装时提示“此计算机已安装GeoGlobe软件其他版本，请卸载后再安装”。


### 解决方法： ###
1)删除如下注册表节点：  
32位下节点路径为："/HKEY_LOCAL_MACHINE/SOFTWARE/GeoGlobe"  
64位下节点路径为："/HKEY_LOCAL_MACHINE/SOFTWARE/Wow6432Node/GeoGlobe"；   
2)重新运行程序。
  
