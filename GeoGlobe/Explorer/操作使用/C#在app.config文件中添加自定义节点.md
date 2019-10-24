问题描述：

C#在app.config文件中添加自定义节点

问题解答：

在app.config文件的<configSections>节点下增加如
<section name="OSGB" type="System.Configuration.NameValueSectionHandler"/>
然后在<configSections>同级下增加<OSGB>节点
如下：

在app.config文件的<configSections>节点下增加如
<section name="OSGB" type="System.Configuration.NameValueSectionHandler"/>
然后在<configSections>同级下增加<OSGB>节点
如下：
    ` <OSGB>
    <add key="1" value="E:\ZYZ\testdata\JYH\osgb\osgb.oindex" />
 </OSGB>
`

在C#代码中读取appconfig需要引用的命名空间包括
> 
using System.Configuration;
using System.Collections.Specialized;

> 
NameValueCollection nvcosgb = (NameValueCollection)ConfigurationManager.GetSection("OSGB");
foreach(string key in nvcosgb.AllKeys)
{
     string str = nvcosgb[key].ToString();
}


在C#代码中读取appconfig需要引用的命名空间包括

    using System.Configuration;
    using System.Collections.Specialized;


> 
NameValueCollection nvcosgb = (NameValueCollection)ConfigurationManager.GetSection("OSGB");
foreach(string key in nvcosgb.AllKeys)
{
     string str = nvcosgb[key].ToString();
}