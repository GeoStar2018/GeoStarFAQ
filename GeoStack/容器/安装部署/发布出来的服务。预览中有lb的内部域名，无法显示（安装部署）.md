#GeoStack  容器  配置文件 #

   问题现象： 发布出来的服务。预览中有lb的内部域名，无法显示。

   问题原因： 需要修改soms库中的ggs_sr_appserver中的记录，将lb.gfstack.geo 修改为ip，然后重启服务。