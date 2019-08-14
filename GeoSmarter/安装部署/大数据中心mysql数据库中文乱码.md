问：

安装大数据中心之后再mysql上进行数据库的初始化，中文字符乱码


答：

数据库安装之后默认的字符集应该是Latin1，需要在配置文件中改为utf8
在mysql的安装目录下的my.ini文件中进行配置修改 ：
[client] 
default-character-set = utf8

[mysql] 
default-character-set = utf8

[mysqld] 
character-set-client-handshake = FALSE 
character-set-server = utf8
collation-server = utf8_unicode_ci 
init_connect=’SET NAMES utf8’

然后重启mysql
