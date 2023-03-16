# Android 11 的 Pixel Launcher 在主屏幕上提示应用建议

> 原文：<https://www.xda-developers.com/pixel-launcher-android-11-hints-showing-suggested-apps-home-screen-dock/>

第一个 [Android 11 开发者预览版现在](https://www.xda-developers.com/android-11-developer-preview-1-google-pixel/)可供下载。如果你是谷歌 Pixel 用户，你可以前往我们的指南[为你的设备下载版本](https://www.xda-developers.com/how-to-download-android-11-developer-preview-for-google-pixel-and-other-android-devices/)，然后你可以在这里用[我们的 Pixel 设备指南安装 Android 11 开发者预览版。第一个开发者预览版包括来自 Android 10 的](https://www.xda-developers.com/how-to-install-android-11-r-developer-preview-beta-1-google-pixel-2-3-4-3a-xl/)[数量的变化](https://www.xda-developers.com/android-11-developer-preview-changes/)，一堆[隐私和安全特性](https://www.xda-developers.com/android-11-developer-preview-privacy-security-features-changes/)，以及几个[开发者关注的变化](https://www.xda-developers.com/android-11-developer-preview-new-development-features/)。谷歌计划在稳定的 Android 11 发布之前再发布两个开发者预览版和三个测试版。与此同时，我们将梳理最新版本，寻找下一个 Android 版本中的所有新内容。我们已经在当前版本中发现了许多即将推出的功能，包括针对 Pixel 4 系列的新的[增强触摸灵敏度选项](https://www.xda-developers.com/google-pixel-4-new-increased-touch-sensitivity-option-android-11/)，暂停音乐的[新运动感应手势](https://www.xda-developers.com/android-11-new-motion-sense-gesture-pause-music-pixel-4/)，重新设计的[通知历史](https://www.xda-developers.com/android-11-testing-redesigned-notification-history/)页面，新的[截图预览](https://www.xda-developers.com/android-11-scrolling-screenshot-feature/)，以及更多的。现在，我们在 Android 11 的 Pixel Launcher 中发现了新的代码字符串，指向一个即将到来的名为“hotseat”的功能。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些特性目前还没有在实时构建中实现，并且可能会被开发人员在未来的构建中随时引入。

Pixel Launcher 的当前版本会根据您的活动推荐应用程序。这些建议显示为最近应用程序屏幕下方的一行应用程序，以及应用程序抽屉中的第一行应用程序(如下图所示)。即将推出的“hotseat”功能基于这一行为，并在主屏幕上显示推荐的应用程序，而不是 dock。这些建议的应用程序基于您的使用情况，它们会取代主屏幕上最下面一行的应用程序。

*当前行为*

根据该代码，谷歌将为用户提供选择加入新功能的选项，并将应用程序钉在 hotseat 上——这是应用程序的底部行或主屏幕上的 dock。在设置该功能时，用户将看到几个解释其工作原理的提示，包括将应用程序固定到 hotseat、隐藏建议的应用程序以及手动删除应用程序的说明。该代码还引用了一个 pin 预测功能，该功能很可能会根据您的使用情况建议您应该将哪些应用程序固定到 hotseat。

```
 <string name="hotseat_items_migrated">Your hotseat items have been moved to the last page.</string>
<string name="hotseat_migrate_accept">"I'm in"</string>
<string name="hotseat_migrate_dismiss">No thanks</string>
<string name="hotseat_migrate_message">To pin a favorite app, drag it over a suggested app. To hide a suggested app, touch &amp; hold it.</string>
<string name="hotseat_migrate_prompt_content">Tap to set up</string>
<string name="hotseat_migrate_prompt_title">Get suggested apps on the home screen</string>
<string name="hotseat_migrate_title">Suggested apps replace the bottom row of apps</string>
<string name="hotseat_no_migration">You can remove items from the hotseat manually to see suggested apps in their spot.</string>
<string name="hotseat_onboard_notification_detail">Tap here to set it up</string>
<string name="hotseat_onboard_notification_title">Your hotseat just got smarter</string>
<string name="pin_prediction">Pin Prediction</string> 
```

* * *

*感谢 PNF 软件为我们提供了使用许可 [JEB Decompiler](https://www.pnfsoftware.com/?aid=xdadev) ，这是一款针对 Android 应用的专业级逆向工程工具。*