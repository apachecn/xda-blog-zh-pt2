# Chrome OS 将在环境模式下获得增强的锁屏功能

> 原文：<https://www.xda-developers.com/ambient-mode-enhanced-lockscreen-functionality-chrome-os/>

**更新 2 (4/20/2020 @美国东部时间下午 2:20):Chrome OS 的环境模式也会在锁屏上显示天气信息。**

**更新 1 (4/2/2020 @美国东部时间下午 4:20):**Chrome OS 的环境模式功能现在部分工作。

在过去的几个月里，我们了解到 Android 的几个功能正在向 Chrome OS 转移。回到去年 12 月，Chrome OS 79 [在锁屏](https://www.xda-developers.com/chrome-os-79-media-controls-lock-screen/)上引入了媒体控制，这是我们在 Android 上已经有很长一段时间了。然后，在一月初，Chrome OS 80 [向平台](https://www.xda-developers.com/chrome-os-80-introduces-android-10-gesture-navigation/)引入了类似 Android 10 的手势。随后，谷歌在 Chrome OS Canary 频道上发布了一个新的[快速回答功能](https://www.xda-developers.com/quick-answers-chrome-os-available-canary-channel/)，它的工作方式很像 Android 上的上下文快捷方式，并为高亮显示的文本提供信息/相关建议。现在，我们有理由相信 Chrome OS 可能很快就会获得 Android 的新环境模式。

谷歌[在去年的 IFA 贸易展上宣布了新的环境模式](https://www.xda-developers.com/google-assistant-ambient-mode-smartphone-tablet-smart-display/)。该模式基本上允许你将任何 Android 智能手机或平板电脑变成智能显示器。然后，您可以使用它来显示日历、当前天气、通知、提醒、音乐控制甚至智能家居控制中的信息。最初，这个功能[只对几个设备](https://www.xda-developers.com/google-assistant-ambient-mode-rolling-out/)可用。然而，就在这个月，一加宣布[也将从 OnePlus 3 开始在其所有手机上发布该功能](https://www.xda-developers.com/google-assistants-ambient-mode-rolling-out-oneplus-phones/)。现在，我们在 Chromium Gerrit 中发现了一个新的提交，它增加了一个新的特性标志。[标志描述](https://chromium-review.googlesource.com/c/chromium/src/+/2053037/1/chrome/browser/flag_descriptions.cc)声明“启用环境模式以显示具有更多功能的增强锁屏”，从而明确了 Chrome OS 中的这种环境模式将不仅仅用于显示图像。

关于这种新的环境模式的信息是去年 7 月 Chromium Gerrit 上的 ChromeStory 首次发现的。当时，唯一已知的信息是该功能可以让你在锁定屏幕上以幻灯片的形式查看壁纸。根据这一新发现，我们现在可以肯定这项功能与 Android 上的环境模式有关，可能允许用户在锁定屏幕上查看他们的日历、天气应用程序、通知、提醒等信息。一旦最近发现的提交被合并，该特性的标志将可在 chrome://flags # enable-ambient-mode 访问。

**来源:[铬革里特](https://chromium-review.googlesource.com/c/chromium/src/+/2053037)**

* * *

## 更新 1:部分工作

Chrome OS 的环境模式功能正在慢慢取得进展。在 Chrome OS 83 Canary 中，我们能够启用一个标志来查看新的环境模式设置。这些新设置出现在“个性化”下的系统设置中目前，环境模式有两个选项:谷歌照片和艺术画廊。这两种方法现在都行不通，但是你可以想象这将会是什么样子。

该标志将环境模式描述为“具有更多功能的增强锁定屏幕”正如我们在上面的原始文章中所写的，这将最终不仅仅是一个图像的屏幕保护程序。它可以将你的 Chromebook 变成一个智能显示器。这项功能还处于非常早期的开发阶段，所以在测试版和稳定版中看到它还需要一段时间。

* * *

## 更新 2:天气信息

Chrome OS 的环境模式仍在开发中，更多的功能已经被发现。谷歌正致力于将“简略信息”添加到环境视图中。一个新的提交特别提到了天气信息，这将非常有用。该委员会表示，天气信息将显示为“环境屏幕上简略信息的一部分”，这意味着将提供其他信息。

**Via: [Chrome 拆箱](https://chromeunboxed.com/chromebooks-chrome-os-lock-screen-ambient-display-widgets-weather-info/)**