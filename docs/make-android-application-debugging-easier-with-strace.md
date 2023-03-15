# 使用 STrace 简化 Android 应用程序调试

> 原文：<https://www.xda-developers.com/make-android-application-debugging-easier-with-strace/>

Logcat 是一个强大的诊断工具，旨在帮助开发人员调试应用程序中的错误。没有它，修复大多数应用程序将会非常困难。然而，logcat 似乎并不是应用程序开发人员唯一可用的诊断工具。

现在，有一个由 XDA 资深会员 [alireza7991](http://forum.xda-developers.com/member.php?u=4825267) 移植的替代工具。STrace 是一个调试工具，用来监控程序的系统调用或它接收到的信号。与 logcat 不同，Strace 可用于监控单个应用程序，因此更容易发现异常行为。该工具可用于查找崩溃或异常的原因。

使用 STrace 非常简单。你所需要做的就是把 bin 文件推送到你设备上的 */system/bin/* ，用 chmod 设置正确的权限。然后，您可以从终端模拟器或 ADB shell 运行它。

如果您对一款新的调试软件感兴趣，请访问[实用线程](http://forum.xda-developers.com/showthread.php?t=2516002)，了解更多关于 STrace 的信息。