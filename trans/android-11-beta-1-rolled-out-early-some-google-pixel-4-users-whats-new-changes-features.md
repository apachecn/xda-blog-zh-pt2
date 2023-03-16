# Android 11 Beta 1 向一些 Pixel 4 用户提前推出:以下是新内容

> 原文：<https://www.xda-developers.com/android-11-beta-1-rolled-out-early-some-google-pixel-4-users-whats-new-changes-features/>

第一个 Android 11 开发者预览版于二月份发布，随后是[预览版 2](https://www.xda-developers.com/android-11-developer-preview-2-changes/) 、[预览版 3](https://www.xda-developers.com/android-11-developer-preview-3-changes/) ，以及最近的[预览版 4](https://www.xda-developers.com/google-android-11-beta-june-3-2020-developer-preview-4-live-release/) 。谷歌本应在 6 月 3 日发布 Android 11 Beta 1，但因为种种原因， [Beta 发布会被无限期推迟](https://www.xda-developers.com/google-android-11-beta-june-3-2020-developer-preview-4-live-release/)，与 Beta 版一同发布。然而，Android 11 Beta 1 仍然提前向一些谷歌 Pixel 4 用户推出。他们设法从谷歌获得了最新的官方软件更新，并与我们分享了 Android 11 Beta 1 版本的所有新内容！

**[所有安卓 11 新闻](https://www.xda-developers.com/tag/android-11/)**

## Android 11 Beta 1 中的新功能

Android 11 开发者预览版 1 测试了一个颇有争议的举动:将音乐播放器通知移到快速设置面板，让它和其他开关放在一起。为了容纳音乐播放器，快速设置面板将从一行扩展到两行，并将在一侧显示快速设置切换，而音乐播放器将占据另一侧。通过再次向下滑动来完全打开快速设置面板会将音乐播放器移动到面板的底部，所有的开关都在它的正上方。

这个特性存在于构建中，但是不容易访问，必须手动启用。随着 Android 11 Beta 1 的推出，这项功能现在终于可以作为一个选项使用了。变化是音乐播放器现在已经移动到折叠视图中开关的另一侧，并且移动到展开视图中开关的顶部。

当它最终到达 Android 11 的官方稳定版本时，该功能还可能进一步改变。

### 新图标形状:锥形矩形，卵石，容器

随着 Pixel 4 的发布，谷歌推出了 [Pixel Themes](https://www.xda-developers.com/december-2019-android-security-patches/) 应用。Pixel Themes 允许您从大量预安装的选项中自定义 UI 的某些部分，如字体、强调色、图标形状和图标填充。开发者预览版 4 增加了两个新的图标形状选项:六角形和花朵。现在，这个列表已经[增加了三个图标形状](https://twitter.com/MishaalRahman/status/1267554366342471682):锥形矩形、卵石形和容器形。

如果这种模式继续下去，我们可以希望在未来的测试版中看到更多的图标形状。

Android 11 的关键特性之一是控件 API，它将允许开发者在电源菜单中设置家庭自动化快捷方式。在 Android 11 的早期预览版中，顶部电源菜单项下方有一个“快速控制”部分，而电源菜单的其余部分是透明的。在 Android 11 开发者预览版 4 中，电源菜单背景是深色的，包括顶部的电源菜单项。此外，“快速控制”现在说“设备控制”，并有一个描述文本时，它是空的，说“为您连接的设备添加控制”。当您从支持的应用程序添加控件时，此文本会消失，以便为您喜爱的控件腾出空间。

Beta 1 带来了新的“能量菜单”设置，这将控制卡和通行证，并控制能量菜单中的功能。

动画为我们在电源菜单上能看到什么提供了进一步的指导:

收到新更新的用户无法测试新的“设备控制”功能，因为还没有可供最终用户测试控制 API 的应用程序。当谷歌举办测试发布会时，这种情况应该会改变。

### 在 Pixel Launcher 中控制应用程序建议

自定义字符串在 Pixel Launcher 中继续。开发者预览版 4 带来了网格大小定制，手势教程，从建议行中删除应用的能力，以及混合 hot seat——建议替换 dock 中缺失的位置。Beta 1 现在提供了控制应用建议的能力，以及一些向新用户介绍该功能的 onboarding 消息。

上下文相关的 hotseat 特性也有一个有用的动画:

谷歌去年在[的第二个安卓 Q 测试版](https://www.xda-developers.com/android-q-beta-2-notification-bubbles/)中引入了[泡泡](https://developer.android.com/guide/topics/ui/bubbles)。该功能将允许用户以浮动覆盖的形式查看消息应用程序的通知和对话，非常类似于 Facebook Messenger 的聊天标题。它没有在 Android 10 的稳定版本中正式宣布，而是隐藏在开发者选项中。随着 [Android 11 开发者预览版 1](https://www.xda-developers.com/android-11-developer-preview-1-google-pixel/) ，谷歌[引入了新功能](https://www.xda-developers.com/android-11-developer-preview-changes/)，例如能够[只对气泡区域](https://www.xda-developers.com/android-11-tests-partial-screenshots-bubble-messages/)而不是整个屏幕进行截图。

Android 11 默认支持气泡通知，现在 Beta 1 新增了启用气泡通知的子菜单。此子菜单位于“设置”>“应用程序与通知”>“通知”>“气泡”。

这是页面上显示的动画:

### 新的开发者选项:“Wi-Fi 增强的 MAC 随机化”

从 Android 8.0 开始， [Android 设备在当前没有与网络关联的情况下探测新网络时，使用随机 MAC 地址](https://source.android.com/devices/tech/connect/wifi-mac-randomization)。在 Android 9 中，你可以启用一个开发者选项(默认情况下**被禁用**)，让设备在连接 Wi-Fi 网络时使用随机 MAC 地址。在 Android 10 中，默认情况下，客户端模式、SoftAp 和 Wi-Fi Direct 会启用 MAC 随机化。

Android 11 Beta 1 引入了一个新的开发者选项，称为 Wi-Fi 增强的 MAC 随机化。此功能允许在每次手机连接到启用了 MAC 随机化的 Wi-Fi 网络时更改 MAC 地址。

### 辅助功能设置的图形

这是一个相对较小的变化。Android 11 Beta 1 在一些辅助功能设置中增加了一些图形，即对讲和选择说话。

* * *

## Android 11 Beta 1 中正在开发的功能

这些功能在 Android 11 Beta 1 中存在，但它们处于不同的完成阶段，还没有准备好。我们可以期待在未来的版本中看到这些特性。

Android 11 开发者预览版 1 包含了一个[新的截图预览](https://www.xda-developers.com/android-11-scrolling-screenshot-feature/)，暗示支持滚动截图。不幸的是，滚动截图仍然没有在 Beta 1 上发布。

### 锁定屏幕可能的时钟定制

在“设置”>“风格和壁纸”中有一个新条目，叫做“时钟”。此设置面板仅包含锁定屏幕的默认时钟选项。这暗示着在未来的测试版中可能会添加更多的自定义或样式选项。

* * *

这就是我们在这个版本中所能找到的全部内容。我们预计谷歌会在 Android 11 测试版发布会播出时透露更多关于即将推出的功能的信息。关注我们的 Android 11 新闻标签，了解到目前为止我们在下一个 Android OS 版本中报道的所有最新消息。

**[所有安卓 11 新闻](https://www.xda-developers.com/tag/android-11/)**