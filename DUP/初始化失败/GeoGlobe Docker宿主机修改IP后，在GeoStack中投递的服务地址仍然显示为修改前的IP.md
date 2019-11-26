【问题描述】

修改GeoGlobe Docker宿主机的IP后，同时也修改GeoStack页面中容器宿主机的IP，但投递出来的服务地址仍然显示为修改前的IP。

【解决方法】

> 1.	访问http://Docker宿主机IP:2375/nodes，检查返回消息中Addr字段的值，实际返回的IP地址仍然为Docker宿主机修改前的IP。
> 2.	在Docker宿主机上执行docker swarm leave命令，使当前Docker宿主机退出swarm集群管理。
> 3.	在Docker宿主机上执行docker swarm init命令，重新制作docker集群。
> 4.	再次访问http://Docker宿主机IP:2375/nodes，返回消息中Addr字段的值显示为当前新的IP地址。
> 5.	重新在GeoStack页面中投递新的服务，服务地址已更新为新的Docker宿主机IP地址。
