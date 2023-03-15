# Android 11 Beta 3 的新功能:猫、表情符号和音乐

> 原文：<https://www.xda-developers.com/android-11-beta-3-features-changes/>

周四，谷歌发布了最后一个 Android 11 测试版，之前传言下个月会有稳定版。上个月的 [Android 11 Beta 2](https://www.xda-developers.com/android-11-platform-stability-beta-2-available-google-pixel-2-3-3a-4-xl/) 版本带来了最终的 SDK、NDK、面向应用的表面、平台行为以及对非 SDK 接口的限制，而 Android 11 Beta 3 只是包括了为稳定更新做准备的错误修复。不过，谷歌确实在 Beta 3 中对 Android 11 进行了一项改动:用户不再需要打开定位服务来使用使用[曝光通知系统](https://www.xda-developers.com/google-apple-new-privacy-functional-improvements-exposure-notification-covid-19-contact-tracing-api/) (ENS)的应用程序。不过，像往常一样，在 Pixel 设备上安装了更新之后，我们发现这个版本中有一些未经宣布的变化。Beta 3 没有早期 Beta 版那么多变化，但不管怎样，这是我们的发现。

## Android 11 Beta 3 -面向用户的新变化

### 安卓 11 复活节彩蛋来了

每个新的 Android 版本都有一个新的复活节彩蛋，Android 11 现在可以在 Beta 3 中使用。要访问它，请进入设置>系统>关于手机>安卓版本，并反复点击“安卓版本”字段。轻敲几下后，你会看到中间有一个绿色圆圈，里面有一个较小的白色圆圈，周围有几个较小的白色(或者黑色，如果你的系统主题是灯光主题)圆圈。这实际上是一个转盘，你需要顺时针转动 3 次，直到你看到 Android 11 标志出现，以及带有猫表情符号的祝酒词。(你"[把音量调到 11](https://en.wikipedia.org/wiki/Up_to_eleven) ，以防你没听懂。)

一旦你这样做了，你就可以进入一个新的迷你游戏，它包含 Android 11 的[智能家庭电源菜单功能](https://www.xda-developers.com/android-11-power-menu-device-controls-smart-home-dream/)设备控制。你可以通过打开电源菜单(长按电源按钮)开始，然后点击三点菜单“添加控制”在左下角，点击“查看其他应用程序”找到“猫控制”

没错，安卓牛轧糖的猫游戏又回来了。

如果你喜欢像这样愚蠢的小游戏(或者只是喜欢猫)，那么我相信你会从中得到乐趣。玩够了这个，你甚至会在 Android 11 的通知中的新对话部分遇到另一个与猫有关的复活节彩蛋。这是一个可以在气泡中打开的通知，就像来自消息应用程序的对话一样。

*演职员表:@anoop_v1 on 电报*

Android 11 将媒体播放通知与其他通知分开，将它们放在快速设置下的一个专用部分。如果应用程序支持，该功能还可以[存储多达 5 个之前的媒体会话](https://www.xda-developers.com/android-11-media-controls/)。

Android 11 Beta 2 自动将所有媒体播放通知放置在快速设置下的专用空间中，用户无法恢复到旧的行为。虽然 Android 11 Beta 3 仍然不允许你将媒体播放通知放在原来的位置，但它在设置>声音>媒体中引入了一个新的切换，称为“媒体会话结束时隐藏播放器”启用此切换将在活动媒体会话结束时隐藏媒体控制。这是为那些不想看到最近没有播放任何东西的应用程序的媒体控制的人准备的。

Android 11 Beta 3 的另一个小变化是能够隐藏未展开的快速设置面板中的媒体播放控件。以下截图显示了刷走媒体播放器前后的快速设置用户界面:

### 新表情符号在这里

Unicode Consortium [今年早些时候宣布了 Unicode 13](https://www.xda-developers.com/unicode-13-62-new-emoji-2020/) ，所有新的表情符号都进入了 Android 11。你可以闪存一个 Magisk 模块[将它们安装在任何根 Android 设备](https://www.xda-developers.com/android-11-new-emoji-install-root-magisk-module-unicode-13/)上，或者你可以使用类似 Gboard 的输入法来查看它们[，但在 Android 11 Beta 3 中你不需要这样做，因为表情样式已经被嵌入到系统字体文件中。以下是 SwiftKey 中新表情符号设计的截图:](https://www.xda-developers.com/gboard-android-11s-new-emojis/)

由于 Android 11 的新电源菜单打包了如此多的按钮，包括标准的电源菜单控件，通过[快速访问钱包 API](https://www.xda-developers.com/android-10-11-developer-preview-quick-access-wallet-google-pay/) 的非接触式支付方法，以及通过设备控制 API 的智能家居控制，谷歌不得不将关机和重启按钮合并为一个“电源”按钮。点击“电源”会显示标准的关机和重启选项，这是 Android 11 Beta 3 的新设计。

### 强制 90Hz 选项重新出现在 Pixel 4 上

Android 11 Beta 2 在 Pixel 4 上引入了低亮度水平下的[屏幕闪烁问题，这是因为该设备经常在具有不同伽马校准的 60Hz 和 90Hz 显示模式之间切换。一些用户试图通过手动强制手机始终保持在 90Hz 显示模式来解决这个问题，但谷歌取消了 Android 11 Beta 2 开发者选项中的强制 90Hz 切换，从而破坏了他们的计划。令人欣慰的是，类似的切换现在已经在 Android 11 Beta 3 的开发者选项中回归，正如 Redditor /u/](https://www.xda-developers.com/android-11-beta-2-5-fixes-pixel-4-screen-flickering-and-more/) [amenotef](https://www.reddit.com/r/android_beta/comments/i4wh1b/fyi_beta_3_has_two_different_smooth_display/) 所发现的那样。

* * *

这就是 Android 11 Beta 3 中半值得注意的变化。谷歌现在专注于修复错误和提高 Android 11 的稳定性，以迎接传言中的 9 月 8 日(T1)的稳定发布。当然，我们将继续挖掘最新的 Android 11 版本，看看我们是否能找到更多关于未宣布和正在开发的功能的细节。