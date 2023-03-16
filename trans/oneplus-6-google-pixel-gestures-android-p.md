# 获取 Android P 上 OnePlus 6 的谷歌 Pixel 手势

> 原文：<https://www.xda-developers.com/oneplus-6-google-pixel-gestures-android-p/>

# 获取 Android P 上 OnePlus 6 的谷歌 Pixel 手势

你知道你可以在运行 Android P 的 OnePlus 6 上启用谷歌像素导航手势吗？点击这里了解如何！

OnePlus 6 的 Android P Beta 3[刚刚发布](https://www.xda-developers.com/oneplus-6-android-p-developer-preview-4-beta-3/)，我们已经在这里深入报道了所有的新变化[。那些看到我们拍摄的一些截图的人可能已经注意到导航栏已经发生了变化，这是因为我们设法找到了如何在 OnePlus 6 上从谷歌像素](http://www.xda-developers.com/android-p-oneplus-6-beta-3)中启用[新导航手势。你所需要的是亚行，你也可以启用它们。甚至不需要 root 权限！如果你感兴趣，请继续阅读。](https://www.xda-developers.com/android-p-iphone-x-gestures-official/)

## 如何在 OnePlus 6 Android P Beta 3 上启用谷歌像素导航手势

### 步骤 1 -设置 adb 和 USB 调试

这部分很简单。你可以简单地按照我们的教程来设置 adb [这里](https://www.xda-developers.com/install-adb-windows-macos-linux/)。接下来，按照下面的截图，在 Android P 上的 OnePlus 6 上启用 USB 调试。

1.  导航到**设置>系统>关于手机**
2.  点击“ **Build number** ”直到它说你是开发者。
3.  返回上一屏，进入**开发者选项。**
4.  启用 **USB 调试。**

### 步骤 2 - adb 命令

现在，这是我们启用像素手势的地方。请确定您的手机已连接，并且您已授权访问您的电脑来调试它。然后在 adb 中运行以下命令。

```
 adb shell settings put secure swipe_up_to_switch_apps_enabled 1 
```

看看你的 OnePlus 6。新的导航栏应该是活动的！

* * *

真的是这样！这个设置只是重新启用手势，这是 AOSP 的一部分。一加似乎把它们留了下来，它们工作得或多或少很完美。你不能在启用它们的情况下使用不同的启动器，但这是我们目前唯一注意到的错误。如果你这样做，你会反复收到通知，告诉你一加启动器已经崩溃，你将无法切换应用程序。发生这种情况后，当我切换回一加启动器时，我的启动器看起来像下面的图片。

如果您发现任何其他问题，请告诉我们！如果你正在寻找一种不同风格的手势，请查看下面 XDA 自己的导航手势应用程序。

[app box Google play com . xda . nobar]