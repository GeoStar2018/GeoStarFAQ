问题现象：  数据中心solr服务无法使用

问题原因：  数据中心的solrcloud配置文件中solr的地址配置为ip。如果大数据中心和solr在同一台机器，需要配置为域名。