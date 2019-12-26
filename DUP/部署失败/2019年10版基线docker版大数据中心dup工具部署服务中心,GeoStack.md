问题描述：

2019年10版基线docker版大数据中心dup工具部署服务中心,GeoStack
的dup工具部署GeoStack。发布服务失败





问题解答：


GeoStack的dup工具在部署geoagent时，/etc/rc.local文件未添加执行权限。服务器重启后，geoagent未运行。

