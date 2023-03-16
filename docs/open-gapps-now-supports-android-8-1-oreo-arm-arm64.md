# Open GApps 现在支持 Android 8.1 Oreo (ARM+ARM64，x86+x86_64)

> 原文：<https://www.xda-developers.com/open-gapps-now-supports-android-8-1-oreo-arm-arm64/>

GApps 包(Google Apps 的缩写)在定制 ROM 开发社区中是必不可少的。GApps 不与 LineageOS 等定制 rom 捆绑的原因是，虽然 LineageOS 是开源的 Android 发行版，但 Google apps 不是开源的。Play Store、Gmail、Maps 等应用程序不使用 Apache 或 GPLv2 许可证。因此，定制 ROM 开发人员不能将它们与他们的构建捆绑在一起，因为这样做会带来法律上的挑战。

多年来，许多不同的 GApps 封装一直很受欢迎。ParanoidAndroid GApps 曾经是使用最广泛的 gapp 之一，但这些包在 2015 年停止使用。同年，Open GApps 试图在 ParanoidAndroid GApps 停止的地方继续前进。

据开发者称，Open GApps 的显著特点是，它完全是通过编写构建脚本来开发的，这些脚本允许自动创建新的更新包。他们的开发过程是开源的，每天(欧洲)晚上都会生成构建。

自从第一次发布以来，Open GApps 逐渐成为最值得推荐的 GApps 包。它允许用户从 ARM、ARM64 和 x86 平台中进行选择，支持的 Android 软件版本从 Android 4.4 KitKat 到 Android Oreo 不等。

最近发布的 LineageOS 15.1 增加了用户对定制 rom 的兴趣。最近在[项目 Treble](https://www.xda-developers.com/tag/project-treble/) 中的发展也意味着，在经历了一个设备越来越被锁定从而抑制了开发的时代之后，开发社区有所期待。LineageOS 15.1 的第一个构建版本于本周发布(基于 Android 8.1 Oreo)，但 OpenGApps 并未提供 Android 8.1 Oreo 的 GApps(具体来说，SetupWizard 仍为 8.0)。

现在这种情况发生了变化，因为 OpenGApps 现在为 ARM、ARM64、x86 和 x86_64 平台提供了 Android 8.1 Oreo 的软件包。

OpenGApps 警告说，Android Oreo 的 GApps 包仍然是“测试版质量”。然而，Android 8.1 Oreo 的 GApps 的发布意味着他们现在可以兼容 LineageOS 15.1 等 Android 8.1 定制 rom。因此，用户不再需要使用不能自动更新的 GApps 软件包。他们可以通过 [TWRP](https://www.xda-developers.com/tag/twrp/) 刷新开放的 GApps 包——需要注意的是，在刷新定制 ROM 之后(重启系统之前)，必须立即刷新 GApps 包，以避免崩溃。

2018 年 3 月 2 日更新:Open GApps 现在也为 x86 和 x86_64 平台提供软件包。

* * *

[**下载 OpenGApps**](http://opengapps.org/)