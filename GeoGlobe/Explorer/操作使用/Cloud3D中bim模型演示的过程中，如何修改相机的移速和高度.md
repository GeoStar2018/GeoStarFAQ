问题：

Cloud3D中bim模型演示的过程中，如何修改相机的移速和高度

解答：


需要在appconfig.xml文件中修改
<Config Name="IndoorCameraConfig" Type="" Description="室内相机配置">

              <Config Name="ManHeight" Type="Float" Description="人的高度">
                            <Value>1.75</Value>
              </Config>
              <Config Name="MoveSpeed" Type="Float" Description="人行走速度">
                            <Value>2.0</Value>
              </Config>
</Config>
