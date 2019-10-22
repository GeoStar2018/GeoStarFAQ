问：大数据中心数据中心如何安装索引服务器solr。


答：

1.将solrServer.tar.gz复制到GeoSmarter安装目录(默认/usr/GeoSmarter/)

2.
解压压缩包
[root@localhost root]# cd /usr/GeoSmarter/
[root@localhost GeoSmarter]# chmod +x solrServer.tar.gz
[root@localhost GeoSmarter]# tar -zxf solrServer.tar.gz

3.修改配置文件

/usr/GeoSmarter/solrServer/apache-tomcat-8.5.31/webapps/solr/WEB-INF/web.xml

      <env-entry>
      <env-entry-name>solr/home</env-entry-name>
      <env-entry-value>/usr/GeoSmarter/solrServer/solrHome</env-entry-value>
      <env-entry-type>java.lang.String</env-entry-type>
    </env-entry>

第三行改为solrHome的实际地址

4.修改tomcat端口号/usr/GeoSmarter/solrServer/apache-tomcat-8.5.31/conf/server.xml

  修改solr端口号/usr/GeoSmarter/solrServer/solrHome/solr.xml,端口号与tomcat一致

    <int name="hostPort">${jetty.port:8080}</int>

5.启动tomcat

    [root@localhost GeoSmarter]# cd /usr/GeoSmarter/solrServer/apache-tomcat-8.5.31/bin
    [root@localhost bin]# ./startup.sh
    