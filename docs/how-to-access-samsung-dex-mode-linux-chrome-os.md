# 如何在 Linux 和 Chrome OS 上访问三星 DeX 模式

> 原文：<https://www.xda-developers.com/how-to-access-samsung-dex-mode-linux-chrome-os/>

谷歌还没有在安卓系统中提供一个成熟的桌面界面，但是你可以在一些运行安卓 10 的设备上通过 T2 访问隐藏的准系统版本。另一方面，少数原始设备制造商为[提供他们自己的桌面模式](https://www.xda-developers.com/lgs-android-10-update-desktop-mode-interface/)的实现，而三星的 [DeX](https://www.xda-developers.com/tag/samsung-dex/) 无疑是其中最完美和[功能最丰富的](https://www.xda-developers.com/hands-on-linux-on-samsung-dex-samsung-galaxy-note-9/)选项。三星 DeX 的最新版本甚至可以[与 MAC 和 Windows PCs 无缝集成](https://www.xda-developers.com/galaxy-note-10-samsung-dex-windows-mac-pc/)。

虽然三星确实[将 DeX 的 PC 支持移植到了老款旗舰产品](https://www.xda-developers.com/samsung-galaxy-s9-note-9-dex-pc-support-android-10-update/)，但他们仍然没有提供与这一便捷功能相对应的官方 Linux(和 Chrome OS)配套应用。从使用 Linux 的普通三星用户的角度来看，这意味着如果你有一个外部显示器，你只能访问 DeX 模式。本质上没有操作系统级别的限制，所以 XDA 的高级成员[克迈斯](https://forum.xda-developers.com/member.php?u=388343)决定创建一个概念验证技术，最终作为三星 DeX 的 Linux 客户端。

非官方的方法不需要 root 访问，但你需要一些额外的硬件附件(一个 USB-C 转 HDMI 坞站，加上一个 HDMI“虚拟”终结器)来简化这个过程。还需要三星 Galaxy 设备附带的 USB 电源插头电缆组合。在软件方面，该方法依赖于一个名为 [scrcpy](https://www.xda-developers.com/free-android-mirroring-app-scrcpy-seamless-copy-paste-stay-awake/) 的免费开源项目，它可以帮助你将实际的 DeX 接口从三星手机暴露给运行 Linux 或 Chrome OS 的 PC。此外，您需要在 PC 上设置 Android Debug Bridge(ADB ), scrcpy 将它用作连接隧道。

像剪贴板共享和 APK 文件的拖放安装这样的典型功能在这种方法中没有问题，但是声音路由有点混乱。不过，您可能必须从源代码编译 scrcpy，因为基于 Debian 的操作系统(例如，Ubuntu 和 Chrome OS 上的 [Crostini 环境)的默认包存储库上的可用构建通常是过时的。这一步在 ARM 驱动的 Chrome OS 设备上可能特别成问题，所以选择交叉编译。](https://www.xda-developers.com/linux-apps-chrome-os-overview-crostini/)

**Linux 和 ChromeOS 上的三星 Dex:[教程](https://kmyers.me/blog/android/dexonlinux-dexonchromeos-how-to-no-root/) || [XDA 讨论线程](https://forum.xda-developers.com/galaxy-note-10/development/dexonlinux-dexonchromeos-root-t4111625)**