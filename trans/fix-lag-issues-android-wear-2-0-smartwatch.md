# 如何潜在地修复 Android Wear 2.0 智能手表的滞后问题

> 原文：<https://www.xda-developers.com/fix-lag-issues-android-wear-2-0-smartwatch/>

自从升级到 Android Wear 2.0 以来，许多用户都报告了严重的速度变慢，设备严重滞后，有时似乎会死机。通常，唤醒设备屏幕并试图向上滑动通知卡会使手表在短时间内缓慢、不可用。许多菜单滞后，几乎做任何事情都会使设备几乎无用。

谢天谢地，一个名叫[yozakkg](https://www.reddit.com/user/Yozakgg)的 Reddit 用户已经[发现了](https://www.reddit.com/r/AndroidWear/comments/7igeql/psa_for_huawei_watch_2_owners_disabling_ok_google/)如何修复这个问题，而且方法相对简单。为什么会这样？“确定谷歌”检测。用户甚至不需要 root 权限来修复这个问题——任何人都可以在他们的 Android Wear 2.0 手表上修复禁用这个功能，如果它滞后的话。起初，它似乎只在华为 Watch 2 上有效，但后来的报告显示，所有 Android Wear 2.0 手表都可能遇到该问题。

## 如何修复 Android Wear 2.0 上的滞后问题

修复很简单，因为我们只是要禁用“确定谷歌”热词检测。只需导航至**设置>个性化**，然后向下滚动并禁用“Ok Google detection”，如下图截图所示。

就是这样！你要做的就是这些。不需要额外的软件，不需要 ADB 访问，也不需要设备上的 root 访问。这只会禁用大声说出“Ok Google”并触发手表的始终监听功能。如果你想激活语音搜索，按住电源按钮激活功能仍然有效，所以总体而言，这一设置变化应该不会对 Android Wear 智能手表的功能产生太大影响。

Reddit 用户通过运行“adb shell top”命令找到了修复方法，该命令列出了他们的 Android Wear 2.0 智能手表上正在运行的进程，如下面的截图所示。他们发现最上面运行的进程是 Google 应用程序，因此它消耗了大量的资源。

这是一个需要了解的有用命令，因为它可以帮助用户调试在任何给定时间从设备中消耗最多 CPU 功率(从而延长电池寿命)的命令。它可以在智能手表和安卓手机上运行。如果你的 Android Wear 2.0 智能手表饱受滞后之苦，不妨一试！