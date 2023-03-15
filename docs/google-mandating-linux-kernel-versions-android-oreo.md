# 谷歌正在 Android Oreo 中强制推行 Linux 内核版本

> 原文：<https://www.xda-developers.com/google-mandating-linux-kernel-versions-android-oreo/>

# 谷歌正在 Android Oreo 中强制推行 Linux 内核版本

从今年的 Android Oreo 开始，谷歌现在强制要求所有在 2017 年产品化的 SOC 必须使用内核 4.4 或更新版本。

近十年来，谷歌一直将 Android 作为移动操作系统提供。该公司在 2005 年收购了它，在 2007 年向公众推出了它，然后在 2008 年我们看到了第一款商用 Android 智能手机。谷歌有一些规则和限制，允许一家公司使用 Android 的主要配置(他们过去曾面临法律诉讼)，但在大多数情况下，他们让公司在某些方面自由支配。OEM 一直关注的一个方面是 Linux 内核版本，但随着 Android Oreo 的出现，这种情况正在发生变化。

只要原始设备制造商能够通过谷歌制定的认证测试，他们就不会关心新设备使用的内核版本。这通常不是问题，因为大多数 OEM 会使用与其他 OEM 使用的相同版本的内核，因为它与硬件驱动程序支持的内容密切相关。然而，有些已经被遗漏了，这开始引起安全问题。这是谷歌最近一直在认真对待的事情，所以他们想要开始强制执行这一点是有道理的。

当我们看一下 kernel.org，我们可以看到 3.18 版本的 Linux 内核已经停产。从今年开始，搭载 Android Oreo 的智能手机，谷歌要求所有在 2017 年产品化的 SOC 必须采用内核 4.4 或更新版本。这个版本的 Linux 内核不仅更安全，而且也意味着公司不需要投入太多的资源来保证它的安全。虽然使用较新的内核版本并不能保证所有的漏洞都会被发现，但它确实有助于减少漏洞的数量，并减少需要投入到反向移植安全修复中的工作。

谷歌还要求与 Android Oreo 一起推出的新设备从一开始就支持 Project Treble,这有望使未来升级 Linux 内核版本变得更容易，并减少需要投入到安全补丁的工作。目前升级到 Android Oreo 的现有设备只需要运行 3.18 或更高版本的内核，而不必升级到支持 Project Treble。

* * *

[**来源:谷歌**](https://source.android.com/devices/architecture/kernel/modular-kernels#core-kernel-requirements)