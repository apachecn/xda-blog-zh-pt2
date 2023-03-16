# 用音量键跳过 Android 8.0+上的歌曲——不需要 Root！

> 原文：<https://www.xda-developers.com/skip-music-tracks-android-volume-keys-no-root/>

如果你以前安装过定制 ROM，那么你很有可能见过一个功能，让你重新映射长按音量按钮来控制媒体播放。启用此选项后，您可以长按音量增大按钮跳到下一首曲目，或长按音量减小按钮返回上一首曲目。用音量按钮跳过歌曲的功能在定制 rom 中是如此普遍，以至于我们惊讶地看到它还没有进入主要原始设备制造商的软件中。

我们已经介绍了使用像 [Tasker](https://www.xda-developers.com/tasker-pro-skip-music-tracks-using-volume-keys/) 或[按钮映射器](https://www.xda-developers.com/xda-spotlight-button-mapper-an-app-to-remap-your-phones-hardware-buttons/)这样的应用程序通过音量按钮来控制音乐播放的方法，但这些应用程序都没有完全复制定制 rom 能够提供的功能。如果您使用 Tasker 或按钮映射器，您只能重新映射单次或多次按下的音量增大和减小按钮。像这样的应用程序要么监听媒体音量的变化，要么使用辅助服务来拦截音量键的按钮按压，但这两种解决方案都无法在屏幕关闭时拦截音量键的长时间按压。

在 Android 8.0 Oreo 的源代码发布后不久，我发现了一个新的 Android 功能，它允许一个 Android 应用程序被设置为“[音量键长按监听器](https://www.xda-developers.com/android-oreo-volume-key-long-press/)”我们推测，这个新的 API 将允许应用程序在屏幕关闭时控制长按音量按钮的行为，从而最终使复制流行的自定义 ROM 功能成为可能，而不需要 root。虽然该功能是在 AOSP 实现的，但谷歌从未添加面向用户的方式来将应用程序设置为音量键长按监听器。就像 Android 的[隐藏导航条定制器](https://www.xda-developers.com/nav-bar-customization-was-hidden-in-stock-nougat-all-along-and-it-never-needed-root/)一样，即使没有在设置应用中实现，这个功能仍然可以使用。

这正是 XDA 成员 [Cilenco](https://forum.xda-developers.com/member.php?u=5041228) 用[通过音量键跳过音轨应用](https://forum.xda-developers.com/android/apps-games/app-skip-track-volume-keys-t3914337/)所做的。这是一个开源应用程序，它使用隐藏的音量键长按 listener API，让你即使在屏幕关闭的情况下，也可以长按任何一个音量按钮来改变音乐曲目。它可以在任何 Android 8.0 奥利奥、Android 8.1 奥利奥、Android 9 Pie 或 Android Q 设备上运行。这款应用是在我们发表文章后几个月开发的(开发者甚至[引用了](https://forum.xda-developers.com/showpost.php?p=79298240&postcount=13)这篇文章作为他们开发这款应用的灵感)，但它从未在我们的论坛上分享过，直到上个月末它才最终引起我们的注意。我们很快就把它试了一圈，看看它是否有效——它确实有效！这里有一段来自 XDA 电视台的 Max Weinbach 的实践视频:

要设置它，你所要做的就是从 GitHub 安装 [APK 并运行以下 ADB 命令:](https://github.com/Cilenco/skipTrackLongPressVolume/releases)

```
 adb shell pm grant com.cilenco.skiptrack android.permission.SET_VOLUME_KEY_LONG_PRESS_LISTENER 
```

然后，启用应用程序的通知监听器服务。这个通知侦听器服务实际上不做任何事情，它只是确保应用程序不会在后台被杀死。在我的华为 Mate 20 X 上，我不得不禁用 EMUI 9 的[积极的内存优化功能](https://www.xda-developers.com/phone-software-killing-apps-background/)，但之后我可以确认它在 EMUI 上确实工作。由于这是一个隐藏的 API，不能保证谷歌在未来的 Android 版本中不会取消对它的访问。[自 Android Pie](https://www.xda-developers.com/google-undocumented-hidden-apis-android-p/) 以来，谷歌一直致力于限制未记录/隐藏的 API，因此这可能在 Android Q 或 Android R 的最终版本中不起作用

* * *

或者，如果你不愿意安装 GitHub 的 APK，你可以试试 XDA 知名开发者 [flar2](https://forum.xda-developers.com/member.php?u=4684315) 最新发布的 Next Track(版本 1.18)。在我告诉他这个 API 后，他很快就更新了这个应用程序，所以如果你想要一些更加可定制的东西，就去看看吧。如何设置的说明可以在[这里](https://nexttrack.app/)找到。开发者正在更新他的[按钮映射应用](https://www.xda-developers.com/xda-spotlight-button-mapper-an-app-to-remap-your-phones-hardware-buttons/)，以便使用新的 API。按钮映射器的现有方法是在屏幕关闭时重新映射长时间按下音量按钮，这种方法有点粗糙，并且会在每次重启时重置，但新的 API 会在启动后持续存在。