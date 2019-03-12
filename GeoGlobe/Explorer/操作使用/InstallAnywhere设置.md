软件打包工具InstallAnywhere：

在Install步骤中Add Action，如果需要直接启动打包路径下的某一个文件，这个时候
有Execute Target File命令可以直接启动，但是经过验证发现启动后的程序是处于
临时路径下的，并非安装路径，运行环境会存在问题。

其他代替方法：
使用Create Shortcut创建程序的桌面快捷方式