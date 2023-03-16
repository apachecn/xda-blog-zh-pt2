# Android 11 DP3 测试让你调整画中画窗口的大小

> 原文：<https://www.xda-developers.com/android-11-dp3-tests-letting-you-resize-picture-in-picture-windows/>

# Android 11 DP3 测试让你调整画中画窗口的大小

谷歌正在测试让用户在 Android 11 DP3 中调整画中画窗口的大小。不过，该功能尚未上线。

今天早些时候，谷歌发布了用于 Pixel 设备的 Android 11 开发者预览版 3。我把最新的版本安装到我的 Pixel 3a XL 上，[已经记录了我目前为止所发现的东西(更详细的文章很快就会出现！)我们在这个版本中发现的一个更有趣的新特性是可以调整画中画窗口的大小。这项功能目前正在测试中，默认情况下不会启用。](https://twitter.com/MishaalRahman/status/1253368474501550082)

谷歌在 Android 8.0 Oreo 中为 Android 智能手机引入了画中画窗口。您可以在支持的应用程序的画中画窗口中打开视频，方法是在视频播放时按下主屏幕按钮或执行主屏幕手势。默认情况下，画中画窗口浮动在屏幕顶部的右下角，但用户可以通过将画中画窗口拖到屏幕底部来移动或关闭它。

在 Android 11 DP2 中， [Google 在 SystemUI 中的 PipResizeGestureHandler 类下添加了调整 PiP 窗口大小的代码](https://www.xda-developers.com/android-11-resize-picture-in-picture-pip-windows/)，但该功能尚未可用。不过，在 Android 11 DP3 中，手动发出开发命令后，调整画中画窗口大小的功能现在完全可用。通过触摸四个角之一的外侧，然后向外或向内拖动以分别扩展或缩小窗口，可以调整画中画窗口的大小。调整大小时，窗口的纵横比将保持不变，以免视频失真。下面是我运行 Android 11 DP3 的 Pixel 3a XL 上的新功能演示:

正如你在上面的屏幕记录中看到的，我将一个 YouTube 视频放入一个 PiP 窗口，然后通过向外拖动靠近角落来放大窗口。将手指放在需要启动调整大小手势的确切区域有点棘手，但我在视频中成功调整了窗口大小两次。我们不知道谷歌是否计划在稳定的 Android 11 版本中发布这项功能，但我们会关注它的进一步发展。