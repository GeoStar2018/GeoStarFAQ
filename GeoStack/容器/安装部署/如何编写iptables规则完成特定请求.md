问：
怎样编写一条防火墙策略规则，使得iptables服务可以禁止源自192.168.10.0/24网段的流量访问本机的sshd服务（22端口）？

答：执行命令iptables -I INPUT -s 192.168.10.0/24 -p tcp --dport 22 -j REJECT即可。
