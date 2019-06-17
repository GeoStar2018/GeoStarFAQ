问题：如何安装Memcached?

解答：

memcached <1.4.5 版本安装

1、解压下载的安装包到指定目录。

2、在 1.4.5 版本以前 memcached 可以作为一个服务安装，使用管理员权限运行以下命令：

c:\memcached\memcached.exe -d install
注意：你需要使用真实的路径替代 c:\memcached\memcached.exe。
3、然后我们可以使用以下命令来启动和关闭 memcached 服务：
c:\memcached\memcached.exe -d start
c:\memcached\memcached.exe -d stop

4、如果要修改 memcached 的配置项, 可以在命令行中执行 regedit.exe 命令打开注册表并找到 "HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\memcached" 来进行修改。
如果要提供 memcached 使用的缓存配置 可以修改 ImagePath 为:
"c:\memcached\memcached.exe" -d runservice -m 512
-m 512 意思是设置 memcached 最大的缓存配置为512M。
此外我们还可以通过使用 "c:\memcached\memcached.exe -h" 命令查看更多的参数配置。

5、如果我们需要卸载 memcached ，可以使用以下命令：

c:\memcached\memcached.exe -d uninstall
memcached >= 1.4.5 版本安装

1、解压下载的安装包到指定目录。

2、在 memcached1.4.5 版本之后，memcached 不能作为服务来运行，需要使用任务计划中来开启一个普通的进程，在 window 启动时设置 memcached自动执行。
我们使用管理员身份执行以下命令将 memcached 添加来任务计划表中：
schtasks /create /sc onstart /tn memcached /tr "'c:\memcached\memcached.exe' -m 512"
