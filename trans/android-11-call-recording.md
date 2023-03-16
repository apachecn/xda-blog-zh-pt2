# Android 11 DP2 透露谷歌正在为拨号程序添加通话录音

> 原文：<https://www.xda-developers.com/android-11-call-recording/>

对于许多通过语音通话开展业务的用户来说，记录电话通话的能力至关重要。它对任何涉及法律、保险或医疗事务的人都非常有用。然而，对大多数用户来说，在 Android 上记录电话并不容易。虽然有些 OEM 在他们的拨号器应用程序中提供呼叫记录功能，但并不是每个 OEM 都提供此功能。第三方应用过去可以使用迂回的方法记录电话，但 [Android 9 Pie 使第三方应用完全无法](https://www.xda-developers.com/android-pie-blocks-non-root-call-recording-apps/)记录电话，至少在没有 root 访问权限的情况下。去年，谷歌表示他们正在[考虑在未来的 Android 版本中添加一个呼叫记录 API](https://www.xda-developers.com/future-android-version-call-recording/) ，看起来这可能最终会在 Android 11 中实现。

今天早些时候，谷歌发布了 [Android 11 开发者预览版 2](https://www.xda-developers.com/android-11-developer-preview-2-google-pixel-announcement-changelog/) 。在深入研究新的框架变化时，我们发现了一个名为“ACCESS_CALL_AUDIO”的新权限，其保护级别为“appop”或“signature”。有趣的是,“appop”权限实际上可以授予非系统应用程序，不像“signature”权限要求应用程序由 OEM 签名。深入挖掘后，我们发现新的字符串更加详细地描述了这个权限。根据一个字符串，这个权限只能授予默认的拨号器应用程序，它允许应用程序“在电话通话中录制或播放音频”

```
 <permission android.label="@string/permlab_accessCallAudio" android:description="@string/permdesc_accessCallAudio" android:name="android.permission.ACCESS_CALL_AUDIO" android:protectionLevel="appop|signature"/>
<string name="permdesc_accessCallAudio">Allows this app, when assigned as default dialer application, to record or play audio in telephony calls.</string>
<string name="permlab_accessCallAudio">Record or play audio in telephony calls</string> 
```

我们很高兴看到 Android 11 中可能引入对第三方拨号应用程序的呼叫记录支持。谷歌终于[在谷歌手机应用](https://www.xda-developers.com/google-phone-app-call-recording-hands-on/)中添加了对 Pixel 设备的通话记录支持，但大多数设备都无法使用 Pixel 的 dialer 应用。通过这一更改，在 stock dialer 应用程序中没有呼叫记录支持的设备上的用户将能够从谷歌 Play 商店下载不同的 dialer 应用程序来记录他们的电话呼叫。