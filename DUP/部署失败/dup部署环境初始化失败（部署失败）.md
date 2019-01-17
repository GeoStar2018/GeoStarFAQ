# dup 部署失败 #

  问题现象： dup部署环境初始化失败

  问题原因： 第4版的dup工具中，lxc_host_baseenv_check.sh的29行getenforce拼写错误。