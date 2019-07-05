问题标题：
ES乱码怎么办

![](picture/1.png)

解决方案:
将elasticsearch\bin目录下的elasticsearch.in.bat 文件中的set JAVA_OPTS=%JAVA_OPTS% -Dfile.encoding=UTF-8中的UTF-8改为GBK;
这个错误不影响，应该是客户端打开一个连接未关闭，es主动关闭引起的
