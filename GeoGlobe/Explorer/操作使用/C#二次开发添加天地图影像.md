问题现象： 

C#二次开发添加天地图影像


问题解决：

m_GeoSpace3D = new GeoSpace3D();
string url = "http://t0.tianditu.com/img_c/wmts";
DataLayer imgLayer= m_GeoSpace3D.DataSourceBox().CreateDataLayer(url, DataSourceType.DS_OGC_WMTS);
m_GeoSpace3D.LayerBox().AddLayer(imgLayer);