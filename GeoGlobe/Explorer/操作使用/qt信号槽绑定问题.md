问题描述：

qt信号槽绑定问题

问题解答：
qt4中绑定信号槽的写法有：

> connect(m_pListWidget, SIGNAL(customContextMenuRequested(const QPoint&)), this, SLOT(onListContextMenu(const QPoint&)));


 在GeoMap开发中建议使用如下写法：

 
> connect(m_pListWidget, &QgsFlightTreeWidget::customContextMenuRequested, this, &QgsFlightTreeWidget::onListContextMenu);
