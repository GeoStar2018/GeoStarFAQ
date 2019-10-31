问题描述：

如何在FusionCloud中关闭虚拟机HA服务

解决方法：

步骤1 登录FusionSphere OpenStack主节点。

●Region Type I 场景：

使用PuTTY，以Cascaded-Reverse-Proxy登录被级联层FusionSphere OpenStack主节点。默认帐号：fsp，默认密码：Huawei@CLOUD8。

●RegionType II 或Region Type III 场景：
使用PuTTY，以Reverse-Proxy登录FusionSphere OpenStack主节点。默认帐号：fsp，默认密码：Huawei@CLOUD8。

步骤2 执行以下命令并输入root密码Huawei@CLOUD8!，切换到root用户。
su - root

步骤3 执行以下命令，防止超时退出。
TMOUT=0

步骤4 导入环境变量，具体操作请参见9.8.3 导入环境变量。

步骤5 执行以下两条命令，关闭虚拟机HA服务。

> cps template-params-update --service nova nova-api --parameter ha_enabled=False
> cps commit





