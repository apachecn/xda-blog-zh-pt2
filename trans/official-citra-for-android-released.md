# 官方的安卓版 Citra 作为第一款移动任天堂 3DS 模拟器发布

> 原文：<https://www.xda-developers.com/official-citra-for-android-released/>

我们已经多次报道了任天堂 3DS 在 Android 上的仿真，尽管早期的尝试是通过 PC 上非常流行的 Citra 仿真器的非官方 Android 端口实现的。在这两个非官方端口开发者的帮助下，现在有了一个正式的用于 Android 的 Citra 版本。更重要的是，这个任天堂 3DS 模拟器在谷歌 Play 商店上是免费的！

今天发布的官方端口中有许多最初端口中没有的功能，所有这些功能都提供了一个相当成熟的任天堂 3DS 仿真体验。这包括 amiibo 支持、动作控制、麦克风和摄像头支持以及游戏手柄支持，仅举几例。Citra 3DS 模拟器背后的团队在他们的网站上记录并发布了整个开发过程的故事，其中深入探讨了之前的两个非官方端口如何影响了这个正式版本的开发。如果你还记得第一次在 Android 上模拟 3DS 游戏的尝试，它几乎不起作用，因为它很慢并且有很多问题。第二个(也是正在进行的)[【MMJ】非官方端口](https://www.xda-developers.com/nintendo-3ds-emulator-android-unofficial-citra-port/)在性能方面要好得多，但是普通用户可能会希望坚持使用现在可用的官方版本。

https://www.youtube.com/watch?v=iiH2JtFADV8

我在正式版上做了一些简单的测试，发现任天堂 3DS 游戏如《马里奥赛车 7》和《动物穿越:新叶》在我的由高通骁龙 865 驱动的一加 8 Pro 上运行得非常好。我们还在由高通骁龙 865 驱动的 [OPPO Find X2 Pro](https://forum.xda-developers.com/find-x2-pro) 上玩了一点火徽:命运，它基本上以稳定的 60fps 运行。我们将在周末进行一些更深入的测试，看看 Citra 在许多采用不同芯片组的设备上的可行性如何。目前，Citra 背后的团队建议您的设备使用高通骁龙 835 或更好的，尽管性能也将严重依赖于设备的 GPU 驱动程序。总的来说，高通骁龙设备运行 Citra 的效果会好于三星 Exynos 或海思麒麟设备。您的智能手机还必须至少运行 Android 8.0 Oreo，并支持 OpenGL ES 3.2。在不支持的设备上，您可能会遇到图形故障和其他问题。

左:窃听(球员是透明的)|||右:工作

你可以从下面的谷歌 Play 商店下载 Citra for Android 应用程序。在应用内购买 4.99 美元可以解锁高级功能，目前包括一个黑暗模式主题和一个增加图形保真度的纹理过滤选项。虽然基础应用是免费的，但 Citra 团队要求您通过在 Patreon 上对他们的开发工作做出贡献来支持他们。

以下是努力使 Citra 的 Android 移植成为可能的开发人员:

*   领导这个项目
*   前端(UI)的 [Dolphin 模拟器](https://dolphin-emu.org/)和`Aarch64 machine code emitter`的开发者，我们从他们那里大量借鉴。
*   [BreadFish64](https://github.com/BreadFish64) 用于 OpenGL ES 改进、运动控制支持和纹理过滤。
*   [柳树雨](https://github.com/liushuyu)针对 OpenGL ES 的 bug 修复。
*   最初重新利用 Dolphin UI，添加初始 OpenGL ES 支持，并实现大部分 Aarch64 [dynarmic](https://github.com/MerryMage/dynarmic) 后端。
*   [鸢](https://github.com/FearlessTobi)用于 Amiibo 支持、Mic 支持、翻译、错误修复、从 Dolphin upstream 移植前端更改等等。
*   [微火鸭](https://github.com/weihuoya)用于实现 Android 的 AAC 解码
*   [zhaowenlan1779](https://github.com/zhaowenlan1779) 为软件键盘小程序和摄像头支持实现。

* * *

来源:[雪铁龙](https://citra-emu.org/entry/announcing-citra-android/)