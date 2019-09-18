问题描述：

如何使用GeoShow的api

问题解答：

1、先把GeoShow工程下的js文件夹，整个拷贝到目标工程下。
2、再引入脚本
    
GeoGlobeMap
    `<script type="text/javascript" src="<%=basePath%>js/geoMap/OpenLayers/OpenLayers-min.js"></script>`

    `<script type="text/javascript" src="<%=basePath%>js/geoMap/GeoGlobeJS.min.js"></script>`


翻牌器
    `<script type="text/javascript" src="<%=basePath%>js/odoo.js"></script> `

 GeoSmarter
    `<script type="text/javascript" src="<%=basePath%>js/GeoSmarter/GeoSmarter.debug.js"></script>`

svg、视频
    `<script type="text/javascript" src="<%=basePath%>js/GeoSmarter/svg.js"></script> `


 
    `<script type="text/javascript" src="<%=basePath%>js/GeoSmarter/Video-plugin.js"></script>`


jquery
    `<script type="text/javascript" src="<%=basePath%>js/jquery/jquery-1.11.3.min.js"></script>`

    `<script type="text/javascript" src="<%=basePath%>web/workbench/assets/jquery-ui/1.11.2/jquery-ui.min.js"></script>`



 echarts
    `<%-- <script type="text/javascript" src="<%=basePath%>js/echarts/2.2.7/dist/echarts.js"></script> --%>`

    `<script type="text/javascript" src="<%=basePath%>js/echarts/3.3.1/echarts.min.js"></script>`

    `<script type="text/javascript" src="<%=basePath%>js/echarts-wordcloud.min.js"></script>`


Highcharts

    `<%-- <script type="text/javascript" src="<%=basePath%>js/Highcharts-4.1.9/js/highcharts.js"></script> --%>`

`<script type="text/javascript" src="<%=basePath%>js/Highcharts-4.1.9/js/highcharts-3d.js"></script>`
`<%-- <script type="text/javascript" src="<%=basePath%>js/Highcharts-4.1.9/js/modules/exporting.js"></script> --%>`

`<%-- <script type="text/javascript" src="<%=basePath%>js/Highcharts-4.1.9/js/modules/data.js"></script> --%>`

`<%-- <script type="text/javascript" src="<%=basePath%>js/Highcharts-4.1.9/js/modules/drilldown.js"></script> --%>`

`<script type="text/javascript" src="<%=basePath%>js/Highcharts-5.0.7/code/highcharts.js"></script>`

`<script type="text/javascript" src="<%=basePath%>js/Highcharts-5.0.7/code/highcharts-3d.js"></script>`

`<script type="text/javascript" src="<%=basePath%>js/Highcharts-5.0.7/code/modules/exporting.js"></script>`

`<script type="text/javascript" src="<%=basePath%>js/Highcharts-5.0.7/code/modules/data.js"></script>`

`<script type="text/javascript" src="<%=basePath%>js/Highcharts-5.0.7/code/modules/drilldown.js"></script>`





jqxWidget

`<script type="text/javascript" src="<%=basePath%>js/jqwidgets/jqxcore.js"></script>`
`<script type="text/javascript" src="<%=basePath%>js/jqwidgets/jqxdata.js"></script> `
`<script type="text/javascript" src="<%=basePath%>js/jqwidgets/jqxbuttons.js"></script>`
`<script type="text/javascript" src="<%=basePath%>js/jqwidgets/jqxscrollbar.js"></script>`
`<script type="text/javascript" src="<%=basePath%>js/jqwidgets/jqxmenu.js"></script>`
`<script type="text/javascript" src="<%=basePath%>js/jqwidgets/jqxdatatable.js"></script>`
`<script type="text/javascript" src="<%=basePath%>js/jqwidgets/jqxtabs.js"></script>`
`<script type="text/javascript" src="<%=basePath%>js/jqwidgets/jqxcheckbox.js"></script>`
`<script type="text/javascript" src="<%=basePath%>js/jqwidgets/jqxlistbox.js"></script>`
`<script type="text/javascript" src="<%=basePath%>js/jqwidgets/jqxdropdownlist.js"></script>`
`<script type="text/javascript" src="<%=basePath%>js/jqwidgets/jqxgrid.js"></script>`
`<script type="text/javascript" src="<%=basePath%>js/jqwidgets/jqxgrid.sort.js"></script>` 
`<script type="text/javascript" src="<%=basePath%>js/jqwidgets/jqxgrid.pager.js"></script>`
`<script type="text/javascript" src="<%=basePath%>js/jqwidgets/jqxgrid.columnsresize.js"></script>`
`<script type="text/javascript" src="<%=basePath%>js/jqwidgets/jqxgrid.columnsreorder.js"></script>` 
`<script type="text/javascript" src="<%=basePath%>js/jqwidgets/jqxgrid.selection.js"></script>` 
`<script type="text/javascript" src="<%=basePath%>js/jqwidgets/jqxgrid.edit.js"></script>` 
`<script type="text/javascript" src="<%=basePath%>js/jqwidgets/jqxpanel.js"></script>`
`<script type="text/javascript" src="<%=basePath%>js/jqwidgets/scripts/demos.js"></script>`
jqxWidget

ztree
`<script type="text/javascript" src="<%=basePath%>js/jquery-zTree/3.5/js/jquery.ztree.all-3.5.min.js"></script>`
ztree

3、引入样式
`<link rel="stylesheet" href="<%=basePath%>js/GeoSmarter/css/style.css" type="text/css" />`
