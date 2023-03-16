# Nova Launcher 和 YouTube 很快就会尊重 Android 10 的黑暗模式

> 原文：<https://www.xda-developers.com/nova-launcher-beta-youtube-android-10-dark-theme/>

**美国东部时间 2019 年 9 月 10 日凌晨 4:30 更新:** YouTube 终于获得了正确的黑暗主题同步。滚动到底部了解更多信息。这篇发表于 2019 年 9 月 18 日的文章被保存如下。

在我看来， [Android 10](https://xda-developers.com/tag/android10) 最好的新功能是全系统黑暗主题切换。当我过去热衷于定制 rom 和主题化的时候，我会尽可能地在每一个应用程序上添加黑暗主题。既然谷歌已经给 Android 添加了一个黑暗主题开关，并鼓励所有开发者添加他们自己的黑暗主题，我就不必再如此频繁地摆弄我的手机了。谷歌通过推出其整个应用套件的更新，引领了在 Android 中采用黑暗主题的努力，但我们也看到了第三方应用，如 [Tasker](https://www.xda-developers.com/tasker-5-8-4-automate-android-10-dark-mode/) 和 [Reddit](https://www.xda-developers.com/reddit-for-android-android-q-dark-mode/) 加入并添加了尊重 Android 10 设置的黑暗模式。现在，流行的 Nova Launcher 应用程序的最新测试版增加了一个新的“系统”主题，遵循 Android 10 的设置，我们发现了 YouTube 应用程序即将添加类似功能的证据。

## Nova 启动器中的系统主题

如果你安装了最新的测试版更新(可从[官方网站](https://help.teslacoilapps.com/beta)或 [Google Play](https://play.google.com/apps/testing/com.teslacoilsw.launcher) 获得)，你会在 Nova 设置的夜间模式下拉列表中看到一个新的“系统”主题。启用此设置将导致 Nova 在 Android 10 中切换主题时自动在亮主题或暗主题之间切换。你已经可以根据你所在位置的自定义时间表或日出/日落时间表来自动化 Nova 的黑暗主题，但由于最近 Tasker 增加了[功能，你将可以更好地控制它。](https://www.xda-developers.com/tasker-5-8-4-automate-android-10-dark-mode/)

与大多数其他应用程序中的黑暗模式不同，Nova Launcher 的黑暗模式更加可定制。你可以[改变背景颜色](https://www.xda-developers.com/nova-launcher-different-night-mode-color-option/)并切换启动器的哪些部分被主题化，包括搜索栏、应用抽屉、抽屉图标或文件夹。最近的测试版更新甚至增加了对谷歌发现提要中[切换黑暗模式的支持。](https://www.xda-developers.com/nova-launcher-61-beta-dark-google-discover-numeric-dots-support/)

* * *

## YouTube 中正在进行的系统主题

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些特性目前还没有在实时构建中实现，并且可能会被开发人员在未来的构建中随时引入。

谷歌去年在 YouTube 应用程序中广泛推出了[黑暗模式，但你必须在“通用”设置中手动启用它。最新 14.38.50 更新中的字符串透露，YouTube 应用程序将添加一个“系统”主题设置，该设置尊重 Android 10 中的黑暗模式偏好。](https://www.xda-developers.com/youtube-dark-mode-android-roll-out/)

```
 <string name="app_theme_appearance_dark">APPEARANCE_DARK</string>
<string name="app_theme_appearance_entry_dark">Dark theme</string>
<string name="app_theme_appearance_entry_light">Light theme</string>
<string name="app_theme_appearance_entry_system">Use device theme</string>
<string name="app_theme_appearance_light">APPEARANCE_LIGHT</string>
<string name="app_theme_appearance_summary">Choose your light or dark theme preference</string>
<string name="app_theme_appearance_system">APPEARANCE_SYSTEM</string>
<string name="app_theme_appearance_title">Appearance</string>
<string name="auto_switched_to_dark_by_device_theme">Dark theme is on to match your device theme</string>
<string name="auto_switched_to_light_by_device_theme">Light theme is on to match your device theme</string>
<string name="theme_not_match_with_system_theme">"New! Set YouTube's appearance to always match your device theme"</string> 
```

我在运行 Android 10 的 Pixel 2 XL 和一加 7 Pro 上更新到了最新版本，但新的偏好设置在这两款设备上都没有显示。我怀疑在未来几周更广泛地推出之前，它将很快通过服务器端更新对一些用户可用。到时候我们会通知你的。

* * *

## 更新:YouTube 黑暗主题同步现已推出

黑暗主题同步已经开始在 YouTube 上推广。这一服务器端的变化现在允许 YouTube 尊重你的系统设置，或者你可以根据自己的喜好选择将应用程序锁定在亮或暗的主题中。这种改变是在服务器端进行的，但是你需要在 v14.38.50 或更高版本上才能看到。如果你在找更高的版本，可以从 APKMirror 下载 [v14.40.52](https://www.apkmirror.com/apk/google-inc/youtube/youtube-14-40-52-release/) 。

**来源:[安卓警察](https://www.androidpolice.com/2019/10/08/youtube-dark-theme-android-10/)**