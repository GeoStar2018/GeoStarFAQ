问：

cas登陆页面的ui默认为GeoStack的，若我需要修改为大数据中心的UI或者项目自定义的UI怎么修改。

答：

在cas的配置文件（cas/WEB-INF/cas.properties）中找到cas.themeResolver.pathprefix属性，将其属性改成UI所在路径。如大数据中心修改为(/WEB-INF/view-geosmarter/jsp/)重启cas
