问题现象： 

Web端每次添加飞行节点的时候（SceneBox().addCustomFlyPointByMove()），后台服务Explorer会向前端返回接受消息(onReceiveRoutePoint)，返回对应的飞行点坐标信息



问题解决：


参数分别为飞行ID、cameraposition，cameradirection，cameraup，以及飞行时间