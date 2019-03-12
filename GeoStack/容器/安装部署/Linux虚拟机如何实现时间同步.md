1.	问题描述：
Linux虚拟机如何实现时间同步？


2.	问题解决
yum -y install chrony
	systemctl enable chronyd && systemctl start chronyd
