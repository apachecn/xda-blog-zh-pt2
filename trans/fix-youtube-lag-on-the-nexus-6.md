# 这里有一个快速修复 Nexus 6 最近的 YouTube 应用程序延迟问题的方法

> 原文：<https://www.xda-developers.com/fix-youtube-lag-on-the-nexus-6/>

# 这里有一个快速修复 Nexus 6 最近的 YouTube 应用程序延迟问题的方法

如果你在 Nexus 6 上观看视频和滚动浏览 YouTube 应用程序上的评论时遇到延迟，这里有一个快速简单的解决方法。

众所周知，Android 是一个通用的移动操作系统。即使你从一部 Nexus 手机跳到另一部，你的软件体验也会有细微的不同。理论上，你应该不会注意到 Nexus 6 和 Nexus 6P 之间的许多软件差异。

但在 Nexus 6 上，当你同时观看视频和浏览评论时， [YouTube 应用程序莫名其妙地滞后了](http://forum.xda-developers.com/nexus-6/help/youtube-lag-t3272824)。许多 Nexus 6 用户报告说，这个问题是在跳转到 Android 6.0 棉花糖之后才开始的。这是怎么回事，你怎么解决？

修理它很简单。你只需要打开开发者选项*下的 ***禁用硬件覆盖*** 选项。以下是更改选项对 YouTube 性能影响的前后对比。

为什么这种修复有效？我们并不完全确定我们自己。甚至连 Android 工程团队都还没有弄清 YouTube jank 的真相:

#### ***在运行 Android M 的 Nexus 6 上播放 Youtube 视频时，我们确实注意到一些首次加载的滚动评论时的 jank。在强制 GPU 合成时，jank 似乎有所改善。Android 6.0 上的 Youtube 使用 SurfaceViews 进行视频播放，因为它比使用 TextureViews 耗电更少。强制 GPU 合成以功耗为代价提高了评论滚动的流畅度。敬请关注。***

如果你注意到在 AMA 会议期间发表的评论，这个团队确实提到，强制 GPU 合成可以提高 YouTube 应用程序的性能。禁用硬件覆盖基本上就完成了这个任务:通过启用此选项 [SurfaceFlinger](https://source.android.com/devices/graphics/) 将放弃使用硬件覆盖，而是始终使用 GPU 进行合成。不幸的是，禁用硬件覆盖确实会导致功耗增加，并且实际上只应该用于调试某些类型的媒体应用程序。**解决这个问题的一种方法是将 [Tasker](https://play.google.com/store/apps/details?id=net.dinglisch.android.taskerm&hl=en) 等应用程序与[安全设置](https://play.google.com/store/apps/details?id=com.intangibleobject.securesettings.plugin&hl=en)插件配合使用，以便在您使用 YouTube 应用程序时自动切换“禁用硬件覆盖”选项。**

* * *

* *如何获得开发者选项？转到设置，然后转到关于设备，然后向下滚动到内部版本号，并点击内部版本号字段 7 次。你在 XDA，你应该知道这一点！*