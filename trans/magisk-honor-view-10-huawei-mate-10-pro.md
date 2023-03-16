# Magisk 现已在 Honor View 10 和华为 Mate 10/10 Pro 上提供

> 原文：<https://www.xda-developers.com/magisk-honor-view-10-huawei-mate-10-pro/>

Magisk 是一款流行的无系统 root 管理器，现在可用于 Honor View 10、华为 Mate 10 和华为 Mate 10 Pro。Systemless root 允许你对系统应用和库进行修改，以实现诸如[音频增强模块](https://forum.xda-developers.com/apps/magisk/magisk-dolby-atmos-r6-5-t3554616)、全系统广告拦截、[字体更改](https://www.xda-developers.com/magisk-blob-emoji-pixel-nexus-oreo/)、[谷歌摄像头端口](https://www.xda-developers.com/google-camera-mod-portrait-mode-lens-blur-4k-video/)在[基本手机上](https://www.xda-developers.com/pixel-2-google-camera-port-essential-phone/)、[夜灯和](https://www.xda-developers.com/enable-night-light-camera2-api-xiaomi-mi-a1-magisk/)[小米 Mi A1](https://www.xda-developers.com/xiaomi-mi-a1-xda-android-review/) 上的 Camera2 API ，甚至允许[完全定制谷歌 Pixel 2 的 Active Edge](https://www.xda-developers.com/customize-google-pixel-2-active-edge-sense-plus/) 。它可以做到这一点，还可以做更多，所有这些都不会触动谷歌的安全网，这意味着你仍然可以在你的根设备上使用 Android Pay。现在最新的华为和 Honor 旗舰设备的所有者也可以享受 Magisk。

* * *

## Magisk for the Honor View 10 和华为 Mate 10/10 Pro

XDA 知名开发商[topjohnwu](https://forum.xda-developers.com/member.php?u=4470081)[刚刚宣布](https://forum.xda-developers.com/honor-view-10/development/magisk-root-honor-view-10-mate-10-pro-t3749280)Magisk 可用于这些设备。 [Honor View 10](https://www.xda-developers.com/honor-view-10-mini-review/) 和[华为 Mate 10 系列](https://www.xda-developers.com/huawei-mate-10-pro-porsche-official/)都采用了最新的[海思麒麟 970 SoC](https://www.xda-developers.com/huawei-kirin-970-soc-details-cortex-a73/) ，这意味着它们的启动映像与大多数基于高通骁龙的设备略有不同。正因为如此，Magisk 从未在任何华为或 Honor 设备上可用——直到现在。

上个月，Honor USA 宣布了 [Honor 开源计划](https://www.xda-developers.com/honor-open-source-program-honor-view-10/)。Honor 承诺向[开发者](https://www.xda-developers.com/honor-announces-developers-honor-view-10-recipients/)和其他人播种 1000 台 View 10 设备，他们的开发努力将有益于 Honor 粉丝群。该公司承诺为该设备发布内核源代码，他们[最终做到了](https://www.xda-developers.com/honor-view-10-kernel-source-code-available/)，现在第一批开发者已经拿到了 View 10，我们开始看到这一举措的成果。

几个小时内，topjohnwu 就让 Magisk 开发了他的 View 10。他在推特上说，他只花了一个小时就找到了设备——这证明了开发者和关键成员实际获得测试设备是多么重要。

随着发布的准备就绪，topjohnwu [在我们的论坛](https://forum.xda-developers.com/honor-view-10/development/magisk-root-honor-view-10-mate-10-pro-t3749280)上宣布，用户现在可以将 Magisk 闪存到他们的设备上。由于官方的 TWRP 尚未在任何搭载 Android Oreo 的华为或 Honor 设备上可用(尽管 XDA 资深公认开发人员 [Dees_Troy](https://forum.xda-developers.com/member.php?u=912474) 正在[进行移植](https://twitter.com/MishaalRahman/status/963525560713523200))，你必须仔细遵循他的指示，以便为 ramdisk 打补丁，然后刷新修改后的 ramdisk。如果偶然出现任何问题，topjohnwu 还慷慨地提供了一个股票 ramdisk 映像作为附件，您可以用它来闪存。至于 Magisk Manager 应用程序，你可以从我们论坛的[常用位置获取。](https://forum.xda-developers.com/apps/magisk/official-magisk-v7-universal-systemless-t3473445)

由于华为 Mate 10、Mate 10 Pro 和 Honor View 10 的 Magisk 处于如此早期的状态，你应该确保你知道如何使用 ADB 和 fastboot 来摆脱任何困境。你们中的大多数人将会等待官方 TWRP 的发布，这很好。不过，如果这种趋势继续下去，我们对 Honor View 10 在定制开发方面的未来感到兴奋。随着 Honor 开源项目的其他开发者收到他们的设备，我们也将报道他们取得的任何进展。