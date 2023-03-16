# 驾驶模式会自动启动 Android Auto 或者勿扰

> 原文：<https://www.xda-developers.com/android-pie-driving-mode-android-auto-do-not-disturb/>

Android 9 Pie 的一个关键主题是更智能的操作系统。Android 已经全面采用了自动检测用户正在做什么并相应调整设置的功能。Android Pie 中新的自适应电池和亮度算法只是 Android 如何发展以更好地识别您的个人用例的两个例子。除了几个月前我们[在 settings intelligence](https://www.xda-developers.com/android-p-predictive-settings-automate-frequent-settings/)中发现的新功能之外，谷歌似乎正在测试 Google Play 服务版本 14.3.62 中一个名为“驾驶模式”的功能当激活时，该功能将使用各种运动传感器、背景音频提示(如发动机噪音)和/或蓝牙连接来确定您是否在移动的车辆中，如果是。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些功能目前还没有在 live build 中实现，可能会在未来的版本中随时被 Google 拉出来。

## Google Play 服务中的驾驶模式

驾驶模式的目的是通过自动启动汽车友好应用程序(Android Auto)或在行驶中的车辆上防止分心(请勿打扰模式)，让你专注于驾驶。它通过使用谷歌[在三月](https://android-developers.googleblog.com/2018/03/activity-recognitions-new-transition.html)开放的 [ActivityTransition API](https://developers.google.com/android/reference/com/google/android/gms/location/ActivityTransition) 来实现。这个 API 是谷歌 Pixel 2 上的 Pixel 环境服务如何能够在驾驶时[自动启用请勿打扰模式，也是 Tasker 的](https://www.xda-developers.com/pixel-2-do-not-disturb-mode-driving/) [Detact 插件](https://www.xda-developers.com/detact-tasker-plugin-automate-daily-routine/)如何工作。谷歌可能会在未来的 Google Play 服务更新中为所有设备带来这一 Pixel 2 特有的功能。

```
 <string name="car_driving_mode_activity_recognition_auto_launch_summary">From motion and Bluetooth connections</string>
<string name="car_driving_mode_audio_activity_recognition_auto_launch_summary">From motion, Bluetooth, and audio cues</string>
<string name="car_driving_mode_frx_autolaunch_ar_trigger_section_header">When driving is detected</string>
<string name="car_driving_mode_frx_autolaunch_ar_trigger_summary">Allows driving mode to use sensors and background audio cues like engine noise to detect when you’re in a car.</string>
<string name="car_driving_mode_frx_autolaunch_bluetooth_trigger_section_header">When connected to Bluetooth</string>
<string name="car_driving_mode_frx_autolaunch_trigger_header">Select when to turn on driving mode automatically</string>
<string name="car_driving_mode_frx_choose_behavior_header">Select what you want driving mode to do</string>
<string name="car_driving_mode_frx_intro_body">Your device uses motion and Bluetooth connections to figure out when you’re in a moving vehicle.&lt;br/>&lt;br/>Driving mode can then turn on automatically, and open Android Auto to help you stay connected while driving.</string>
<string name="car_driving_mode_frx_intro_body_audio_enabled">Your device uses motion, Bluetooth connections and background audio cues like engine noise to figure out when you’re in a moving vehicle.&lt;br/>&lt;br/>Driving mode can then turn on automatically, and open Android Auto to help you stay connected while driving.</string>
<string name="car_driving_mode_frx_intro_body_car_dock">Driving mode makes it easy to use your phone while keeping your eyes on the road.&lt;br/>&lt;br/>When you place your phone in this dock, Android Auto can open automatically to help you stay connected while driving.</string>
<string name="car_driving_mode_frx_intro_header">Use driving mode</string> 
```

我设法在我运行 Android Pixel 2 XL 和 OnePlus 6 的谷歌 Pixel 2 XL 上激活了这项新功能。下面是展示设置过程和设置的截图。Android Auto 能够在检测到你连接到白名单蓝牙设备时自动启动，但这种新的驾驶模式通过检查你的运动和背景音频更进了一步。该功能将无法判断你是司机还是乘客，但幸运的是，在启用驾驶模式之前，它有一个询问你许可的选项。

一旦该功能上线，你会在 Android Pie 的连接首选项中看到一个新选项。作为奖励，我们还设法启用了设置“Better Together”的菜单，即将推出的 Chrome OS/Android 集成将在一个横幅下耦合即时共享、轻松解锁和 Android 消息同步。“Better Together”现在出现在播放服务中的事实很有希望，因为以前它是作为 Pixel 2 上的预装系统应用程序提供的。我们希望这意味着该功能将适用于所有 Android 设备，但我们必须等待，看看谷歌在 10 月 9 日宣布什么。如果你想知道的话,“了解更多”链接目前指向谷歌支持网站上[这个无法访问的页面](https://support.google.com/chromebook/answer/9094445?p=better_together)。

最后，我们使用 PNF 软件提供的 [JEB 反编译器来测试最新的 Play 服务版本。虽然它帮助我们激活了新功能，但我们没有发现任何其他新功能。如果我们有新的发现，我们会告诉你们的。JEB Decompiler 未来会帮助我们为大家带来更多高质量的 app 拆机，敬请期待！](https://www.pnfsoftware.com/?aid=xdadev)