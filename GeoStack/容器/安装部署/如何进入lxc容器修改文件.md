问题描述：

如何进入lxc容器修改文件？


解决办法：

吉奥的lxc容器统一放置在路径为/var/lib/libvirt/images文件夹下面。当要修改容器内的配置文件时，直接使用命令cd /var/lib/libvirt/images/<容器名>，然后进入相应的文件夹完成修改。
