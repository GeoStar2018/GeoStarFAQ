问题描述：

使用Geosmarter的docker版基线部署的大数据中心，在服务器重启后，服务未自动运行





问题解答：

1.在大数据中部署的时候，指定win服务服务器运行dup工具包，后期管理也使用dup工具，来进行服务的重启、停止等操作。

2.使用docker update –restart=always 命令对运行的容器做服务器重启后，docker自动启动的更新操作。
