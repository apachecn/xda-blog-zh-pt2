# Android 11 屏幕录制器可能很快会支持录制内部音频

> 原文：<https://www.xda-developers.com/android-11-screen-recorder-internal-audio/>

最初的几个 Android 10 开发者预览版在 SystemUI 中有一个准系统屏幕记录器，但在发布时用户无法访问该功能。然而，随着第一个 [Android 11 开发者预览版](https://www.xda-developers.com/android-11-developer-preview-2-changes/)，屏幕记录器变得可以从快速设置磁贴中访问。现在在 Android 11 开发者预览版 2 中，屏幕记录器有一个改进的 UI，通知用户记录敏感信息的可能性，并让用户选择他们是否希望记录麦克风的音频和/或在屏幕上显示轻敲。然而，目前没有办法记录设备上播放的音频，但在未来的预览版中可能会有所改变。

*从左到右:屏幕记录快速设置磁贴、屏幕记录下拉选项、新屏幕记录倒计时、新屏幕记录状态栏指示器。*

Android 11 中的 SystemUI 增加了与屏幕记录功能相关的新字符串。这些字符串表明您将能够录制“来自您设备的声音，如音乐、通话和铃声”

```
 <string name="screenrecord_device_audio_and_mic_label">Device audio and microphone</string>
<string name="screenrecord_device_audio_description">Sound from your device, like music, calls, and ringtones</string>
<string name="screenrecord_device_audio_label">Device audio</string> 
```

这个文本目前在屏幕记录功能中不可见，并且在 Android 11 中负责屏幕记录的三个类中的任何一个中都没有记录内部设备音频的能力的指示:RecordingController、RecordingService 和 ScreenRecordDialog。Android 10 [使得应用程序可以通过 audiopaybackcapture API](https://www.xda-developers.com/android-q-record-audio-monitor-device-temperature/)录制来自其他应用程序[的音频](https://developer.android.com/guide/topics/media/playback-capture)。事实上，[谷歌 Play 商店](https://www.xda-developers.com/android-10-record-internal-game-audio/)上已经有第三方应用程序利用这个 API 让你从你的设备上捕捉视频和音频。我测试了 Android 11 DP2 中改进的屏幕录制功能，以确保它不支持录制内部音频，遗憾的是，它仍然只支持录制麦克风的音频。为了进行自我测试，请尝试开始屏幕录制，然后在大声说话的同时在 Google 相册中打开一个视频——如果您可以听到自己在屏幕录制中对着视频说话，那么很可能只是从麦克风录制音频。当然，我将这个结果与我提到的使用该 API 的第三方应用程序进行了比较。

假设谷歌确实允许你在未来的 Android 11 预览版中录制内部设备音频，我不确定它是否真的有用。虽然以 Android 10 为目标的应用程序默认允许其音频由使用 AudioPlaybackCapture API 的应用程序捕获，但以 Android 9 Pie 为目标的应用程序必须通过在其清单文件中启用 allowAudioPlaybackCapture 标志来选择加入。如果音频被声明为媒体、游戏或未知类型，也只能被捕获。系统应用程序，如 SystemUI，也能够从应用程序录制音频，即使它们的音频采集策略设定为 ALLOW_CAPTURE_BY_SYSTEM，但如果是这种情况，它们也不允许存储音频。

由于屏幕记录是“com.android.systemui”的一部分，而不是“com.google.android.systemui”，这意味着该功能很可能会成为 AOSP 的一部分。因此，其他智能手机制造商的设备一旦升级到 Android 11，就应该能够享受这一功能，当然，除非 OEM 已经有了类似或更好的屏幕记录器。很多 OEM 屏幕录像机让你改变录制的分辨率、比特率和帧速率，所以谷歌的仍然是相当准系统，即使他们增加了录制内部设备音频的能力。