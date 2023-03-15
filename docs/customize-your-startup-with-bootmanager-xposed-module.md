# 使用 Bootmanager Xposed 模块定制您的启动

> 原文：<https://www.xda-developers.com/customize-your-startup-with-bootmanager-xposed-module/>

如果你已经安装了很多应用程序，其中很多可能会被设置为在启动时启动。然而，如果你想快速启动或者有更多的空闲内存，这可能不是最佳选择。幸运的是，有几个工具可以用来解决这个问题，现在有一个工具利用了 XDA 公认的开发人员 [rovo89](http://forum.xda-developers.com/member.php?u=4419114) 的神奇的 [Xposed 框架](http://www.xda-developers.com/android/say-goodbye-to-custom-stock-roms-and-hello-to-xposed-framework/ "Say Goodbye to Custom “Stock” Roms and Hello to Xposed Framework") ( [线程](http://forum.xda-developers.com/showthread.php?t=1574401))使安装变得轻而易举。

BootManager 由 XDA 资深会员 [defim](http://forum.xda-developers.com/member.php?u=4501300) 创建，让你轻松定制哪些应用程序允许在启动时启动。要安装该应用程序，您只需从 Xposed 存储库、Xposed 应用程序的回购浏览器或 Google Play 下载 APK。一旦安装完毕，您就可以通过 Xposed 安装程序激活该模块。要使用 BootManager，只需选择不想在启动时启动的应用程序。如果您想查看输出日志文件，只需使用 BootManager 的 grep 查看 */data/xposed/debug.log* 即可。

要使用 BootManager，请访问[模块线程](http://forum.xda-developers.com/showthread.php?t=2432359)。