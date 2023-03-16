# 自定义内核修复了一些谷歌像素 4 XL 单元的绿色着色问题

> 原文：<https://www.xda-developers.com/custom-kernel-fix-green-tinting-issues-google-pixel-4-xl-units/>

# 自定义内核修复了一些谷歌像素 4 XL 单元的绿色着色问题

在低亮度下有“绿色色调”问题的谷歌 Pixel 4 XL 用户现在可以使用 XDA 认可的开发商 tbalden 制作的自定义内核来修复该错误。

2019 年的谷歌 Pixel 4 阵容首次在该系列中推出了 90Hz 刷新率的移动显示器，但常规和“XL”变种的面板来自两家不同的制造商。虽然 Pixel 4 配备了 LG 显示屏，但谷歌决定在 Pixel 4 XL 上使用三星制造的面板，这与在[一加 7 Pro](https://forum.xda-developers.com/oneplus-7-pro) 上发现的面板相同。在我们对谷歌 Pixel 4 家族的详细[显示器分析中，XDA](https://www.xda-developers.com/google-pixel-4-4-xl-display-analysis/)[的迪伦·拉加](https://www.xda-developers.com/author/dylan-raga/)指出，由于错误的伽马校准，Pixel 4 XL 上的三星显示器在较低亮度下的色彩饱和度方面存在一些严重缺陷。事实上，如果你在谷歌上搜索“[谷歌像素 4 绿色色调](https://www.google.com/search?q=google+pixel+4+green+tint)，你会发现很多关于屏幕在低亮度水平下呈绿色色调的投诉。

**[谷歌像素 4 XL XDA 论坛](https://forum.xda-developers.com/pixel-4-xl)**

显然，用于 90Hz 显示模式的屏幕校准导致一些用户在低亮度水平下看到绿色色调。这种影响可能不会对每个用户都那么明显，因为大多数人很少在超低亮度水平下使用他们的手机，在这种情况下绿色色彩最明显。然而，一些用户报告了问题确实明显的情况，甚至在更高的亮度水平下。

好消息是，XDA 认可的开发者 [tbalden](https://forum.xda-developers.com/member.php?u=3088420) 已经为[提供了一个新的 CleanSlate 定制内核](https://forum.xda-developers.com/showpost.php?p=82660965)的更新，它将伽马校正值从 60Hz 显示模式应用到 90Hz 模式。内核配套应用程序也收到了一个新的选项，名为“**降低 90Hz 低亮度**”。那些使用应用程序的[高级版本的用户可以通过一个便捷的快速磁贴来切换调整。](https://play.google.com/store/apps/details?id=org.cleanslate.csconfig)

这是开发人员制作的一个视频，展示了他应用修复前后的情况:

开发人员还在这个定制内核中包含了上述 degreenify 模块的替代模块，可以在指定的亮度级别下强制 60Hz。值得一提的是，你应该在“CleanSlate R”分支下下载这个包，而不是“CleanSlate Q”，以防你在你的 Google Pixel 4 XL 上使用 [Android 11 开发者预览版](https://www.xda-developers.com/google-android-11-beta-june-3-2020-developer-preview-4-live-release/)。

**[Google Pixel 4xl 的 CleanSlate 定制内核——XDA 下载讨论线程](https://forum.xda-developers.com/pixel-4-xl/development/kernel-cleanslate-v1-0-0-t4027435)**