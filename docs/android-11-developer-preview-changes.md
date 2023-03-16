# Android 11 开发者预览版:目前为止我们从 Android 10 发现的所有变化！

> 原文：<https://www.xda-developers.com/android-11-developer-preview-changes/>

谷歌发布了 Android 11 的[首个开发者预览版，正式开启了下一个版本的 Android。第一个预览版是](https://www.xda-developers.com/android-11-developer-preview-1-google-pixel/)[为开发者准备的](https://www.xda-developers.com/android-11-developer-preview-new-development-features/)，但是也有几个面向消费者的特性需要注意。我们将在一周内不断更新这篇文章，介绍我们在挖掘过程中发现的所有新特性。

**阅读更多:** [新开发者特性](https://www.xda-developers.com/android-11-developer-preview-new-development-features/) | [新隐私和安全特性](https://www.xda-developers.com/android-11-developer-preview-privacy-security-features-changes/)

### 预定黑暗主题

这会让很多人开心。顾名思义，你现在可以安排黑暗主题在特定的时间出现。选项和我们得到的夜灯一样:日落到日出或自定义时间。

### 默认情况下启用气泡通知

Android 10 中引入了气泡，我们知道谷歌打算用它们做更多的事情。在 Android 11 DP 1 中，默认开启气泡通知。你仍然需要长按通知并点击“气泡”来使用这个功能，并且应用程序必须实际支持它。你不需要在开发者选项中启用这个选项。

### 通知中的“对话”部分

“通知”下拉菜单中有一个新的“对话”部分这是来自消息应用程序的通知将出现的地方，并且有一些新的快速操作可以对它们进行操作。你可以选择“暂停”一个通知，静音，显示为一个气泡，或者“收藏”，我们不知道这是做什么的。设置图标旁边的删除消息图标(第二个屏幕截图)从对话部分删除通知。

### 快速设置中的屏幕录制切换

如果你拍了很多屏幕录像，你会很高兴看到在快速设置下拉菜单中有一个“屏幕录像”的切换。但是，此时屏幕录制不会捕获内部应用程序音频。

### 免打扰设置的新用户界面

“请勿打扰”再次被重组。异常被组织到人、应用、警报和其他中断中。其他设置是相同的，但移动了一点。

### 新的“每次询问”权限选项

权限在 Android 10 中是一件大事，Android 11 中也有一些新功能。有一个新的“每次询问”选项，这意味着应用程序每次想使用你的相机、联系人等时都会询问你的许可。

### 应用程序不会因为重复的权限请求而烦扰你

有没有对不断询问你权限的应用程序感到沮丧？ [Android 11 将通过阻止应用程序询问权限来阻止这种](https://developer.android.com/preview/privacy/permissions#dialog-visibility),如果你为特定权限轻按两次“拒绝”。

还将考虑这些行动:

*   如果用户按下后退按钮来关闭许可对话框，这不算是“拒绝”动作。
*   如果用户使用 [`requestPermissions()`](https://developer.android.com/reference/androidx/core/app/ActivityCompat#requestPermissions(android.app.Activity,%20java.lang.String%5B%5D,%20int)) 从你的应用进入系统设置，然后按下返回按钮，这个*算不算“拒绝”动作。*

 *### 更多地方的手势设置

Android 10 最显著的变化之一是完整的手势导航系统。在 Android 11 中，手势的设置已经放在了辅助功能设置中，以及设置>系统>手势的旧位置。这应该更容易找到。

### Android 11 动态系统更新开发者选项中的安装程序

[动态系统更新](https://www.xda-developers.com/android-q-dynamic-system-updates-project-treble/)现在在 Android 11 的开发者选项中。在上面的截图中，你可以看到安装动态系统更新包的安装程序是什么样子。

### 在开发者选项中显示显示刷新率的新设置

对于喜欢在屏幕上看到信息的人来说，开发者选项中有一个新的切换来显示当前的显示刷新率。

### 蓝牙设备在飞行模式下保持连接

[正如我们之前报道的](https://www.xda-developers.com/airplane-mode-stop-shutting-down-bluetooth-audio-android-11-r/)，Android 11 改变了飞行模式的行为。如果您当前使用的是连接到手机的蓝牙设备，当您启用飞行模式时，蓝牙将不会关闭。

### Pixel 4 增加了新的触摸灵敏度选项

对于 Pixel 4 用户来说，一个有趣的新功能是显示选项中的[“增加触摸灵敏度”](https://www.xda-developers.com/google-pixel-4-new-increased-touch-sensitivity-option-android-11/)。描述称，它“在使用屏幕保护器时改善了触感。”如果你使用特别厚的屏幕保护，比如钢化玻璃，这是一个很方便的功能。人们是否知道这个开关的存在是另一回事。

回到 2019 年 5 月，戴夫·伯克说他们将在“Android R”中添加对滚动功能的支持。Android 11(艺术家以前称为 Android R)在这里，[也是滚动截图](https://www.xda-developers.com/android-11-scrolling-screenshot-feature/)。但是有一个问题:它还没有工作。我们能够手动激活 UI 元素，如上所示，但是它不起作用。我们可能会在即将发布的版本中看到它。

### 在 Pixel 4 上暂停音乐的新动作感应手势

运动感是 Pixel 4 的一个主要功能，但媒体控制功能非常有限。你只能用它来跳过歌曲或回到上一首歌曲。Android 11 增加了一个播放/暂停音乐的[手势](https://www.xda-developers.com/android-11-new-motion-sense-gesture-pause-music-pixel-4/)，用整只手在显示屏前模仿敲击。

Android 的原生共享菜单近年来变化很大，许多人仍然不喜欢它。在 Android 11 中，谷歌试图通过允许应用程序被钉在菜单上来使其更容易使用。这意味着这些应用程序将永远在顶部，很容易找到。

### 新的放大设置

谷歌在 Android 11 中修改了放大设置页面。第一页显示了“使用快捷方式放大”和“放大设置”选项“设置”页面有放大区域和启用全屏放大的选项。对于这些重要的辅助功能选项，这是一个更好、更有用的菜单。

* * *

请关注这篇文章，因为我们将继续添加更多来自 Android 11 的发现！

**[安卓 11 新闻上 XDA](https://www.xda-developers.com/tag/android-11/)***