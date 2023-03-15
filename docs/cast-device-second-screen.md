# 在全高清电视上播放

> 原文：<https://www.xda-developers.com/cast-device-second-screen/>

# 使用第二个屏幕，让您的设备屏幕呈现出应有的样子

第二个屏幕允许您以电视的原生分辨率将设备屏幕投射到电视上，而不是 Android 想要使用的任何分辨率。

不久前，在 XDA 门户网站上，我们报道了谷歌如何实现他们的承诺，允许[谷歌 Chromecast](http://forum.xda-developers.com/hardware-hacking/chromecast) 用户最终[通过这个小而便宜的发电站将他们的设备屏幕](http://www.xda-developers.com/android/chromecast-android-screen-mirroring/)投射并镜像到大屏幕上。然而，由于该功能在设备上的限制，[我们的成员挺身而出，决定“修复”](http://www.xda-developers.com/android/enable-chromecast-mirroring-from-any-device/)谷歌的错误，并赠送给几乎所有设备镜像主屏幕，只有少数例外。但这篇文章不是关于 Chromecast 甚至谷歌的。相反，我们关注的是 XDA 资深成员 farmerbb 带来的成果，这应该会让你们中的很多人非常高兴，因为你们决定冒险使用全高清电视。

开发人员展示了他的应用程序，被称为第二屏幕。不管它的名字可能暗示什么，这不是一个将你的主屏幕扩展到电视的工具，而是一个将你当前的屏幕恰当地投射到大屏幕上的工具。主要的问题是，无论何时播放屏幕，Android 都试图使用它认为合适的任何分辨率。它不关注你的屏幕实际上有什么分辨率，本质上是将你的设备屏幕的原始版本镜像到它被投射到的电视上。无论你是使用 DNLA、MHL 还是其他电视设备，比如 Miracast，甚至是 Chromecast，都会发生这种情况。Second Screen 旨在为您提供一种正确投射屏幕的方法，以便您在向朋友和家人展示时，屏幕看起来是最佳的。它允许用户选择分辨率，甚至 DPI，以便充分利用您的电视。除此之外，该应用程序还有几个附加功能，例如关闭屏幕和触觉反馈，以便在你施法时节省电池的使用。此外，它还提供了使用 WiFi 或蓝牙输入设备的简单连接选项，以便将您的设备变成家庭娱乐系统。至于顶部的樱桃，你可以在桌面模式下使用 Chrome，而不必手动进入并自己更换客户端。

这款应用需要 root 才能运行，不幸的是，它只能在 AOSP 的 rom 上运行。你可以在其他设备上随意尝试，但是开发者不能保证它能在其他软件上运行。这方面的反馈非常重要，所以如果你有一台运行任何 AOSP 版本的设备，并且有 Chromecast、Miracast 或任何安装了接收 cast 的电视，请尝试一下并报告你可能有的任何反馈。现在，去把你的心扔出去吧！你可以在[秒屏 app 线程](http://forum.xda-developers.com/showthread.php?t=2766268)中找到更多信息。