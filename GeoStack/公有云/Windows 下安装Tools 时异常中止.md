问题描述：

Windows虚拟机在安装Tools过程中，遇到异常情况导致安装中断。


可能原因：

安装过程中网络中断，或安装过程被强行中止。

处理步骤：
    
    1 在虚拟机桌面，选择“开始 > 运行”。
    2 在弹出的窗口中输入cmd。
    3 执行以下命令，进入Tools所在文件夹。
    – 32位操作系统：cd /d C:\Program Files\Xen PV Drivers\bin
    – 64位操作系统：cd /d C:\Program Files(x86)\Xen PV Drivers\bin
    说明：如果操作系统中不存在以上文件夹，可从其他虚拟机拷贝相应文件夹到该虚拟机中。
    4 执行以下命令，卸载Tools。
    uninstall.vbs
    5 重启虚拟机。
    6 重新安装Tools。






