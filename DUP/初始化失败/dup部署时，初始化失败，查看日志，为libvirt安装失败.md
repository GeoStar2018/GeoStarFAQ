 问题现象： 

dup部署时，初始化失败，查看日志，为libvirt安装失败。


问题原因：  

删除防火墙和NetworkManager 时，使用yum autoremove 来删除，导致依赖包丢失。在删除的时候只能使用 yum remove 删除。修复libvirt依赖的rpm包。
