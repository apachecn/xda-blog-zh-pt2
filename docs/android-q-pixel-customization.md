# Android Q beta 通过样式、时钟等暗示了像素定制

> 原文：<https://www.xda-developers.com/android-q-pixel-customization/>

**更新(美国东部时间 8/16/19 @上午 10:25):**像素定制建议现在出现在最新的 Android Q beta 上，面向部分像素所有者。

谷歌在三月份发布了第一个 Android Q 测试版，随后在四月初发布了第二个测试版。当第二个测试版发布时，我们发现了一个名为“[像素主题](https://www.xda-developers.com/android-q-pixel-themes-google-pixel/)的新谷歌应用的 APK 存根除了展示一些代号为“安东尼”、“约翰娜”和“小早川怜子”的主题预览，存根基本上是空的 Android Q 已经通过开发者选项中有限的强调颜色、图标形状和字体选择提供了基本定制，但是“像素主题”的存在表明谷歌准备在未来的版本中提供更好的像素定制。在尚未发布的 Android Q 测试版中，我们发现了更多的迹象，表明谷歌将增加有限的像素主题支持。

我们分析了来自未发布的 Android Q beta 版本的设置 Google 和 SystemUIGoogle APKs，发现两个新字符串负责建议用户定制他们的 Pixel。当您打开“设置”时，您可能会在“网络与互联网”菜单上方找到一些建议。例如，如果你没有启用指纹解锁，那么你可能会看到一个“使用像素印记”的建议。在未来的 Android Q 版本中，您可能会看到“自定义您的像素”建议:

```
 <string name="style_suggestion_summary">Try different styles, wallpapers, clocks, and more</string>
<string name="style_suggestion_title">Customize your Pixel</string> 
```

该建议建议用户“尝试不同的风格、壁纸、时钟等等。”样式很可能是指强调色定制，而时钟很可能是指我们之前发现的的锁屏时钟定制[。](https://www.xda-developers.com/android-q-lock-screen-clock-customization/)

一旦该功能上线，[我相信](https://twitter.com/MishaalRahman/status/1139203083223949312)当你长按 Pixel Launcher 主屏幕上的任何空白区域时，显示的“壁纸”选项将会更新为“样式&壁纸”点击这个将启动壁纸应用程序，我相信它将在稍后更新，以包括新的“像素主题”功能。

根据在 SystemUI 的 ThemeOverlayManager 类中找到的代码，看起来您将能够更改 Android 框架的强调颜色、图标形状和字体，或者更改 SystemUI 的图标包、设置和默认启动器。在功能发布之前，我们可能会看到更多的像素定制功能。我敢打赌，在 10 月份谷歌 Pixel 4 系列发布之前，我们不会看到这个功能。

*T* *感谢 PNF 软件公司为我们提供使用许可[杰布反编译器](https://www.pnfsoftware.com/?aid=xdadev)，这是一款用于 Android 应用的专业级逆向工程工具。*

*这篇文章在美国东部时间 2019 年 7 月 10 日下午 4:48 更新，以反映我们检查了一个泄露的 Android Q beta 版本，该版本与 Android Q beta 5 不同。*

* * *

## 更新:出现在一些

正如在最初的文章中提到的，我们在“定制你的像素”的设置中找到了建议字符串。一些 Pixel 用户现在在最新的 Android Q beta 中看到了这一点，上面有我们之前发现的确切文本:“尝试不同的风格、壁纸、时钟等等。”现在，点击建议会将用户带到壁纸应用，但很明显谷歌正在准备更多的定制选项。

**来源:[安卓警察](https://www.androidpolice.com/2019/08/16/android-q-custom-styles-clocks/)**