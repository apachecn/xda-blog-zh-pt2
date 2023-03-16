# Android P 可能会添加“预测设置”来自动切换设置

> 原文：<https://www.xda-developers.com/android-p-predictive-settings-automate-frequent-settings/>

Android P 将给我们钟爱的操作系统带来一系列变化。从[自动颜色模式调整](https://www.xda-developers.com/pixel-2-android-p-automatic-color-mode/)到[允许开发者调整他们的音频输出](https://www.xda-developers.com/android-p-fine-tune-audio-output/) - Android P 将改进 Android 的许多现有优势，给用户带来真正“智能”的智能手机体验。

我们发现了即将推出的功能集的提示，这些功能集可能会改善您一天中处理设备的方式。在 Android P Developer Preview 2 中被称为“设置建议”,这款应用程序提到了一个似乎可以自动进行频繁切换设置的系统。

在您授予应用程序必要的权限后，这些自动化提示可能会由您的日历和位置数据触发，尽管我们发现的提示也表明其他设置不依赖于这些数据。

以下是我们在 APK 中找到的字符串，打包为*com . Google . Android . settings . intelligence*:

```
 <string name="predictive_ringer_notification_title">Ringer suggestion</string>
<string name="predictive_settings_ringer_silence_description">You usually mute your phone at this time</string>
<string name="predictive_settings_ringer_silence_title">Tap to silence your phone</string>
<string name="predictive_settings_ringer_turn_on_description">You usually turn on your ringtone at this time</string>
<string name="predictive_settings_ringer_turn_on_title">Turn on your ringtone</string>
<string name="predictive_settings_ringer_vibrate_description">You usually set phone to vibrate at this time</string>
<string name="predictive_settings_ringer_vibrate_title">Tap to set phone to vibrate only</string>

<string name="feedback_body_notification">Please provide your feedback here</string>
<string name="feedback_chooser_text">Select an email app</string>
<string name="feedback_email">pixel-predictive-settings-feedback@google.com</string>
<string name="feedback_subject_notification">Predictive Settings Notification Feedback</string>
<string name="feedback_text">Feedback</string>

<string name="permission_dialog_accept_button">Got it</string>
<string name="permission_dialog_description">"%s uses your location and calendar to provide personalized suggestions based on your routines. If you don't allow location and calendar permissions, you may still receive other suggestions."</string>
<string name="permission_dialog_reject_button">Deny permissions</string>
<string name="permission_dialog_title">Get personalized setting suggestions</string> 
```

这个应用程序目前显示“开车时使用蓝牙”功能(从开发者预览版 1 开始，通过在开发者选项>功能标志中切换它，它已经可见)，但该功能本身目前并不工作。对于其余的功能集，我们怀疑一旦你确认你的切换活动的例行性质，应用程序可能会自动执行功能，直到你以某种方式中断相同的功能。

*当前预测设置*

从 Developer Preview 2 开始，这些特性都不起作用。而且当 Android P 退出开发者预览版时，也不能保证它们能准备好公开发布。尽管如此，这些迹象表明，Android P 可能只是引入了自动化日常切换需求的基石。