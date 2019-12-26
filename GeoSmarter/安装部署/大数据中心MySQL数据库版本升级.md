问题描述：

因MySQL 5.6.38版本存在安全漏洞，需将大数据中心MySQL数据库由5.6.38升级至5.7.28版本。




问题解答：

- 1.	大数据中心MySQL数据库初始版本为5.6.38：

> mysqlselect @@version
> 
> -;
> 
> +-----------+
> 
> | @@version |
> 
> +-----------+
> 
> | 5.6.38|
> 
> +-----------+
> 
> 1 row in set (0.00 sec)



-  2.	备份整个5.6.38版本的数据库。
-  3.	进入5.7.28版本的mysql/bin目录下，执行以下命令进行数据库的初始化：


**[mysql@host-172-15-110-97 bin]$ ./mysqld --user=mysql --basedir=/home/mysql/mysql-5.7.28-linux-glibc2.12-x86_64 --datadir=/home/mysql/mysql-5.7.28-linux-glibc2.12-x86_64/data --initialize**

- 4.	手工在/home/mysql/mysql-5.7.28-linux-glibc2.12-x86_64目录下分别创建log和run目录，在log和run目录下分别创建mysqld.err和mysqld.pid文件。
- 5.	取5.6.38版本的my.cnf文件放到/home/mysql/mysql-5.7.28-linux-glibc2.12-x86_64目录下，作为5.7.28版本启动数据库的配置文件。
- 6.	将5.6.38版本data目录下的所有数据文件拷贝至5.7.28版本的data目录下覆盖同名文件，并确保所有数据文件和文件夹的属组均为mysql:mysql。
- 7.	执行以下命令启动5.7.28版本的mysql：


**[mysql@host-172-15-110-97 bin]$ ./mysqld_safe --defaults-file=/home/mysql/mysql-5.7.28-linux-glibc2.12-x86_64/my.cnf &**


- 8.	连接至5.7.28版本的mysql，查询从5.6.38版本mysql中迁移过来数据库信息是否正常。
- 9.	将大数据中心所有配置文件中的数据库连接地址修改为5.7.28版本mysql的地址，并重新启动大数据中心的Tomcat。

