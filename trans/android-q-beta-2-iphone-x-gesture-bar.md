# Android Q Beta 2 揭示了 iPhone X 风格手势栏的工作

> 原文：<https://www.xda-developers.com/android-q-beta-2-iphone-x-gesture-bar/>

# Android Q Beta 2 揭示了 iPhone X 风格手势栏的工作

最新的 Android Q 测试版适用于谷歌 Pixel 和 Project Treble 兼容设备。我们发现了一个支持新 iPhone X 风格手势栏的设置。

在今年 5 月的谷歌 I/O 之前，我们不会知道谷歌 Android Q 的新导航手势会采取什么形式。我们已经发现手势控制的工作方式即将发生两次而不是一次的变化。我们发现的第一个导航手势实验[取消了后退按钮](https://www.xda-developers.com/android-q-gestures-back-button/)，并增加了任务间更流畅的过渡动画。第二组变化是隐藏在 Android Q Beta 1 的 Pixel Launcher 中的[，最显著的变化发生在 home 和最近的应用程序动作上。谷歌今天早些时候发布了第二个 Android Q 测试版](https://www.xda-developers.com/android-q-iphone-navigation-gestures/)[，用于谷歌 Pixels 和任何 Project Treble 兼容智能手机](https://www.xda-developers.com/android-q-beta-2-notification-bubbles/)。如果你安装了测试版，你可能已经注意到最近新的应用程序转换动画类似于我们在二月份发现的。然而，你可能没有发现的是 Android Q 中手势工作方式的额外变化。

我在一台谷歌 Pixel 3 XL 上闪现了第二个 Q beta，发现了一个隐藏的设置，它去掉了后退按钮，用一个大型手势栏取代了 home 键药丸，让人想起了 iPhone X 上的 iOS 手势。下面是一个展示新手势栏的短片:

这显然是一个正在进行中的工作，因为过渡动画是错误的，在最近的应用程序中循环的快速 scrim 动画丢失了，而且没有办法回去，至少据我所知。谷歌不太可能完全取消后退按钮操作，因为这将导致我们与 Android 应用程序交互的方式发生巨大变化，但谷歌有可能在未来的某个时候添加后退按钮手势。也有可能这只是谷歌正在进行的许多手势控制实验之一，这些实验可能永远不会公开。这是我们看到的第三次手势变化，显然不可能所有的变化都出现在最终的 Android Q 版本中。

要启用这个新的手势栏，只需输入以下 ADB shell 命令:

```
 adb shell settings put global quickstepcontroller_showhandle 1 
```

如果我们在最新的 Android Q 版本中发现更多隐藏的变化，我们会让你知道。关注我们的 [Android Q 标签](https://xda-developers.com/tag/android-q)获取更多关于最新版本 Android 的新闻。