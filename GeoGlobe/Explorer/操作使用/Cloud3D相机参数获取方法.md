//获取当前相机参数方法
> var m_para;
function GetCurrentPos(){
    //接收相机参数回调
    g_GeoSpace.SceneBox().onReceiveRoutePoint= function (para) {
        //接收到相机参数，包括相机姿态信息
        m_para = para;
    }
    //发送记录相机信息命令
    g_GeoSpace.SceneBox().addCustomFlyPointByMove();};