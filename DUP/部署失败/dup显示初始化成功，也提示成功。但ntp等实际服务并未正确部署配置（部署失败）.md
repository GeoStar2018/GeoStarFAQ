# dup 部署失败 #

 问题现象： dup显示初始化成功，也提示成功。但ntp等实际服务并未正确部署配置。

 问题原因： 在进行服务分配的时候将容器服务。和作为支撑的ntp等服务部署在一个服务器上，容器服务依赖的libvirt程序会对基础服务包产生影响。
