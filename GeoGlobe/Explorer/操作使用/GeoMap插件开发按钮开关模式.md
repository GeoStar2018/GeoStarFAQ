问题描述：

GeoMap插件开发按钮开关模式

问题解答：

以QListWidget为例

    m_pListWidget->setContextMenuPolicy(Qt::CustomContextMenu);
//绑定槽函数

    connect(m_pListWidget, &QgsFlightTreeWidget::customContextMenuRequested, this, &QgsFlightTreeWidget::onListContextMenu);
    m_pListItemMenu = new QMenu(m_pListWidget);

//绑定菜单功能

    connect(m_pListItemMenu->addAction(QString::fromLocal8Bit("重命名")), SIGNAL(triggered(bool)), this, SLOT(onListItemRename()));


onListContextMenu槽函数写法
    
    void QgsFlightTreeWidget::onListContextMenu(const QPoint& pt)
    {
    QListWidgetItem *item = m_pListWidget->itemAt(pt);
    if (item)
    {
    m_pListItemMenu->exec(QCursor::pos());
    }
    else
    {
    m_pListGlobeMenu->exec(QCursor::pos());
    }
    }