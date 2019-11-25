问题描述：

请使用Linux系统命令统计出establish状态的连接数有多少?

解决方法：

$ netstat -an |grep ESTABLISHED |wc -l
netstat命令-a参数是显示所有链接，-n是不要域名解析，即都是以数字IP的显示。

现实生产系统的时候，如果服务器维持的链接是成千上万的话，少用netstat，多用ss。





