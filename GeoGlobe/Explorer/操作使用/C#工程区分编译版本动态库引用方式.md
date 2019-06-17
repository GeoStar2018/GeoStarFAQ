问题现象： 

C#工程区分编译版本动态库引用方式


问题解决：


在C#工程中，Debug和Release两种编译状态下如果想引用不同路径下的动态库通过直接设置引用无法解决。

可以采用修改工程的.csproj文件中配置完成。
将.csproj文件使用记事本打开，在ItemGroup中找到Reference项。写法如下：
<Reference Condition="'$(Configuration)'=='Release'" Include="GeoStar.Core">
      <HintPath>..\..\..\..\Explorer\releasex64\GeoStar.Core.dll</HintPath>
</Reference>
<Reference Condition="'$(Configuration)'=='Debug'" Include="GeoStar.Core">
      <HintPath>..\..\..\..\Explorer\debugx64\GeoStar.Core.dll</HintPath>
</Reference>