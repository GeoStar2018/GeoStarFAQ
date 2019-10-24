问题描述：

C++_tinyxml2使用

问题解答：

tinyxml2解析xml文件

    
> 
tinyxml2::XMLDocument doc;
doc.LoadFile("../xml.xml");
tinyxml2::XMLElement * snapshot = doc.RootElement();
tinyxml2::XMLElement * camera = snapshot->FirstChildElement("Camera");
const char* str1 = camera->FirstChildElement("Postion")->GetText();