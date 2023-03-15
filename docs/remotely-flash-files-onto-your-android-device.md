# 远程将文件闪存到您的 Android 设备上

> 原文：<https://www.xda-developers.com/remotely-flash-files-onto-your-android-device/>

将文件刷新到 Android 设备上的传统方式有几个缺点。如果你想手动这样做，这涉及到用 USB 电缆连接你的设备，你似乎只是在几分钟前丢失了。然后是测试新主题、mod 和 rom 的试错过程。然而，这一切都可以通过 XDA 资深会员 [Prl91](http://forum.xda-developers.com/member.php?u=4979049) 的 RemoteFlash 来避免。

RemoteFlash 允许你将个人电脑上的文件直接闪存到你的 Android 设备上，省去了线缆和麻烦。它由两个组件组成:一个作为 PC 客户端的独立 Java 应用程序，和一个用于 Android 的简单 APK。安装 APK 后需要重新启动，该应用程序将在后台静默运行，而 PC 客户端会自动扫描您的设备，随后通过擦除*/数据*和*/缓存*选项刷新选定的文件。请记住，PC 和您的设备必须在同一个 WiFi 网络上，并且网络上安装了 RemoteFlash 的任何其他设备都必须断开连接，扫描才能正常运行。Prl91 建议使用 *OpenRecoveryScript* 进行自定义恢复，例如 TWRP，尽管 CWM 可能根据安装的版本而可用。

在撰写本文时，Prl91 还没有对错误的文件传输执行 MD5 检查，尽管有一个系统可以持续监控通过 TCP 套接字流的字节流。如果有一个字节丢失或连接闪烁，客户端会立即取消从 PC 到设备的传输。然而，Prl91 计划在将来实现 MD5 检查。

PC 客户端和安卓 APK 都可以在 XDA 论坛上免费下载，更多信息可以在[应用线程](http://forum.xda-developers.com/showthread.php?t=2307677)中找到。