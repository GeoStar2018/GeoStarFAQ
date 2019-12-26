问题描述：

GeoMap框架中打开选择文件对话框


问题解答：
> 
> QString strFilter = QObject::tr("Situation Symbol(*.symx)"); //以*.symx文件为例
> QString strFilePath = QgsFileDialog::getOpenFileName("", nullptr, QObject::tr("Open Data"), "", strFilter);
> if (strFilePath.isEmpty() || strFilePath.isNull())
> 	return;
> GsString sPath = strFilePath.toUtf8().data();



**注：QgsFileDialog::getSaveFileName为框架中保存文件对话框**