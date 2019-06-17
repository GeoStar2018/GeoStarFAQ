问题：

如何安装ES？

方法：

1.1	使用root用户永久修改文件描述符和MMap

vim  /etc/sysctl.conf
在/etc/sysctl.conf文件最后添加如下内容：
fs.file-max = 655360
vm.max_map_count=262144
使修改生效
/sbin/sysctl -p

1.2	创建启动Elasticsearch的用户组
用户组和用户名可自定义，后续设置保持一致即可

groupadd es         //添加es组
useradd es -g es     //创建es用户并加入es组
vim  /etc/security/limits.conf
在/etc/security/limits.conf文件最后添加如下内容：
* soft nofile 655360 
* hard nofile 655360
es soft memlock unlimited
es hard memlock unlimited

1.3	启动Elasticsearch

su es
给Elasticsearch安装目录授权
chmod -R 777 elasticsearch-5.6.12
进入 Elasticsearch安装目录bin目录执行
./elasticsearch  
后台启动
./elasticsearch -d

