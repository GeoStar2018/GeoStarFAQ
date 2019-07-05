问题描述

Desktop导入Shape数据到Oracle中，数据有58万，但只有28万导入进去

解决办法：

这个问题的根本原因是数据库使用了UTF8的字符集。Shape中一个2字节的字符串，在UTF8中其实应该是4个字节表示，但是Oracle里面创建属性结构的时候还是2个字节，所以就超长了，不让导入。一般来说支持中文的Oracle数据库都不会用UTF8，否则大部分的中文系统都会碰到这个问题，解决方案有两个：

1）、字符集AL32UTF8的库转换成AL16UTF16字符集方法： 
以DBA身份进入SQLPLUS
SQL> sqlplus sys/sys as sysdba;
……
SQL> shutdown immediate;
SQL> startup mount;
SQL> alter system enable restricted session;
SQL> alter system set job_queue_processes=0;
SQL> alter system set aq_tm_processes=0;
SQL> alter database open;
SQL> alter database character set internal_use AL32UTF8;(ZHS16GBK)
SQL> shutdown immediate;
SQL> startup;
这样就可以讲ORACLE的字符集修改为UTF8，如果需要修改为GBK只需将alter database character set internal_use AL32UTF8;(ZHS16GBK)这句最后的AL32UTF8修改为ZHS16GBK即可。

2）、将中文字符串Oracle属性结构字节扩大1倍。

