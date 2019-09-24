//当前编辑模型对象
    `var currentModel=new modelParameter(0,null,null,null);`

//模型编辑选择
    `function modelEditorPicker(){
    var scenePicker = g_GeoSpace.SceneBox().scenePicker("worldPicker");
    scenePicker.enableModelPick(true);
    scenePicker.onInfoGot=function(obj){
        currentModel=obj;
    }};`


//模型平移
> function modelEditorTranslate(){
    //取消高亮(如果需要)
    var scenePicker = g_GeoSpace.SceneBox().scenePicker("worldPicker");
    scenePicker.enableModelPick(false);
    scenePicker.cancelHighlight();


 //参数解释：第一个参数为模型对象；第二个参数为枚举类型modelEditorDirectionType，其中包括东南西北上下六种枚举；第三个参数为数量
> 
    g_GeoSpace.SceneBox().sceneEditor("worldEditor").modelTranslate(currentModel,modelEditorDirectionType.south,2);};


//模型缩放
> function modelEditorScale(){
    //取消高亮(如果需要)
    var scenePicker = g_GeoSpace.SceneBox().scenePicker("worldPicker");
    scenePicker.enableModelPick(false);
    scenePicker.cancelHighlight();

    //参数解释：第一个参数为模型对象；后三个参数分别对应的x.y.z缩放比例，正数代表放大，负数为缩小
    g_GeoSpace.SceneBox().sceneEditor("worldEditor").modelScale(currentModel,0.5,0.5,0.5);};

//模型旋转
> function modelEditorRotate(){
    //取消高亮(如果需要)
    var scenePicker = g_GeoSpace.SceneBox().scenePicker("worldPicker");
    scenePicker.enableModelPick(false);
    scenePicker.cancelHighlight();

    //参数解释：第一个参数为模型对象；中间三个参数为轴方向；最后一个参数为旋转角度
    g_GeoSpace.SceneBox().sceneEditor("worldEditor").modelRotate(currentModel,1,1,0,75);};