# dup 初始化失败 #

问题现象：dup部署初始化提示成功，实际上无脚本保存在服务器上。

问题原因： 服务器的selinux 需要配置为permissive。