# 谷歌在 Android Q 上测试自动汽车碰撞检测像素

> 原文：<https://www.xda-developers.com/google-tests-automatic-car-crash-detection-pixel-android-q-beta/>

[Google I/O 2019](https://www.xda-developers.com/tag/google-io-2019/) 是当前的热门话题，因为每个人都希望更深入地了解 Google 在其产品和服务组合中发布的所有公告。在活动中，我们了解到了 [Android Q Beta 3](https://www.xda-developers.com/android-q-beta-3-released/) 的变化和[的功能，如黑暗模式、新的导航手势](https://www.xda-developers.com/everything-new-android-q-beta-3/)、数字福利的改进、通知通道建议、[项目主线以实现更快的安全更新](https://www.xda-developers.com/android-q-project-mainline-security/)、[气泡](https://www.xda-developers.com/android-q-system-alert-window-deprecate-bubbles/)、[直播字幕](https://www.xda-developers.com/google-accessibility-live-caption-android-q-live-relay-live-transcribe/)等等。这些公告只是触及了表面，因为在谷歌在此次活动中披露的新资源中，将会发现更多有趣的花絮。例如，谷歌现在正在测试其 Pixel 设备的车祸检测功能。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些功能目前还没有在 live build 中实现，可能会在未来的版本中随时被 Google 拉出来。

Android Q Beta 3 采用了名为“安全中枢”的新谷歌应用，包名为*com . Google . Android . apps . Safety Hub*。该应用程序的功能是像素专属的，这一点从清单声明中可以明显看出:

```
 <uses-feature android:name="com.google.android.feature.PIXEL_EXPERIENCE" android:required="true"/> 
```

应用程序中出现的字符串暗示谷歌正在开发一项功能，该功能可以检测出你何时遭遇车祸:

```
 <string name="car_crash_alert_icon_description">Car crash icon</string>
<string name="car_crash_detection_dogfood_title_text">Car Crash Detection Dogfood</string>
<string name="car_crash_dogfood_app_name">Car Crash Dogfood</string>
<string name="car_crash_permission_preference_title">@string/car_crash_permissions_menu_item_text</string>
<string name="car_crash_permissions_menu_item_text">Car Crash Dogfood Permissions</string>
<string name="dogfood_welcome_text">\u0009Welcome to the car crash detection dogfood. 
```

此功能的应用程序中还包含两种图形资源:

虽然这些字符串暗示了汽车碰撞的自动检测，但还不清楚这种检测将如何实现。谷歌可以求助于使用来自加速度计和麦克风的数据，但即使这样，它的检测也可能不可靠。这些字符串也没有透露一旦检测到碰撞会发生什么——我们猜测该应用程序可能会警告第一反应者或电话上列出的紧急联系人。希望未来的 Q Betas 版会揭示更多关于这个应用程序如何工作以及它会做什么的信息。

* * *

感谢《XDA》的主编米莎尔·拉赫曼发现了这一点。

*感谢 PNF 软件公司为我们提供了使用[反编译器](https://www.pnfsoftware.com/?aid=xdadev%22%3EJEB)的许可，这是一款针对 Android 应用的专业级逆向工程工具。*