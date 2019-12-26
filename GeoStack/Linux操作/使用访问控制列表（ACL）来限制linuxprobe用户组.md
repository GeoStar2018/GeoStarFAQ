问题描述：

使用访问控制列表（ACL）来限制linuxprobe用户组，使得该组中的所有成员不得在/tmp目录中写入内容？

问题解答：

想要设置用户组的ACL，则需要把u改成g，即setfacl -Rm g:linuxprobe:r-x /tmp。