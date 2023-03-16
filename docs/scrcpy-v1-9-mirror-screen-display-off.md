# Scrcpy v1.9 可以镜像您的屏幕，即使显示器关闭

> 原文：<https://www.xda-developers.com/scrcpy-v1-9-mirror-screen-display-off/>

就移动集成而言，微软的 Windows 10 Insider 版本一直在突飞猛进。你的[手机](https://www.xda-developers.com/microsoft-your-phone-android-windows-10/)应用变得越来越功能丰富，现在支持通过 Wi-Fi 和[移动数据](https://www.xda-developers.com/microsoft-phone-app-syncing-notifications-mobile-data/)同步[通知](https://www.xda-developers.com/windows-10-insider-build-syncing-notifications-with-android/)。您的手机还支持[屏幕镜像](https://www.xda-developers.com/windows-10-android-app-mirroring-insider-build/)，尽管只支持部分设备。你的手机更像是一个连接你的手机和你的电脑的无所不包的解决方案，是微软官方的连接解决方案。但是其他的解决方案已经存在很长时间了。屏幕共享的一个解决方案是 [scrcpy](https://www.xda-developers.com/scrcpy-control-android-on-pc/) 。

scrcpy 于 2017 年 12 月首次出现在 GitHub 上，允许用户从 Windows 控制和查看 Android 设备。这是一个神奇的应用程序，通过 USB 连接无缝工作。好处是你可以用鼠标和键盘控制你的整个设备，你可以在更大的屏幕上显示你的手机。控制是实时的，几乎没有输入延迟。它通过在 Android 设备上执行服务器来工作，然后通过 ADB 隧道经由套接字与 PC 通信。该程序不需要你的设备是根，只是有开发者选项启用，允许 USB 调试打开。

现在，开发者 rom1v 发布了 scrcpy 版本。此次更新中最大的新功能是 scrcpy 现在可以在显示器关闭时镜像您的设备屏幕。值得注意的是，屏幕实际上并没有关闭，也就是说，如果你的手机有永远显示功能，它不会显示出来，所以手机没有被锁定，只是屏幕没有显示任何东西。此次更新还包括几项生活质量的改进，如设备到计算机剪贴板复制，反之亦然。除此之外，还增加了鼠标焦点点击进入功能，这意味着如果窗口不在焦点上，你不再需要点击来使它回到焦点上，然后再次点击来控制你的设备。一次点击就足够了。

Scrcpy v1.9 现在可以在 GitHub 上获得[，尽管 1.9 还没有官方的预建档案。然而，如果你想走这条路，有手动构建应用程序的说明，这并不太复杂。](https://github.com/Genymobile/scrcpy/tree/v1.9)

**变更日志:**

*   添加镜像时关闭屏幕的功能
*   添加设备到电脑剪贴板副本
*   添加计算机到设备剪贴板副本
*   在 Windows 的正确目录中找到 scrcpy-server.jar
*   修复鼠标焦点点击链接
*   聚焦丢失时不要最小化窗口
*   禁用 X11 合成器旁路
*   在失败的字符上继续文本注入
*   将 Home 键绑定到 MOVE_HOME 而不是主屏幕
*   如果不支持展开/折叠面板，请不要崩溃
*   如果设置了- no-control，请勿打开设备电源
*   改进帧速率计数
*   添加运行时选项以渲染过期帧(即不跳过帧)
*   在 Windows 版本中将 SDL 降级到 2.0.8
*   在 Windows 版本中将 FFmpeg 升级到 4.1.3
*   在 Windows 版本中将平台工具升级到 29.0.1 (adb)