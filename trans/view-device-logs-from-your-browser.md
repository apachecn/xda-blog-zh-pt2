# 从浏览器查看设备日志

> 原文：<https://www.xda-developers.com/view-device-logs-from-your-browser/>

如果您经常使用 logcats 无论是为了开发还是为了报告 bugs 那么您应该已经熟悉了检索它们有多麻烦。我们之前报道了一种创新的、针对平板电脑优化的本地查看日志的方法。现在，XDA 的高级成员 [_miha_](http://forum.xda-developers.com/member.php?u=2554465) 开发了一个应用程序，允许通过网络浏览器查看日志，使这个过程变得更加容易。

Remote Logcat 顾名思义，允许您通过互联网浏览器查看您的 Android 设备日志，可以是实时的，也可以是通过查看以前创建的日志。这消除了对 USB 电缆和 SDK / ADB 设置的需要。此外，它甚至不需要 root 访问权限。该应用程序还允许您将 apk 文件直接发送到设备来更新应用程序。该应用程序非常适合那些可能不在家并希望进行一些调试的开发人员，以及寻找简单方法创建日志的用户。然而，开发者确实提到日志过滤目前有些麻烦。

该应用程序的其他功能包括:

*   按意图触发日志记录
*   当没有互联网连接时，通过短信触发日志记录
*   将日志保存到 SD 卡或通过网络/电子邮件分享*

*分享功能需要开发者的另一个免费应用， [Autoshare](http://forum.xda-developers.com/showthread.php?t=1135180) 。

该应用可从[原线程](http://forum.xda-developers.com/showthread.php?t=1523852)免费获得，需要 Android 1.5 以上版本。