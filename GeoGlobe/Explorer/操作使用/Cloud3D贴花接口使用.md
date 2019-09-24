透视贴花接口使用，正交贴花要素使用方法类似
`var decalOrthoElement=g_GeoSpace.DrawBox().createDrawElement("decalOrthoElement");
var point=new rawPoint3D(114,30,50);
decalOrthoElement.decalOrthoElement(point,Cloud3D.textureSourceType.videoTexture,".\xx.mp4");
decalOrthoElement.height(60);`