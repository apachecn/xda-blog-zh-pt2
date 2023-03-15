# 针对 Android 驱动程序问题的三种一体化解决方案

> 原文：<https://www.xda-developers.com/three-all-in-one-solutions-for-android-driver-issues/>

过去的情况是，每当你想在一个设备上使用 ADB 或 FastBoot 时，你需要为每个设备安装一个特定的驱动程序。对于任何经常刷新几个设备的人或在许多不同的手机和平板电脑上测试的开发人员来说，这可能会带来一些不便，尤其是在第一次设置时，必须在 OEM 网站的黑暗角落里寻找正确的驱动程序。谢天谢地，由于这个老问题有几种不同的解决方案，现在事情变得简单了。

你可能还记得我们之前谈论过的 XDA 资深会员 [1wayjonny](http://forum.xda-developers.com/member.php?u=391935) 的[环球裸体司机](http://www.xda-developers.com/android/universal-naked-driver-updated-again-supports-new-nexus-devices/)。这是一个基于 Windows 的工具(兼容 XP、Vista、7 和 8 ),允许您在的 250 多种不同设备上轻松使用 ADB、Fastboot 和(针对华硕设备的)APX。查看上面的链接和[论坛帖子](http://forum.xda-developers.com/showthread.php?t=1161769&usg=3bV9PmMcPfSfH4pmqQzlitUJ2rU.)了解更多关于这个的信息。

在 Universal Naked Driver 的成功基础上，Koush 已经获得了在 UND 线程中收集的设备/供应商 id，并使用它们创建了一个[替代解决方案](https://plus.google.com/103583939320326217147/posts/BQ5iYJEaaEH)，它声称可以在所有 Android 手机和所有版本的 Windows 上工作，可能是 XP 或更高版本。你可以从上面链接的 G+帖子中找到 Koush 的通用 ADB 驱动程序及其源代码。

最后但同样重要的是一个名为[临时 Android 驱动安装程序](https://code.google.com/p/cadi/)的项目，简称 CADI。这是 XDA 资深成员 [jrloper](http://forum.xda-developers.com/member.php?u=4193553) ，的创意，和前面提到的两个选项一样，它试图减轻设备驱动程序的挫折感。然而，与 CADI 不同的是，它完全集成到了 XDA 精英公认的开发商 [AdamOutler](http://forum.xda-developers.com/member.php?u=3682533) 的[休闲](http://www.xda-developers.com/android/casual-for-verizon-galaxy-note-ii-receives-major-update/)中，并采取了稍微不同的方法来解决问题。它使用 Pete Batard 开发的名为 [libwdi](https://github.com/pbatard/libwdi) 的开源 USB 设备驱动安装程序的元素，并在动态生成驱动程序和自动处理安装过程之前，基本上确定哪些设备通过 USB 连接。这是一个很好的例子，三个开源项目在一个辉煌的非专有可爱的三位一体中走到了一起。

因此，如果你仍然被每个设备的单独驱动程序的问题所困扰，那么研究其中一个，或者所有这些选项，肯定是对你最有利的。请在下面的评论中告诉我们你最喜欢的避开司机的方法。