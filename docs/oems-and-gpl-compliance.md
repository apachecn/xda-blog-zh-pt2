# OEM 和 GPL 合规性

> 原文：<https://www.xda-developers.com/oems-and-gpl-compliance/>

在 XDA，我们喜欢开源。事实上，你可以说我们喜欢它。我们有一个 [GPL 政策](http://www.xda-developers.com/android/xda-developers-and-the-gpl/)来确保用户了解遵循 GPL 的最佳方式，并确保其他人可以利用他们的工作来改进我们所有的设备。

然而不幸的是，原始设备制造商经常落后于第三方开发者的努力。虽然一些原始设备制造商的源代码发布非常值得称赞(即[索尼](http://www.xda-developers.com/android/sony-xperia-z-kernel-source-released-prior-to-worldwide-device-launch/)，在[无数](http://www.xda-developers.com/android/an-official-alpha-release-with-kernel-source-who-does-this-sort-of-thing/)场合，超越 GPL 许可，发布 [AOSP 设备树](http://www.xda-developers.com/android/sony-releases-aosp-code-for-xperia-tablet-z-new-httpclient-android-tutorial-available-xda-developer-tv/))，但许多其他原始设备制造商需要更长的时间来发布源代码。但他们最终做到了，为此我们应该为他们鼓掌。

然而不幸的是，最近有许多用户与我们联系，试图提高对一些 OEM 厂商的认识，这些 OEM 厂商不遵守 GPL 许可证，发布带有 Linux 内核的设备，但拒绝发布源代码。在我们接触过的公司中，Micromax 和 Rockchip 是最先想到的两家。

我们的一个论坛成员联系了 [Micromax](http://forum.xda-developers.com/forumdisplay.php?f=2142) 为他们的内核请求 GPL 源代码，得到了如下回复:

> 感谢您的邮件，我们想通知您，我们这边无法提供任何内核源代码。

不幸的是，这位 Micromax 工作人员证实，他们不会提供 GPL 授权的内核源代码，因此承认违反了 GPL。我毫不怀疑一些阅读这篇文章的人将会把代码贡献给主要的 Linux 内核，并且能够对 Micromax 实施他们的版权保护。

关于 Rockchip——常见于“电视棒”式设备中的流行低成本 RK29xx 和 RK30xx 芯片组的制造商，也存在 GPL 合规性问题，具体而言，一些源文件已被删除，仅保留编译后的“目标文件”。这允许从源代码构建内核，但是不能满足 GPL 的全部要求(因为这些目标文件是直接构建到主内核中的)。这可以防止用户修改许多重要的驱动程序。

我们很乐意与 Rockchip 和 Micromax 合作，帮助他们实现 GPL 兼容。除了维护合法性之外，遵循 GPL 的好处还包括能够将来自社区的代码合并回它们的源代码树，从而通过修复节省他们的时间和金钱。不幸的是，两人都没有回复我们的邮件。虽然我们仍然欢迎他们与我们联系(他们可以通过 pulser _(at)_ xda-developers.com 联系)，但似乎双方都无意采取行动。

现在的问题是，社区是否能够创造必要的压力，以确保通过遵守 GPL 来维护法律。在这篇文章发表之前，我们联系了 Micromax，但我们的置评请求没有得到回应。