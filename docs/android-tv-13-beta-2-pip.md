# Android TV 的 Android 13 带来了“扩展”的画中画模式

> 原文：<https://www.xda-developers.com/android-tv-13-beta-2-pip/>

# Android TV 的“扩展”画中画模式在 Android 13 Beta 2 中实现

Android 13 引入了新的扩展画中画模式，允许开发者在 Android TV 上创建更长更宽的 PiP 窗口。

在新的 Android 13 测试版的兴奋中，很容易忘记手机(和平板电脑)不是唯一需要升级的东西。虽然最初的 Android 13 测试版对 Android TV 来说有点平淡无奇，但最新版本包含了用户很久以来一直想要的东西——改进的画中画模式。

尽管 Android TV 多年来一直支持画中画模式，但 Android 13 将是第一个允许开发者创建扩展 PiP 窗口的版本。在引擎盖下，画中画 API [已经更新](https://developer.android.com/reference/android/content/pm/PackageManager#FEATURE_EXPANDED_PICTURE_IN_PICTURE)以适应屏幕上的多窗口实例。因此，最终用户可以无缝地改变画中画窗口的大小。这对于使用电视进行视频通话或监控安全摄像头的人来说特别有用，因为它们可以容纳更多的参与者或流。还将有一个新的停靠模式，可以调整主应用程序的大小，以允许 PiP 窗口位于边缘。

值得注意的是，扩展画中画模式和对接功能的到来早在三月的[就已经暗示过了。虽然 Google 没有在 Beta 1 版本中发布它们，但是它们最终在 Beta 2 版本中发布了。Android 13 还增加了应用程序标记不应被画中画窗口覆盖的 UI 元素的功能。被称为“](https://www.xda-developers.com/android-13-tv-expanded-picture-in-picture-mode/)[保持清晰](https://developer.android.com/reference/https://developer.android.com/reference/android/view/View#attr_android:preferKeepClear/view/View?hl=en#attr_android:preferKeepClear)”的 API 确保画中画片段永远不会覆盖屏幕的重要部分。

与手机版本不同，Android TV 测试版在实际测试方面仍然相当有限。例如，第二个测试版只有[作为模拟器镜像](https://developer.android.com/tv/release/13/preview)可用。甚至谷歌自己的 ADT-3 开发者硬件平台也尚未以可闪存包或无线更新的形式接收 Android TV 13 Beta 2。目前还不清楚谷歌电视或其他现有 Android 电视设备的 Chromecast 何时会推出稳定更新。

* * *

**来源:** [谷歌](https://io.google/2022/program/1e5d0560-24f2-4891-8991-0d93af8d9965/)