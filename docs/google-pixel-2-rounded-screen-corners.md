# 谷歌 Pixel 2 有一个隐藏的命令，可以让圆角应用程序变得更好

> 原文：<https://www.xda-developers.com/google-pixel-2-rounded-screen-corners/>

随着 LG G6 和三星 Galaxy S8 的流行，圆角屏幕已经成为一种越来越流行的趋势。一些用户喜欢这些圆形边缘的外观，T2 试图用 Cornerfly 等应用程序来模仿它。Cornerfly 使用纯黑色覆盖层创建圆角屏幕，给人以圆角的错觉。但这些应用在 Android Oreo 上并不那么好用，所以在常规的谷歌 Pixel 2 上，我们可能会遇到问题。幸运的是，我们已经发现了一个隐藏的命令，你可以与 Cornerfly 等圆角屏幕应用结合使用，以获得 Pixel 2 XL 外观[，而无需支付额外的 200 美元](https://www.xda-developers.com/google-pixel-2-xl-announced-price/)。

现在的情况是，Android Oreo [对应用程序可以在](https://www.xda-developers.com/android-o-is-breaking-apps-that-overlay-on-top-of-the-status-bar/)上绘制的内容进行了限制，比如导航栏、状态栏和其他系统用户界面元素。这意味着，如果你在角落里扩展圆的半径太远，状态栏时钟将会显示在它的上面。

这意味着在 Android Oreo 上，像 Cornerfly 这样的应用程序并不真正工作，然而，我们发现的命令将在 Google Pixel 2 上解决这个问题。原来，在 APK 在谷歌 Pixel 2 和 Pixel 2 XL 中发现的最新 SystemUI 中，谷歌添加了一个名为“RoundedCorners”的新类，该类为某些 SystemUI 元素添加了填充。

谷歌 Pixel 2 XL 上使用了这种方法，因为它实际上有一个圆形屏幕，所以 SystemUI 元素需要向内移动一点以适应这种情况。幸运的是，我们可以在普通的谷歌 Pixel 2 上利用这一点，让 Cornerfly 等应用程序再次正常工作。

我们在 XDA 公认的贡献者 [Quinny898](https://forum.xda-developers.com/member.php?u=3563640) 和 [Austin Greenlee](https://twitter.com/asoep456) 的帮助下对此进行了测试。

* * *

## 在谷歌 Pixel 2 上获得圆角屏幕

### 步骤 1 -设置

你只需要一个 adb 和一个谷歌 Pixel 2。[按照本教程为 Windows、MacOS 或 Linux 设置 ADB](https://www.xda-developers.com/install-adb-windows-macos-linux/)。一旦你设置好了，你就准备好了。

### 步骤 2 -命令

你可以简单地按照下面的命令！两者改变不同的方面。内容填充根据它的值将系统 UI 元素推向屏幕的中心，而圆角大小是这样的，所以系统知道角有多圆。

```
 adb shell settings put secure sysui_rounded_size x.x 
```

```
 adb shell settings put secure sysui_rounded_content_padding x 
```

Google Pixel 2 和 Google Pixel 2 XL 都将内容填充设置为默认值“8.0”。在 Google Pixel 2 XL 上舍入变量大小设置为“26.0”，在 Google Pixel 2 上设置为“0”。

**Pro-tip:** 在 Google Pixel 2 上把 sysui_rounded_content_padding 改成 0 会去掉状态栏图标填充。

你可以根据自己的喜好调整这两个变量，然后在谷歌 Pixel 2 上使用圆角屏幕应用程序来获得 Pixel 2 XL 效果。然而，谷歌 Pixel 2 XL 已经有了圆角，所以在那台设备上尝试这些命令没有什么实际好处。

### 步骤 3 -设置圆角屏幕角

现在，您可以简单地打开 Cornerfly 并使用它。看看文章顶部的截图，看看你能让你的设备变成什么样子。如您所见，这是有区别的，应用程序现在工作正常。试试看，看你怎么想！