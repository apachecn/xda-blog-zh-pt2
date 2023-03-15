# Android 11 Beta 2 -我们发现的所有新功能和开发中的功能

> 原文：<https://www.xda-developers.com/android-11-beta-2-new-features/>

谷歌今天早些时候发布了 Android 11 Beta 2，在 9 月 8 日发布稳定版之前，只剩下一个测试版[。Beta 2 被认为是“平台稳定性”版本，这意味着 Android 11 SDK、NDK API、面向应用的表面、平台行为以及对非 SDK 接口的限制已经最终确定。在他们的官方博客帖子中，谷歌没有提到任何新功能，但这并不意味着没有任何新功能。我们发现的许多变化并不明显，其中一些甚至从上个月](https://www.xda-developers.com/stable-android-11-update-september-8th/)[第一个测试版发布以来就已经存在了。这是我们目前找到的所有东西。](https://www.xda-developers.com/android-11-beta-1-update-live-google-pixel-2-3-3a-4-xl-device-controls-api-quick-settings-media-controls/)

## Android 11 Beta 2 中面向用户的新功能和变化

**快速设置设计中的新媒体播放器现在默认启用**

Android 11 中最受欢迎的变化之一是通知面板中重新设计的媒体播放器。媒体播放器通知现在可以显示在快速设置面板下的专用空间，而不是与其他通知放在一起。在 Android 11 Beta 1 中，你必须切换一个名为“媒体恢复”的开发者选项才能获得这一新设计。现在在 Beta 2 中，这个新的媒体播放器位置是默认启用的。新的播放控制还包括一个按钮，可以在连接的设备之间快速切换媒体输出。

Android 11 的新媒体播放控制的另一个优势是能够记忆和循环播放之前的 5 个媒体会话。这需要开发人员做一些工作来支持，但我们有望很快看到 YouTube Music、Pandora 和 Spotify 等应用程序加入进来。

**媒体播放器控件中新的发光“波纹”动画**

诚然，这是一个相当小的变化，但当我们第一次注意到它时，我们认为这是一个整洁的变化。当与媒体播放通知中的按钮交互时，有一个漂亮的新发光/波纹动画。这是一个小触摸，但它看起来真的很好。

**屏保可以同时录制设备/内部音频和/或麦克风**

Android 10 增加了 AudioPlaybackCapture API，为应用程序提供了一种从其他应用程序捕获音频输出的官方方式。在 Android 10 添加这个 API 之前，大多数屏幕录制应用程序都是从麦克风捕捉音频输出。除了第三方屏幕录制应用，人们多年来一直呼吁谷歌在 Android 中添加一个原生屏幕录制器。这终于在早期的 Android 11 版本中实现了，但你只能从麦克风录制音频。最后，Beta 2 增加了录制设备音频、麦克风或同时录制两者的功能！这将证明对制作指导性的屏幕录像或游戏解说非常有帮助。我们深入研究了代码，发现这项功能使用了前面提到的 AudioPlaybackCaptureAPI，这意味着它[将无法从选择退出](https://www.xda-developers.com/android-q-record-audio-monitor-device-temperature/)的应用程序中录制音频。

**减少共享表中的混乱**

Android 的分享表是其最有用的功能之一，尽管有时会有点烦人。共享表由一系列应用程序填充，这些应用程序具有所谓的共享目标，可以处理您正在共享的内容，无论是文本、图像、视频、URL 等。在共享表的顶部，您会看到您共享的内容的预览。在它下面，你会发现一排[共享快捷方式](https://www.xda-developers.com/remove-direct-share-share-menu-root/)，让你可以快速与特定联系人共享内容，后面是另一排应用程序可以显示的任何其他快捷方式以及你锁定的任何快捷方式。最后，支持你正在分享的内容的任何剩余应用程序将显示在垂直滚动的“应用程序列表”中

除了有时慢得令人痛苦之外，Share Sheet 的最大问题之一是，如果你安装了一堆应用程序，它会变得非常混乱。幸运的是，Android 11 Beta 2 通过合并来自同一应用程序的任何共享目标，稍微整理了一下共享菜单。在上面的截图中，有 3 个来自 MiXplorer 的分享目标，MiXplorer 是一个来自我们论坛的免费且受欢迎的文件管理应用。虽然这 3 个共享目标仍然显示在共享快捷方式部分，但它们都列在完整的“应用列表”中的“MiXplorer”下我运行 Beta 2 的 Pixel 3a XL 没有安装很多应用程序，但如果安装了，这个小变化真的会有助于清理共享表。

**...已锁定的应用程序现在有一个图标表示它们已被锁定**

下面是对 share sheet 的另一个简单而有意义的小变化:钉在 share sheet 顶部的应用程序现在会显示一个真正的大头针图标。

**长按电源菜单中的设备控制按钮，进入活动**

[Android 11 最好的功能之一](https://www.xda-developers.com/android-11-power-menu-device-controls-smart-home-dream/)是能够在电源菜单中显示智能家居控制。这项被称为“设备控制”的功能附带了一个 API，智能家居应用程序的开发者可以连接到该 API。到目前为止，[谷歌家居应用](https://www.xda-developers.com/google-home-android-11-device-controls/)已经增加了支持，本周谷歌[开始通知智能家居开发商](https://www.xda-developers.com/google-smart-home-summit-new-developer-features/)加入进来。如果你不知道，你实际上可以长按任何智能家居控制来打开特定物联网产品的详细控制活动，而不必打开专用的应用程序。这实际上是设备控制的关键功能之一，但它并不为人所知，我们听到了关于它是否可能在 Android 11 Beta 1 中实现的相互矛盾的报告。尽管如此，如果你以前没有意识到，希望你现在意识到了。

如果你没有谷歌 Pixel 手机，不要对这个功能抱太大希望。毕竟，不能保证它会出现在所有运行 Android 11 的设备上。

**在泡泡中启动对话的新图标**

“泡泡”是 Android 11 的突出特色之一，尽管它最初是 Android 10 的开发者选项。在第一个测试版中，气泡功能从开发者选项中移出，进入设置>应用&通知>通知。“允许应用程序显示气泡”选项现在默认启用，但应用程序仍然需要支持将对话显示为气泡。到目前为止，只有[谷歌的消息应用](https://www.xda-developers.com/googles-messages-beta-now-shows-bubble-notifications-on-android-11/)和 [Facebook Messenger](https://www.xda-developers.com/facebook-messenger-chat-heads-switch-android-11-bubble-notifications-api/) 支持在气泡中显示聊天内容。

然而，开发人员增加对气泡通知的支持只是拼图的一部分。用户需要了解这个功能，这就是为什么在最近的测试版中，当你第一次在泡泡中发起聊天时，谷歌添加了一些有用的入职信息。现在在 Beta 2 中，通知中有一个重新设计的图标，以气泡的形式弹出对话。这个通知让用户更清楚地知道，点击它会将消息弹出通知窗口。

**画中画窗口的尺寸较小**

在调整大小时，画中画窗口似乎缺乏灵活性，这是 Android 11 开发者预览版 4 刚刚添加的功能。上面的截图显示了你可以调整窗口大小的程度。很遗憾，这并不多。早期的版本允许你在保持长宽比的情况下调整窗口大小，但是现在窗口大小似乎有了一个上限，可能与设备的 DPI 有关。

**最近应用概览中的新选择按钮图标**

这里有另一个小小的变化:最近应用概览中的“选择”按钮被重新设计了一个新图标。就是这样。

**游戏控制器的 3 个新键盘布局文件**

我们写了 Android 11 [如何为 Xbox、Razer、PDP、Mad Catz 和其他游戏控制器带来 84 个新的按键映射](https://www.xda-developers.com/android-11-84-new-gaming-controller-mappings/)。嗯，Beta 2 又增加了 3 个:另一个 Xbox 360 无线控制器，一个 Xbox USB 控制器，和 Steam 控制器(型号 1001)。这些控制器现在将把它们的按钮正确映射到应用程序在连接到 Android 设备时可以识别的按键输入。

**Pixel Launcher 应用程序抽屉失去了透明度**

不可否认，这种变化可能在早期版本中发生过，但是我们没有注意到它，直到一个消息灵通人士把它带到我们的注意中。当你打开 Pixel Launcher 中的应用程序抽屉时，背景中不再有任何透明度。我们不知道为什么会改变，但我们知道谷歌正在幕后工作，在合成器级别实现 windows 模糊。

**取消强制 90Hz 刷新率选项，平滑显示现在少了一页**

正如一些 Reddit 用户首先向我们指出的那样，在 Android 11 Beta 2 中，Pixel 4 和 Pixel 4 XL 的开发者设置中的“强制 90Hz”刷新率选项已经被删除。此外,“平滑显示”切换在显示设置中被赋予了[更突出的位置](https://www.reddit.com/r/android_beta/comments/hnkwcq/android_11_beta_2_now_available/fxc38ck/)。你可以在上面的推文中看到这两种变化。

Force 90Hz 选项的删除导致了一些用户的投诉，他们现在报告了屏幕闪烁问题。这些问题可能源于刷新率变化时[显示器在不同伽马校准](https://www.xda-developers.com/google-pixel-4-why-90hz-limited-brightness/)之间的切换。这在大多数情况下并不明显，但有些用户可能会在显示器和环境亮度较低时看到这种情况。请记住，Pixel 4 和大多数具有高刷新率显示屏的智能手机一样，不支持真正的可变刷新率切换。相反，手机会在预设的显示模式之间切换。

我们不知道为什么谷歌决定删除这个漂亮的选项。幸运的是，如果你摆弄 ADB 或任何具有 WRITE_SETTINGS 权限的应用程序，你可以很容易地强制手机再次总是以 90Hz 运行(设置设置。最小刷新速率和设置。System.peak_refresh_rate 设置为“90”)。

**对话有专门的设置页面**

在“设置”>“应用与通知”中，有一个专用于对话的设置片段，它独立于其他通知子设置。在这里，您可以更改被识别为“对话”的任何应用程序通知的设置你可以更改优先级，应用程序是否可以显示为气泡，等等。

**对标记截图编辑器进行了细微调整**

Pixel 手机带有一个叫做标记的基本截屏编辑功能。在 Android 11 中，最上面一排图标被改变了。“共享”按钮已被一个共享图标取代，“保存”按钮已被移动到一个新的对话框中，当你点击“完成”时就会出现(以前只是一个返回箭头来退出标记)，现在有一个垃圾桶图标来删除图像。当你点击“完成”时，现在还有一个删除选项，以防你改变主意。

**新的“允许在设置上覆盖屏幕”开发者选项**

开发者选项中有一个新的选项叫做“允许在设置上覆盖屏幕”启用此项将允许具有“显示在其他应用上”权限的应用在设置屏幕顶部显示其浮动窗口。考虑到谷歌计划用 Bubbles API 取代覆盖，我们并不完全确定为什么会增加这个切换。谷歌可能想让屏幕阅读器和其他辅助服务使用覆盖图来帮助用户导航设置。

**当应用程序全屏显示时，气泡整齐地隐藏起来**

据 tipster @AnalogCyan 报道，Android 11 中的浮动气泡图标现在会在你启动应用程序时全屏隐藏。

【Beta 1:禁用特定网络的 Wi-Fi 自动连接

Android 已经支持自动打开 Wi-Fi 并连接到附近的(受信任的)网络，但这对于 Pixel 手机来说一直是一个要么全有要么全无的事情。您要么在“设置”>“网络与互联网”>“Wi-Fi”>“Wi-Fi 偏好设置”中启用了“自动打开 Wi-Fi”设置，要么没有启用。在第一个 Android 11 测试版中，谷歌增加了基于每个 Wi-Fi 网络切换该功能的选项。只需进入“网络”详细信息，查看任何保存的 Wi-Fi 网络，然后切换“自动连接”

**来自 Beta 1:保存最近应用概览中的图片**

Pixel 手机上的设备个性化服务应用程序为最近的应用程序概述添加了一个漂亮的功能:长按文本或图像以打开上下文菜单的能力。在早期的 Android 11 测试版中，谷歌增加了在最近应用概览中长按“保存”图像的功能。

## Android 11 Beta 2 中正在开发的功能

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些特性目前还没有在实时构建中实现，并且可能会被开发人员在未来的构建中随时引入。

**新的 Pixel Launcher 开发者选项，将最近的活动从 Launcher 中分离出来**

在 Pixel Launcher 的隐藏开发者设置中，我们发现了一个新选项，肯定会让那里的修改者兴奋不已。在 Android 9 Pie 中，谷歌将最近应用概述的代码从 SystemUI 移到了 Launcher3，这是 AOSP 启动器应用。从 Android 9 Pie 到 Android 11，最近的应用程序概述已经成为股票启动器的一部分，无论这是谷歌 Pixel 设备上的 Pixel 启动器还是非谷歌设备的 OEM 启动器应用程序。这一变化的好处是手势导航与最近的应用概述无缝集成。然而，这一举措让第三方启动器开发者望尘莫及，因为如果用户不使用股票启动器，手势导航要么被破坏，要么不可靠。Pixel Launcher 中的这个新选项可能暗示了最近的应用程序概览和 launcher UI 之间可能的分离，但我们不知道它将如何实现。不过，我们会留意更多的线索。

**缓存应用暂停执行**

谷歌正在开发一个新的开发者选项，恰当地命名为“缓存应用冷冻器”根据我们挖掘出的一些字符串，这个特性将“暂停缓存应用的执行”用户可以在每个应用程序的基础上切换该功能。

```
 <string name="cached_apps_freezer">Suspend execution for cached apps</string>
<string name="cached_apps_freezer_device_default">Device default</string>
<string name="cached_apps_freezer_disabled">Disabled</string>
<string name="cached_apps_freezer_enabled">Enabled</string>
<string name="cached_apps_freezer_reboot_dialog_text">Your device must be rebooted for this change to apply. Reboot now or cancel.</string> 
```

我们还不能展示这个功能，但是一旦我们让它工作了，我们会更新一些截图。

**设备掉落监视器**

毫不奇怪，谷歌正在开发新的 Pixel 手机，尽管谁知道它们什么时候会问世。至少看起来，谷歌仍在积极收集用户数据，以改进他们未来的设备。Pixel 4 和 Pixel 4 XL 上的 Android 11 Beta 2 有一个新的预装应用程序，名为“设备跌落监视器”。不过，你不会在应用抽屉里找到它。这款应用程序可以检测设备何时快速跌落到地面。它记录自由落体的持续时间和设备的加速度。当检测到跌倒时，应用程序会显示一个通知，要求用户完成一个简短的调查。该调查要求用户估计设备掉落的距离，手机落在什么材料上(混凝土/沥青/硬木/地毯/瓷砖/等等)。)，以及手机是否在保护壳中。完成调查后，该应用程序将告诉用户，“他们的输入将有助于改进未来 Pixel 设备的设计。”我们不知道这个应用程序是否会向普通用户显示调查，因为启动调查的代码似乎被硬编码为返回 false。

**高亮度模式管理器**

针对用户抱怨 Pixel 4 的[显示屏太暗，无法看到室外](https://www.xda-developers.com/google-pixel-4-high-brightness-mode-fix/)，谷歌[更新了自适应亮度算法](https://www.xda-developers.com/pixel-feature-drop-second-features-list/)，以便在检测到极其明亮的环境照明时启用高亮度模式。不过，谷歌似乎正在将这段代码推向 AOSP，因为我们发现了一个名为 HbmSvManager 的新系统应用程序，其包名为 com.android.hbmsvmanager，其中包含了该算法的逻辑。

* * *

和往常一样，如果我们对 Android 11 了解更多，我们会发布一篇关于 XDA 的文章。您可以关注我们的 Android 11 标签，了解我们发现的所有内容:

**[安卓 11 XDA 新闻](https://xda-developers.com/tag/android-11)**