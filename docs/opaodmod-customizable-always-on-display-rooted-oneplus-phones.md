# 一加手机可以通过 OPAodMod 模块启用“始终显示”

> 原文：<https://www.xda-developers.com/opaodmod-customizable-always-on-display-rooted-oneplus-phones/>

# OPAodMod 是一个可定制的始终显示植根于一加手机

想试试总是显示在你的一加手机上吗？OPAodMod，一个允许你启用它的 Xposed 模块，得到了一个大规模的更新。看看吧！

一加在 OnePlus 6 的[初始工厂固件上简要介绍了一个永远显示(AOD)功能，但由于电池问题](https://www.reddit.com/r/oneplus/comments/8mgznp/do_you_want_always_on_display/)决定稍后[将其移除。粉丝们一直呼吁该功能回归，该公司最近](https://www.xda-developers.com/oneplus-6-update-hide-notch-slow-motion-video/)[证实](https://www.xda-developers.com/oneplus-will-finally-bring-an-always-on-display-mode-to-oxygenos/)他们最终将把粉丝最喜欢的永远显示模式带回 OxygenOS，但尚未给出具体的时间表。正如所料，XDA 社区前来救援，因为 XDA 认可的开发者 [Quinny899](https://forum.xda-developers.com/member.php?u=3563640) 已经发布了 *OPAodMod* ，这是一个曝光的模块，为一加手机提供了谷歌像素式的 AOD 功能。

看着眼熟？好吧，我们确实在 2019 年 7 月[报道了这个模块](https://www.xda-developers.com/xposed-module-pixel-always-on-display-oneplus/)的初始版本。然而，它在一段时间后停止接收更新，因为开发者放弃了支持。XDA 公认的开发者 [Quinny899](https://forum.xda-developers.com/member.php?u=3563640) 已经开始了 mod 的工作，甚至设法获得了完整的源代码。从那时起，整个模块已经从中文翻译成英文，同时添加了一个新的 GUI 来定制 UI 元素。该模块还完全兼容运行 OxygenOS 和 HydrogenOS 的一加设备。

完整的特性列表可以在下面找到。

*   不像一加版本，它一直都在显示
*   可定制的布局，选项包括三种数字时钟风格，双字时钟和一个 DVD 屏幕保护程序(这正是你认为它是什么)
*   通知显示，当您收到通知时显示通知文本，几秒钟后返回到图标
*   选择只在你“举起”手机时显示
*   选项隐藏屏幕时翻转/在你的口袋里，禁用它过夜，或在一段时间后(10 分钟或 15 秒)
*   显示您的下一个闹钟、当前天气和当前播放的音乐
*   显示一条短消息(就像锁屏上显示的那样)
*   模块的完整设置 GUI，带有时钟的实时预览

**[OPAodMod — XDA 下载讨论线程](https://forum.xda-developers.com/oneplus-7t/oneplus-7t-7t-pro-cross-device-themes-apps--mods/xposed-opaodmod-display-lots-options-t4100981)**

由于 OPAodMod 依赖于 Xposed 框架，所以在使用 Magisk 对您的设备进行根操作后，您需要结合使用 Riru Core (建议使用最新的 Canary 版本)或使用 [TaiChi](https://taichi.cool/doc/) 的 [EdXposed 来安装该模块。OPAodMod 的当前版本(3.0 版)带有老化保护，即它偶尔将内容移动几个像素，开发者正在努力最小化电池消耗。试试看！](https://www.xda-developers.com/xposed-framework-unofficial-port-android-pie/)