# 在您的手机上添加多用户配置文件支持

> 原文：<https://www.xda-developers.com/add-multiple-user-profile-support-on-your-phone/>

共享平板电脑或手机并不稀奇。手机通常是放松的工具，或者是易于使用的互联网终端，通过它你可以方便地访问网络并与你爱的人保持联系。默认情况下，手机只提供一个用户配置文件，如果你想避免对设备设置的潜在更改或保护你的私人数据隐私，这并不理想。

Android 4.2 操作系统增加了用户资料，但谷歌决定只在平板电脑上提供这项功能。这让手机用户寻找替代解决方案。如你所知，Xposed Framework 可以用来定制你的系统，修改不是设计用来修改的东西。XDA 资深会员 [safet.me](http://forum.xda-developers.com/member.php?u=5074100) 将多用户功能移植到任何带 Xposed 的 ROM 上。该模块完成其工作，并允许在手机上使用多个配置文件，但有两个问题是众所周知的。手机应用程序将无法在新创建的配置文件和模块工程与 AOSP 锁屏只。

要在运行中测试这个模块，请转到[原始线程](http://forum.xda-developers.com/showthread.php?t=2676516)。从那里，抓取 APK，安装它，并在 Xposed Installer 中启用它。重新启动后，您的手机应该支持多个配置文件。