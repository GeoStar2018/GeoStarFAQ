问题描述：

GeoMap三维插件开发信号槽解绑


问题解答：

在GeoMap开发三维插件建议使用如下写法：
QgsSceneContextPtr ptrViewContext = viewContext().dynamicCast<QgsSceneContext>();
disconnect(ptrViewContext->sceneMessage(), 0, this, 0);
