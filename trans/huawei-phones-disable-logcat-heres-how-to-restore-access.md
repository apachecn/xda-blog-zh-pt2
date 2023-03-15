# 华为手机禁用 Logcat，以下是恢复访问的方法

> 原文：<https://www.xda-developers.com/huawei-phones-disable-logcat-heres-how-to-restore-access/>

当我在帮助 XDA 公认的开发人员和门户作家同事 GermainZ 调试我们正在开发的一个新应用程序(我们认为你们会喜欢它)时，我需要 T2 收集和阅读一个日志来找出哪里出错了。在我的手机上，我安装了 XDA 初级会员[plusculused](http://forum.xda-developers.com/member.php?u=6820962)的 [MatLog](http://forum.xda-developers.com/android/apps-games/app-matlog-1-0-0-beta-material-logcat-t3155566) ，这样我就可以开始调试过程了。我继续前进，授予了应用程序访问日志所需的权限，然后在我们一直在测试的应用程序中复制了一个错误。

当我仔细查看日志时，我注意到实际上几乎没有显示任何相关内容。通常，您会看到大量日志充斥屏幕，以至于您需要设置一个过滤器来开始调试，但是 MatLog 只向我显示了几行。我开始在网上寻找，发现许多其他用户想知道为什么他们不能收集任何日志——他们都在使用华为的手机。据推测，他们禁用日志记录的原因是为了略微提高性能(正如您将看到的一些自定义内核所做的那样)，但是在性能提升如此之小的情况下禁用这样一个主要的调试工具有点令人惊讶。**下面是如何重新启用日志猫。**

* * *

**华为秘密调试菜单**

显然，华为的安卓手机上有一个秘密的调试菜单...几年了。用户最初抱怨华为的 Ideos x3 缺乏[日志记录，这是在 2011 年 2 月宣布的。最终有人找到了一个解决方案，这个方案被分享到了我们自己的论坛上...对于](http://pzieye.centelia.net/blaze/viewtopic.php?pid=124#p124)*[三星 Galaxy S](http://forum.xda-developers.com/showpost.php?p=17774443&postcount=8)* ...这个解决方案最终在 2012 年发展到了[堆栈溢出](https://stackoverflow.com/questions/2250112/why-doesnt-logcat-show-anything-in-my-android)。然后在一年后的 2013 年，在[堆栈溢出](https://stackoverflow.com/questions/18124334/huawei-logcat-not-showing-the-log-for-my-app)上再次引用*。是啊。不管怎样，解决办法是这样的。*

 *打开您的拨号器应用程序，并输入以下代码:

`*#*#2846579#*#*`

你不需要按拨号键，因为输入这个代码会立即显示一个名为**项目菜单**的设置页面。在这里，你有几个菜单可以浏览。

`Here's a brief explanation of each page:`

1.  **背景设置** -我们感兴趣的页面。在这里，您可以更改调试设置、USB 连接设置和“设置 UI 主题颜色”(我不完全确定这个选项的功能是什么)。
2.  **单板信息** -设备软硬件的详细信息
3.  **网络信息查询** -关于设备和 SIM 卡网络功能的详细信息
4.  **软件升级** -从 SD 卡应用更新
5.  **恢复工厂** -工厂重置
6.  **电池充电** -电池信息和长期电池寿命的建议充电水平

进入后台设置页面，你会看到几个选项。点击“日志设置”,弹出一个对话框，提供选择日志级别的选项。选中所有 3 个选项以启用完整日志记录。您将看到一条提示消息，指出启用这些日志记录选项“会影响性能”，但是您可以安全地忽略这条警告。完成后，重启手机。您现在应该能够在您的华为手机上收集日志了。现在出去[帮助我们的开发者](http://forum.xda-developers.com/android/apps-games)调试他们的应用程序吧！*