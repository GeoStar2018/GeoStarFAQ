1.	问题描述：
LXC容器语言出现中文乱码问题


2.	问题解答：
编辑/etc/sysconfig/i18n
修改后内容如下：
LANG="zh_CN.UTF-8"
