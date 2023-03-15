# 由于项目 Treble，Honor 8 Pro 和 Honor 9 获得 AOSP 安卓奥利奥 rom

> 原文：<https://www.xda-developers.com/honor-8-pro-honor-9-aosp-android-oreo-rom-project-treble/>

谷歌去年宣布了“三倍计划”( Project Treble )( T1 ),试图改变设备制造商更新智能手机的方式。搭载 Android Oreo 的手机需要兼容，但是对于 OEM 厂商来说,[可以选择为老款智能手机提供三重 Oreo 更新支持。三重支持的一个潜在好处是，主要软件更新可以更快地到达支持它的设备，因为设备制造商可以更新 Android 框架，而不必等待供应商更新他们的代码。不过，由于 Project Treble 的要求，每台支持它的设备都必须能够启动 AOSP 的通用版本，这使得将 AOSP 带到某些设备上变得容易得多，如 Honor 8 Pro 或 Honor 9。](https://www.xda-developers.com/why-current-oneplus-nokia-phones-wont-be-project-treble-certified/)

在 11 月，我们向您展示了 Project Treble 如何让开发人员创建一个可以在多个设备上启动的[单一系统映像](https://www.xda-developers.com/how-project-treble-revolutionizes-custom-roms-android-oreo/)。华为 Mate 9 等设备现在可以运行 AOSP Android Oreo T3，这是以前没有实现的事情。在支持 Project Treble 方面，华为一直领先于 Android OEMs 厂商，因为该公司已经在所有的奥利奥更新(仍在进行中)中包括了 Treble 支持。华为 Mate 10 Pro [等已经搭载 Android Oreo 的设备也可以轻松运行 AOSP Android Oreo](https://www.xda-developers.com/project-treble-aosp-android-oreo-huawei-mate-10-pro/) 。

现在，XDA 公认的贡献者 [surdu_petru](https://forum.xda-developers.com/member.php?u=2335078) 已经为 [Honor 9](https://forum.xda-developers.com/honor-9) 发布了 OpenKirin 的 AOSP Android Oreo，XDA 公认的开发者 [OldDroid](https://forum.xda-developers.com/member.php?u=4960686) 也为 [Honor 8 Pro](https://forum.xda-developers.com/honor-8-pro) 发布了相同的。OpenKirin 是一个为华为/Honor devices 开发 ROM 的知名团队，值得注意的是，该 ROM 基于 AOSP 的通用构建，这要归功于 Project Treble。

AOSP Treble Oreo 定制 rom 基本上是准系统 AOSP，已经包含了超级用户二进制文件——用户只需要安装由 XDA 资深会员 [phhusson](https://forum.xda-developers.com/member.php?u=1915408) 开发的超级用户应用程序，就可以启用超级用户访问。它还配备了**股票 EMUI 相机**，这是由 [phhusson](https://forum.xda-developers.com/member.php?u=1915408) 修改的[让它工作，尽管大多数股票相机功能工作，有些可能不工作。指纹手势、谷歌像素动画、XPe 浏览器和 Nano Gapps 也包括在内。](https://forum.xda-developers.com/project-treble/trebleenabled-device-development/huawei-stock-camera-app-treble-roms-t3735169)

那么什么坏了？实际上，不多。在开发人员的帖子中列出的唯一问题是 2G/3G 信号条将总是以最大强度显示。此外，你不会通过这个版本的安全网，所以没有 Android 支付很遗憾。尽管如此，对于第一次在设备上发布的 AOSP 版本来说，已经有如此多的功能令人印象深刻。但这就是高音项目对你的魔力。以下是如何将构建安装到您的手机上。

## 如何在 Honor 8 Pro 和 Honor 9 上安装 AOSP 安卓奥利奥 ROM

以下说明相当简短，因为在尝试刷新设备之前，您应该已经对修改设备有所了解。

1.  这第一步非常非常重要:**你必须已经在运行 EMUI 8/Android Oreo 更新**。如果你还没有收到更新，你可以按照[的这个指南](https://forum.xda-developers.com/honor-9/how-to/stf-l09c432-how-to-install-oreo-h9-t3707729)获取荣誉 9 或者[的这个指南](https://forum.xda-developers.com/honor-8-pro/how-to/oeminfo-c432-t3625886)获取荣誉 8 Pro。
2.  **解锁您设备的引导程序**。
    1.  在此请求解锁码
    2.  转到开发者选项并启用 USB 调试
    3.  在您的 PC 上设置 [ADB 和 Fastboot 二进制文件](https://www.xda-developers.com/install-adb-windows-macos-linux/)。
    4.  重启进入快速启动模式，然后在命令提示符或终端中输入`fastboot oem unlock [code]`。
3.  从相应的线程下载 Treble ROM zip 并解压缩。前往[此处](https://forum.xda-developers.com/honor-8-pro/development/rom-t3714728)获取荣誉 8 Pro，前往[此处](https://forum.xda-developers.com/honor-9/development/rom-t3739568)获取荣誉 9。
4.  重新启动引导程序。
5.  在解压文件的目录中打开命令提示符或终端，输入以下命令:`fastboot flash system system.img`
6.  进入库存恢复并执行**工厂重置**。

这样做之后，你应该在你的 Honor 8 Pro 和 Honor 9 上启动一个 AOSP 版本的 Android Oreo。现在，AOSP 没有太多的功能，这些 rom 首先关注的是稳定性，所以你会错过相当多的功能。为了帮助你做到这一点，这里有一些建议。

### 安装高音 ROM 后要做什么

我建议您安装以下应用程序:

Substratum 应该覆盖你所有的主题化需求，而 e Xposed Framework 和 GravityBox 应该给你大部分你所缺少的自定义 ROM 特性。像夜灯、自适应亮度和环境显示这样的东西目前正在研究中，因为它们需要安装在/vendor 中的 RRO 框架覆盖，但它应该很快就会可用。与此同时，你可以安装 [Lux](https://play.google.com/store/apps/details?id=com.vitocassisi.luxlite) 、 [CF.lumen](https://play.google.com/store/apps/details?id=eu.chainfire.lumen) 和 [ACDisplay](https://play.google.com/store/apps/details?id=com.achep.acdisplay) 等应用来复制这些功能。

*GravityBox exposed 模块提供的功能足以取代定制 ROM*

如果你有兴趣了解与 Project Treble 相关的所有最新进展，那么看看我们下面这个主题的专门论坛。

[**查看我们的项目三宝发展论坛**](https://forum.xda-developers.com/project-treble/trebleenabled-device-development)