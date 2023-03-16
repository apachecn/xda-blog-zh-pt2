# FTVLaunchX 支持在 Amazon Fire TV 设备上定制启动器

> 原文：<https://www.xda-developers.com/ftvlaunchx-enables-custom-launchers-on-amazon-fire-tv-devices-without-root/>

亚马逊没有正式生产任何基于安卓系统的智能手机，但是这个电子商务巨头确实有一系列使用安卓系统的产品。例如，亚马逊的 Fire TV 设备运行 Android 的一个分支，名为 Fire OS，上面有亚马逊定制的用户界面。尽管底层软件是基于 Android 的，但亚马逊并没有让用户更容易地定制或调整软件以满足自己的喜好。在我们的 Android 智能手机和平板电脑上，使用第三方启动器是我们理所当然的事情，但在 Fire TV 上，你没有这种自由，因为亚马逊阻止你使用定制启动器。

曾经有一个流行的应用叫做[launcher jacking](https://www.xda-developers.com/amazon-fire-os-custom-launcher-widgets/)来绕过这个限制。该应用程序只是将 Fire TV 遥控器上的 home 键重定向到你选择的第三方启动器。使用 ADB，用户可以禁用股票 Amazon 启动器，有效地用自定义启动器替换股票启动器。

不幸的是，亚马逊推出了一个 Fire OS 更新，阻止了 LauncherHijack 包，还删除了 ADB shell 命令来禁用包，有效地阻止了用户在没有 out 的情况下运行自定义启动器。

幸运的是，XDA 初级成员 [TheRealQubix](https://forum.xda-developers.com/member.php?u=10179237) 已经找到了一个新的解决方法，再次使 Fire TV‌的所有者可以用他们选择的没有 root 的自定义启动器替换默认启动器。被称为 FTVLaunchX 的新解决方案受 LauncherHijackis 的启发，也克服了旧方法的一些问题。

FTVLaunchX 已经在 Fire TV Stick 2 代、 [Fire TV Stick 4K](https://www.xda-developers.com/amazon-fire-tv-stick-4k-miracast-screen-mirroring-support-update/) 和 Nvidia Shield 2017 上成功测试。然而，它也可以在其他模型上工作。要了解这个项目的更多信息，请下载 APK‌并获得如何在 Fire TV 上设置它的分步说明，请访问下面的链接。

* * *

**[为亚马逊 Fire TV](https://forum.xda-developers.com/fire-tv/general/ftvlaunchx-custom-launcher-root-t4037397) 下载 FTVLaunchX】**