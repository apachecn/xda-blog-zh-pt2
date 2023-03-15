# Android Generic 项目旨在为您的 PC 带来定制的 rom

> 原文：<https://www.xda-developers.com/android-generic-project-custom-roms-pc/>

除了智能手机和平板电脑，你可以在你的[智能电视](https://www.xda-developers.com/tag/android-tv/)、[智能手表](https://www.xda-developers.com/google-announces-wear-os-based-on-android-11-new-version-snapdragon-wear-4100-support/)、[汽车](https://www.xda-developers.com/tag/android-automotive/)以及其他各种形状和大小的设备中找到安卓操作系统。然而，当涉及到 x86 PCs 的世界时，谷歌正努力推动 Chrome 操作系统。令人欣慰的是，Android 的开源特性和多功能性允许开发人员释放操作系统的全部潜力，并将其移植到 x86(-64)设备上。 [Android-x86](https://www.xda-developers.com/tag/android-x86/) 项目是这一领域的先驱，它也是许多分支的基础，如 [Remix OS](https://forum.xda-developers.com/remix) ( [不再支持](https://www.xda-developers.com/jide-pulling-the-plug-on-remix-os-as-it-focuses-on-enterprise-markets/))和 [Bliss OS](https://www.xda-developers.com/bliss-os-android-for-x86-android-10/) 。Bliss OS/BlissRoms 项目背后的开发团队现在已经提出了一个有趣的工具包，它将彻底改变任何定制 ROM 到 PC 平台的移植过程。

被称为“Android-Generic Project”的整个想法非常类似于 [Project Treble](https://forum.xda-developers.com/project-treble) 的概念以及 Android 的相关[模块化。Bliss OS 开发人员现在正在修改他们的构建脚本，以便人们可以轻松地将典型的定制 ROM 的代码库集成到他们的 x86 PC 专用树(以前称为“Android-PC 项目”)的顶部。那些熟悉 AOSP](https://www.xda-developers.com/googles-project-treble-modularize-android-so-oems-can-update-devices-faster/) [通用系统映像](https://www.xda-developers.com/flash-generic-system-image-project-treble-device/) (GSIs)的人应该很容易注意到相似之处，因为事实上，Android 通用项目在很大程度上是受 XDA 公认的开发者 [phhusson](https://forum.xda-developers.com/member.php?u=1915408) 的定制 GSI 生成脚本的启发。

这是 BlissRoms 团队成员 Jon West 发布的一个短视频，又名 XDA 公认的贡献者 [electrikjesus](https://forum.xda-developers.com/member.php?u=928479) ，展示了使用 Android 通用工具包编译的[肮脏独角兽](https://www.xda-developers.com/dirty-unicorns-back-xda-roms-google-pixel-phones/)的构建:

Android-x86 仍然被用作底层基础，但已经引入了智能预补丁阶段，以消除不同定制 rom 中的冗余补丁。一旦解决了所有的补丁冲突，生成的构建清单应该足以生成一个供应商报告，只需要在最终的构建过程之前将其克隆到 AOSP 或定制 ROM 源中。简而言之，从现在开始，在你的个人电脑上启动像 [CarbonROM](https://twitter.com/electrikjesus/status/1295489622781440010) 这样的定制 ROM 就不需要你紧张了。

值得一提的是，Bliss OS 构建现在是使用 Android 通用构建脚本编译的，这很好地表明了该项目在当前阶段的稳定性。除了 Dirty Unicorns 和 CarbonROM，你还可以在下面的链接中找到 vanilla AOSP、Tesla OS 和 Pixel Experience for PC 的开发中版本。如果你有兴趣将特定的定制 ROM 移植到 PC 上，你可以在[git lab repo](https://gitlab.com/android-generic)中找到所需的工具、文件和文档。

**[安卓-通用项目-XDA 下载讨论线程](https://forum.xda-developers.com/android/software/pc-gsi-build-automation-toolkit-t4132031/)**

* * *

**来源: [BlissRoms 博客](https://blog.blissroms.com/2020/06/26/lets-try-and-change-the-game/)**