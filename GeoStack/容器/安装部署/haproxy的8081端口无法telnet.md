 问题现象：

haproxy的8081端口无法telnet


问题原因：

 重启haproxy服务无法启动，/var/lib/haproxy 文件夹丢失。手动创建haproxy文件夹后，服务启动，恢复正常。