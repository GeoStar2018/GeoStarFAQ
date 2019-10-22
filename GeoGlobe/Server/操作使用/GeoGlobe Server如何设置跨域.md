问题描述：


GeoGlobe Server如何设置跨域？

解决办法：

在GeoGlobe Server的系统设置中找到HTTP响应头，名称添加Access-Control-Allow-Origin内容，值添加*，如下图所示:

![](pic/1.png)