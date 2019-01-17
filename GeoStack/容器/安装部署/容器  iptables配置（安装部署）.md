#GeoStack  容器  iptables配置 #

问题现象： 容器网络不通


问题原因： iptables服务需要开启。CentOS7环境，需要关闭firewalld，将selinux配置为permissive。