# 如何在 POCO F1 或任何其他小米手机上启用 MIUI 的黑暗模式

> 原文：<https://www.xda-developers.com/miui-10-dark-mode-poco-f1-xiaomi/>

小米一直在为几款设备测试 MIUI 上的全系统黑暗模式。Redmi Note 5 (Note 5 Pro 在印度)已经在[稳定版本](https://www.xda-developers.com/android-pie-miui-10-beta-xiaomi-mi-note-3-redmi-note-5-pro-redmi-6-pro/)中提供了该功能，而包括 Mi 8 在内的许多其他受支持的设备早在五月份就通过 [MIUI 全球测试版](https://c.mi.com/thread-2126580-1-1.html) ROM 获得了该功能。 [POCO F1](https://www.xda-developers.com/xiaomi-poco-f1-design-display-gaming-performance-review/) ，也许是小米最近最吸引人的预算旗舰，也将在即将到来的更新中与红米 Note 7 Pro 一起获得黑暗模式-如果不是 MIUI 10，那么肯定是 MIUI 11。

**[POCO F1 XDA 论坛](https://forum.xda-developers.com/poco-f1)**

与此同时，XDA 高级成员 [TrippyEngine](https://forum.xda-developers.com/member.php?u=8317367) 告知我们一个后门，可以在 POCO F1 或任何其他运行稳定版本 MIUI 10 global ROM 的小米智能手机上启用全系统黑暗模式。它要求你运行一个简单的 ADB shell 命令，这种方法甚至可以在不启动小米智能手机的情况下工作。确保你已经在你的电脑上安装了 [ADB 驱动](https://www.xda-developers.com/install-adb-windows-macos-linux/)，并且开启了 USB 调试。

要在 MIUI 10 上启用全系统黑暗模式，请输入命令:

`**adb shell settings put secure ui_night_mode 2**`

要在 MIUI 10 上禁用黑暗模式，请输入:

**T2`adb shell settings put secure ui_night_mode 1`**

要在夜间自动打开黑暗模式，在白天自动关闭，请使用:

`**adb shell settings put secure ui_night_mode 0**`

更新:正如许多用户在下面的评论中指出的，你可能直到重启智能手机才能看到变化。

随着 [Android Q](https://www.xda-developers.com/tag/android-q/) ，开启黑暗模式的选项[将被原生添加到 Android](https://www.xda-developers.com/android-q-toggle-dark-theme/) 中。由于小米[已经在 MIUI 10](https://www.xda-developers.com/xiaomi-miui-10-global-beta-dark-theme/) 全球测试版中引入了该功能，我们希望 MIUI 10 不仅基于 Android Pie，还基于奥利奥，应该会得到黑暗模式切换。小米已经证实，全系统黑暗模式将成为 MIUI 11 的组成部分。

根据之前的报道，MIUI 的测试版黑暗模式描绘了通知阴影，最近菜单，设置和系统应用程序，如拨号器，联系人，相机，画廊，笔记，屏幕录制器，更新程序，计算器和 SIM 工具包。用上面的方法，你应该能够在上面列出的所有应用程序中切换黑暗模式。

如果你在其他应用上发现了黑暗主题，请务必在评论中告诉我们。