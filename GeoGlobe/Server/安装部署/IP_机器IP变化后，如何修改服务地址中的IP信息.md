### 问题描述： ###

机器IP变化后，如何修改服务地址中的IP信息。   


### 解决方法： ###
将配置配置文件和运维数据库信息中的IP修改为机器目前IP；   
1)修改配置文件中的IP信息:   
 \deploylocation\deploylocal\ServiceMgr\WEB-INF\webConfig\ConnectionPool.xml文件  
 ` ConnectionPool name="IP:9010:tomcat" anotherName="domain1" `　　//IP和端口信息：修改为目前机器的IP   

 `  <URL>jdbc:sqlite:C:\Program Files\GeoGlobe\Server\support\dbscript\sqlite\GeoGlobe.db</URL>` 　　//运维数据库地址

2)修改运维数据库IP信息：  
 从上述到运维数据库中找到`GGS_SR_APPSERVER`表，修改该表中IP信息，与1)中配置的一样  

3）将不一致的信息进行修改后，重启GeoGlobeServer。  

    