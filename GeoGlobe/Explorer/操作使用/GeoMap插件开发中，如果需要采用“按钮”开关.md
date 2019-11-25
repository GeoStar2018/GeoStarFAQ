问题描述：

GeoMap插件开发中，如果需要采用“按钮”开关

需要将

    m_toolType=enumToolType::eStateReverseTool;

同时派生类中需要重写父类的activate()和deactivate()，分别在开和关的两种情况下触发（如下图二）

![](pic/11.png)

![](pic/12.png)
