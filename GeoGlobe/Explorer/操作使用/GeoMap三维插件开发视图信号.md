问题描述：

GeoMap三维插件开发视图信号


问题解答：

QgsSceneMessage类对GsSceneMessageHandle进行封装，可以使用QT中信号槽绑定的方式绑定信号。

提供的信号包括：
signals:
	/// \brief 鼠标按下事件
	void onMousePressEvent(KERNEL_NAME::GsButton button, int x, int y);

	/// \brief 鼠标弹起事件
	void onMouseReleaseEvent(KERNEL_NAME::GsButton button, int x, int y);

	/// \brief 鼠标移动事件
	void onMouseMoveEvent(KERNEL_NAME::GsButton button, int x, int y);

	/// \brief 鼠标双击事件
	void onMouseDoubleClickEvent(KERNEL_NAME::GsButton button, int x, int y);

	/// \brief 按键按下事件
	void onKeyPressEvent(KERNEL_NAME::GsKey key);

	/// \brief 按键弹起事件
	void onKeyReleaseEvent(KERNEL_NAME::GsKey key);

	/// \brief 焦点进入场景
	void onFocusEvent();

	/// \brief 焦点移出场景
	void onFocusOutEvent();

使用方法：

connect(ptrViewContext->sceneMessage(), &QgsSceneMessage::onMouseReleaseEvent, this, &QgsLinePlottingTool::onMouseRelease);