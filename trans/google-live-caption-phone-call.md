# 谷歌正准备让你在打电话时使用“实时字幕”

> 原文：<https://www.xda-developers.com/google-live-caption-phone-call/>

谷歌在去年的 Google I/O 2019 上首次公布了其“[直播字幕](https://ai.googleblog.com/2019/10/on-device-captioning-with-live-caption.html)”辅助功能[。该功能使用三种设备上的机器学习模型，可以检测媒体中的英语语音，并自动生成字幕。该功能最初在 Pixel 4 上可用，但后来扩展到了](https://www.xda-developers.com/google-accessibility-live-caption-android-q-live-relay-live-transcribe/) [Pixel 3a、](https://www.xda-developers.com/december-2019-android-security-patches/)、 [Pixel 2、](https://www.xda-developers.com/live-caption-pixel-2-update/)、[三星 Galaxy S20](https://www.xda-developers.com/samsung-galaxy-s20-google-live-caption/) 、[一加 7T](https://www.xda-developers.com/oneplus-7t-pro-open-beta-1-build-live-caption-support/) 和[一加 8](https://www.xda-developers.com/oneplus-8-series-update-adds-live-caption-bullets-wireless-z-integration-dolby-atmos/) 。然而，自该功能推出以来，它尚未收到任何功能更新。不过，这种情况可能很快就会改变，因为我们发现有证据表明，谷歌将允许电话直播字幕。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些特性目前还没有在实时构建中实现，并且可能会被开发人员在未来的构建中随时引入。

在谷歌 Pixel 4 的 Android 11 开发者预览版 3 中，我们分析了负责直播字幕的应用程序设备个性化服务的 2.13.302920511 版本。其中，我们发现了一些字符串，表明用户可以通过电话打开直播字幕。

```
 <string name="call_confirmation_cancel">CANCEL</string>
<string name="call_confirmation_confirmation_message">Enable Live Caption over this phone call? Your use of the feature will be annonunced to others on the call.</string>
<string name="call_confirmation_dialog_name">Enable Live Caption confirmation dialog</string>
<string name="call_confirmation_enable">ENABLE</string>
<string name="call_other_side_transcription_prefix">Caller</string>
<string name="call_system_message_prefix">System</string>
<string name="call_turn_indicator_text">…</string>
<string name="call_user_typed_input_prefix">You typed</string> 
```

通过电话呼叫启用该功能将向所有参与者宣布该呼叫正在被转录成字幕。电话中会播放一个音频文件，这个音频文件简单地说了下面一行:

```
 <string name="system_message_start_call_speaking_mode">Hi, the person you’re about to speak with has call captions turned on. They’ll see captions of what you say to help them listen along.</string> 
```

目前，直播字幕所依赖的 API AudioPlaybackCaptureConfiguration，[不允许](https://developer.android.com/guide/topics/media/playback-capture#allowing_playback_capture)捕捉语音通话音频。然而，有可能在 Android 11 开发者预览版 3 中添加的[新系统专用权限将允许该功能绕过这一限制。](https://twitter.com/MishaalRahman/status/1253390680040394752)

* * *

*感谢 PNF 软件为我们提供了使用许可 [JEB Decompiler](https://www.pnfsoftware.com/?aid=xdadev) ，这是一款针对 Android 应用的专业级逆向工程工具。*