问：

GeoSmarter2019的大数据中心基线软件，cas都做了单客户端登陆限制，但是项目上调试的时候使用多有不便，请问如何解除。

解答：

在大数据中心2019年第四版（含）以前的版本，cas未提供此配置项无法关闭，建议新建多个用户以解决冲突的问题，第五版及以后的版本，在cas的配置文件cas/WEB-INF/cas.properties中找到属性single.client.login将其值改为false，重启cas即可。
