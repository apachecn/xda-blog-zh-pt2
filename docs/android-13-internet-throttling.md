# Android 13 将帮助开发者在网速较慢的情况下测试他们的应用

> 原文：<https://www.xda-developers.com/android-13-internet-throttling/>

Android 应用程序在各种屏幕尺寸、芯片组类型、移动网络等上都能很好地工作，这一点一直很重要。在慢速网络上进行测试尤为重要，因为不是每个人都有千兆互联网或无限制的 5G 数据连接，但在 Android 上人工节流互联网速度总是很困难。谢天谢地，Android 13 可能最终会改变这一点。

根据斯珀的一篇博客文章，谷歌正在为即将到来的 Android 13 更新开发一个新功能，该功能将允许任何网络连接被扼制。该功能实际上还没有工作，但来自 Android 开源项目(AOSP)的代码表明，你将能够以每秒字节数来设置网络速度。

唯一的问题是，这项功能需要内核级的支持，由于大多数设备在发布后不会收到内核的更新，因此许多现有的手机和平板电脑可能不支持网络节流。构建内核时还必须启用某些配置选项，比如 CONFIG_NET_SCHED。

已经有可能用一个节流的网络连接运行 Android Studio 模拟器，但是从来没有一种简单的方法来用一个真实的物理设备测试较慢的网络连接。一些开发者已经使用[微波炉(当它们不运行的时候)](https://stackoverflow.com/a/8630401)或者法拉第笼来减弱测试设备的无线信号。

谷歌还支持 Chrome 网络浏览器中的[节流网络连接，这可以方便地测试网站或网络应用在慢速网络下的表现。该设置在所有基于 Chromium 的 web 浏览器中都可用。苹果的 iOS 和 iPadOS 在开发者设置](https://css-tricks.com/throttling-the-network/)中允许[网络节流已经有一段时间了，但是要进入那个菜单需要在 Mac 上使用 Xcode development studio。](https://dev.to/vvo/enable-network-throttling-on-iphone-applications-in-5-steps-ikf)

Android 13 开发者预览版 2 还增加了应用程序通知的运行时权限，改进了日语文本换行，针对日语、COLR 字体、MIDI 2.0、蓝牙 LE 音频等语言的新文本转换 API，以及其他变化。查看我们的主要 [Android 13 开发者预览 2 报道](https://www.xda-developers.com/android-13-developer-preview-2/)了解更多信息和 Pixel 设备的下载链接。

**来源:** [斯珀](https://blog.esper.io/android-13-network-throttling-setting/)