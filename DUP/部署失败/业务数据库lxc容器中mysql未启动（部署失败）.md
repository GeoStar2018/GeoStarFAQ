# dup 部署失败 #

  问题现象： 业务数据库lxc容器中mysql未启动

  问题原因：在配置阶段mysql容器需要分配至少4G内存。否则mysql无法启动，无法初始化