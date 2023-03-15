# 安卓 VNC 服务器 0.2

> 原文：<https://www.xda-developers.com/android-vnc-server-0-2/>

如果你想远程访问你的手机，你可能想试试 XDA 论坛成员[on IPS](http://forum.xda-developers.com/member.php?u=2546333)开发的安卓 VNC 服务器。

该应用程序可以让你通过 WiFi 或 USB 远程连接到你的 Android 设备。通过 USB 连接需要使用以下 adb 命令将端口 5901 从设备转发到 PC-> ADB forward TCP:5901 TCP:5901，然后从您的 VNC 客户端连接到 localhost:5901。

> *安卓 VNC 服务器的特性包括:*
> 
> *   *用于启动/停止服务器和设置密码的 GUI*
> *   *设置密码进入*
> *   *输入事件由 uinput 处理(无需手动设置设备)*

需要根。

该应用程序可以在市场上免费下载。更多信息，请访问[应用线程](http://forum.xda-developers.com/showthread.php?t=710805)。