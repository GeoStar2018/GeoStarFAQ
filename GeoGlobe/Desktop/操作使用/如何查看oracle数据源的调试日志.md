问题描述：

Desktop将数据导入Oracle的时候如何查看oracle数据源的调试日志？

问题解答：

GeoGlobe导入Oracle数据源的日志需要人工开启，在环境变量中增加SQL_DUMP值设为1，就可以将日志开启。日志的地址：c:\traceora.log；不用的时候值设为0，即可关闭。