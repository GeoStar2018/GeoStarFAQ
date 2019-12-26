问题描述：

大数据中心docker版基线部署，zabbix服务运行的宿主机监控缺失





问题解答：

需要在宿主机上安装zabbix agent，且配置zabbix agent的conf文件中zabbix server地址为docker 容器的ip地址。