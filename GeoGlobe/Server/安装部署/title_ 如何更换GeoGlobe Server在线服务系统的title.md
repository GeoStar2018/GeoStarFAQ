### 问题描述： ###

 如何更换GeoGlobe Server在线服务系统的title。


### 解决方法： ###
修改\GeoGlobe\Server6\support\web\ServiceMgr\WEB-INF\jsp\common路径下的config.jsp文件中的
`<c:set var="C_SiteName_cn" value="GeoGlobe地理信息在线服务系统"/>`信息。
