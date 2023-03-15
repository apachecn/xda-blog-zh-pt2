# Magisk v14.5 Beta 发布，支持 Pixel 2 (XL)等！

> 原文：<https://www.xda-developers.com/magisk-v14-5-beta-released-pixel-2-xl-xiaomi-mi-a1-support/>

# Magisk v14.5 Beta 发布:Pixel 2 (XL)支持，修复小米米 A1 支持和更好的 MagiskHide！

Magisk v14.5 已经发布，它对 MagiskHide 的工作方式和对包括 Pixel 2 (XL)在内的新设备的支持做出了很多改变！

Magisk 由知名开发者 [topjohnwu](https://forum.xda-developers.com/member.php?u=4470081) 创建，已经更新到 Magisk v14.5 beta，离稳定版 15 越来越近了。这个版本本来是正式的稳定版本，但测试人员建议它是一个测试版，因为有很多变化。

Magisk v14.5 带来了许多潜在的变化，以及对 Pixel 2 和 Pixel 2 XL 的官方支持和更好的 MagiskHide 版本。您可以在下面查看完整的变更日志。

## 神奇 v14.5 变更日志

*   [守护程序]将内部路径移动到/sbin/。核心，[新的](https://www.ebay.com/sch/i.html?_nkw=new)映像挂载点是/sbin/。核心/img
*   [MagiskSU]支持切换包名，在 Magisk 管理器隐藏时使用
*   [MagiskHide]添加临时/magisk 删除
*   [magis hide]上述所有更改都有助于隐藏讨厌的应用，如 FGO 和几个银行应用
*   [Magiskinit]对所有设备使用 Magiskinit(动态 initramfs)
*   [Magiskinit]修复小米 A1 支持
*   [Magiskinit]添加像素 2 (XL)支持
*   [Magiskboot]添加对删除 dtbo.img 中 avb-verity 的支持
*   [Magiskboot]修复处理 MTK 启动映像头时的打字错误
*   [script]随着 Magisk Manager 的更新，增加了对签名启动映像的支持(AVB 1.0)
*   [脚本]添加 dtbo.img 备份和恢复支持
*   [杂项]许多小调整，以正确支持旧平台，如 Android 5.0

MagiskHide 采用了两种不同的方法来尝试欺骗设备上的检测算法，如 SafetyNet API。第一个更改是更改 Magisk Manager 的包名(如果您启用了隐藏它),以便对检查包 id 的应用程序隐藏它。除非万不得已，否则不建议这样做。第二个实际上已经将/Magisk 挂载点移动到/sbin/.core。这意味着任何模块都不应该再使用/Magisk 作为硬编码的访问点，因为这些模块将无法在 Magisk 的最新版本上工作(无论是测试版还是发布后的版本 15)。

新设备也将受益于 magiskinit 的加入。现在，它可以在刷新后检测它运行在什么设备上，并根据它运行在什么设备上，动态地注入它需要进行的更改。这意味着所有设备的安装是统一的，并将进一步提高兼容性！

然而 **Magisk v14.5 在很多方面都有缺陷**，开发人员要求更大的样本量来找出到底哪里出了问题。更改 Magisk 的软件包名称通常会导致它完全放弃根访问，同时在 NDK r16 的一加、三星和其他设备的日志中也会出现错误消息，试图调用 su。像素 2 也显示了一个弹出窗口，显示 avb-verity 关闭，但是，这不是一个严重的问题，也没什么好担心的。

如果您对 Magisk v14.5 测试版感兴趣，请查看下面的 XDA 线程，以便在您的设备上显示它！

* * *

[**魔法 v14.5 下载**T3](https://forum.xda-developers.com/apps/magisk/beta-magisk-v13-0-0980cb6-t3618589)