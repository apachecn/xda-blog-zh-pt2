# Android P 可能支持阻止来自未知、私人和付费电话号码的呼叫

> 原文：<https://www.xda-developers.com/android-p-blocking-calls-unknown-private-pay-phone-numbers/>

**更新 10:18PM CST 3/8/18** :今晚，负责以下变更的提交已经合并到主分支。除非将来有一系列的提交来恢复这些更改，这意味着你应该期待这些增强的呼叫阻塞功能会在 Android P Developer Preview 2 中出现。

我们即将发布第一个 [Android P](https://www.xda-developers.com/tag/android-p/) 开发者预览版(根据 AOSP 的活跃程度来判断)，但在 Android 的下一个主要版本中仍有一些可能即将推出的功能。我们最近了解到可能的[原生虹膜扫描仪支持](https://www.xda-developers.com/iris-scanners-native-support-android-p/)，隐私调整，如阻止[摄像头](https://www.xda-developers.com/android-p-background-apps-camera/)和[麦克风](https://www.xda-developers.com/android-p-audio-recording-limitations-privacy/)从闲置应用程序访问，以及更多[更多](https://www.xda-developers.com/tag/android-p/)。现在，我们看到了另一个正在开发的功能:增强的呼叫阻塞功能。

来自索尼工程师的一组新的承诺出现在 AOSP gerrit 中。索尼工程师最近在 Android 中进行了大量与运营商相关的变化，例如让运营商能够[定义 LTE 信号栏](https://www.xda-developers.com/android-p-carriers-define-lte-signal-bars/)，[隐藏设置中的信号强度](https://www.xda-developers.com/android-p-signal-strength-carriers/)，以及[在设置中添加全国漫游切换](https://www.xda-developers.com/android-p-national-roaming-toggle/)，所以看到他们的另一个变化并不令人惊讶。这一次的变化对用户来说更加友好，因为[提交](https://android-review.googlesource.com/q/topic:%22enhanced_call_blocking_function%22+(status:open%20OR%20status:merged))给[默认拨号器应用](https://www.xda-developers.com/tag/google-dialer/)添加了新功能:阻止未知号码、私人号码、付费电话或任何不在你联系人列表中的号码的来电。

*运行[安卓 8.1 奥利奥](https://www.xda-developers.com/android-8-1-oreo-final-release-imminent/)* 的[谷歌 Pixel 2 XL](https://www.xda-developers.com/tag/google-pixel-2/) 上已有的来电屏蔽功能

目前，您只能基于每个号码阻止呼叫。你屏蔽的号码必须手动添加，这意味着你基本上只能在事后屏蔽不需要的号码。但是，通过这些新设置，您可以限制允许谁给您打电话，这样您就不会被不想要的电话打扰了。

以下是将在拨号器应用程序的新阻止号码设置中显示的文本字符串。

### 增强的呼叫阻止功能

```

<string name="phone_settings_call_blocking_txt">Call Blocking</string>

<string name="phone_settings_number_not_in_contact_txt">Numbers not in Contacts</string>

<string name="phone_settings_number_not_in_contact_summary_txt">Block numbers that are not listed in your Contacts</string>

<string name="phone_settings_private_num_txt">Private</string>

<string name="phone_settings_private_num_summary_txt">Block callers that do not disclose their number</string>

<string name="phone_settings_payphone_txt">Pay phone</string>

<string name="phone_settings_payphone_summary_txt">Block calls from pay phones</string>

<string name="phone_settings_unknown_txt">Unknown</string>

<string name="phone_settings_unknown_summary_txt">Block calls from unidentified callers</string>

<string name="phone_strings_call_blocking_turned_off_notification_title_txt">Call Blocking</string>

<string name="phone_strings_call_blocking_turned_off_notification_text_txt">Call Blocking disabled</string>

<string name="phone_strings_emergency_call_made_dialog_title_txt">Emergency call made</string>

<string name="phone_strings_emergency_call_made_dialog_call_blocking_text_txt">Call Blocking has been disabled to allow emergency responders to contact you.</string> 
```

根据字符串，您可以在以下情况下阻止电话号码:

*   电话号码不在您的联系人列表中
*   呼叫者不会透露电话号码(私人)
*   电话号码来自付费电话
*   电话号码没有任何呼叫者 ID 信息(未知/未识别)

如果用户拨打紧急电话，呼叫阻止将被禁用，这是有意义的，因为当有人遇险时，紧急响应人员必须能够联系到他们。在回应一位谷歌员工的评论时，索尼工程师提到,“运营商要求”显示一个持续通知，告诉用户在紧急呼叫后呼叫阻止已被禁用，因此在这些情况下用户不应感到困惑或恐慌。

最后，这些新的增强呼叫阻止功能似乎只有在运营商允许的情况下才可用，这令人失望。我们可以想象某些运营商试图向你出售这些呼叫阻塞功能，作为“增值”套餐的一部分。

最终，这将是对 Android 的一个巨大改变。虽然 Play Store 上有许多免费的呼叫阻止应用程序，但你基本上相信该应用程序不会对你的呼叫历史做任何事情。有了内置功能，你就不用担心这个问题了。

现在，请记住，这项功能实际上还没有在 AOSP 合并。这意味着它还没有被证实会搭载 Android P，但很有可能会。一名谷歌员工在审阅补丁时表示，他们“非常支持这一整体变化”，因此它很可能会很快被合并。它可能不会出现在第一个 Android P 开发者预览版中，但正如我们在 Android Oreo 开发者预览版中看到的那样，即使在提交合并之前最初的预览版下降了，仍然有可能添加新功能。