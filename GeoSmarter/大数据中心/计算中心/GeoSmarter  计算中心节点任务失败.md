【标题】GeoSmarter  计算中心节点任务失败

【问题描述】大数据中心的计算中心节点配置计划任务后，点击运行任务，显示运行中，无法停止。

【解决方法】排除节点问题及计算中心的连接，融合设计器的流程等方面的问题。是由于计算模型中某一个节点任务需要调用数据库，而数据库处于更新或读取状态，未将状态反馈给模型，导致整个模型执行异常。

