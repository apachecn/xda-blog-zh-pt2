# 在 ADBD 不安全的情况下以 Root 模式运行亚行

> 原文：<https://www.xda-developers.com/run-adbd-in-root-mode-with-adbd-insecure/>

毫无疑问，我们都知道亚行。事实上，我们大多数人经常使用它是为了在我们的移动设备上舒适地使用电脑执行命令。它允许你这样做，如推和拉设备上的文件，检索 logcats 发送到你最喜欢的开发时，你的内核导致引导循环，重新启动恢复或引导加载程序，以及许多其他有用的事情。也是大多数一键 root 方法的核心。最终，是 adbd (ADB 守护进程)负责允许您访问 shell 和所有其他很酷的功能。然而，对于大多数股票内核，这似乎只允许您在安全模式下运行 adb，即使您有一个根设备。

因此，如果你有一个股票内核，并希望拥有所有带有不安全 adbd 的产品(写访问*/系统*的好处和更多)，你可能想看看 XDA 精英公认的开发者 [Chainfire](http://forum.xda-developers.com/member.php?u=631273) 的新版本。他发布了一个 *APK* ，允许你的设备在不安全的模式下运行 adbd，即使你是根用户并且在股票内核上。该应用程序不会永久启用不安全的 adbd，因此会在重启后恢复到标准的 adbd。但是，有一个选项可以在引导时重新启动不安全的 adbd。

如果你正在运行一个定制的内核，你很有可能不需要这个应用。Chainfire 提到，这个应用程序必须安装在根设备上，如果你的设备有锁定的引导加载程序，它可能无法工作。请带它转一圈，给开发者留些反馈。

可以在[原线程](http://forum.xda-developers.com/showthread.php?t=1687590)中找到免费应用。或者，你可以在 Google Play 购买一个[捐赠版](https://play.google.com/store/apps/details?id=eu.chainfire.adbd)。

想在门户网站上发表什么吗？联系任何新闻记者。

[感谢 [Chainfire](http://forum.xda-developers.com/member.php?u=631273) 的提示]