问题描述：

GeoShow如何增量迁移

问题解答：

GeoShow项目配置的信息都存储在geo_layout_project表中，如果只是GeoShow增量更新，直接迁移geo_layout_project表就行。
更新geo_layout_projec表里对应的服务器ip及端口，以招投标项目迁移为例：
update geo_layout_project set content=replace(content,'192.168.30.82:8080/ztb_dps','10.28.79.108:9010/ztb_dps')
update geo_layout_project set content=replace(content,'192.168.30.82:8080','ztb.geostar.com.cn ')

