# 新的 Play Store 政策将从 5 月 11 日起终止第三方通话录音应用

> 原文：<https://www.xda-developers.com/google-kill-third-party-call-recording-apps-android/>

内置的通话记录器是 MIUI 和 ColorOS 等定制 OEM 皮肤的主食。它还预装在谷歌 Pixel 手机上，集成到手机应用程序中。但由于地区法律的原因，它并不能在安卓手机上普遍使用。如果你的手机没有这项功能，你可以从谷歌 Play 商店安装一个第三方应用来完成这项工作。但不幸的是，即将到来的 Google Play 政策变化将一劳永逸地扼杀所有第三方通话记录应用。

多年来，谷歌一直积极阻止安卓系统上的通话录音。在 Android 6.0 中，谷歌取消了官方的通话记录 API，该 API 允许开发人员轻松地将通话记录功能嵌入他们的应用程序中。这促使应用程序开发人员寻找非官方的[方式来启用通话记录](https://www.xda-developers.com/how-to-record-calls-android/)。但是，谷歌[在 Android 9.0](https://www.xda-developers.com/android-pie-blocks-non-root-call-recording-apps/) 中又取消了一些变通办法。在 Android 10 中，该公司完全禁止通过麦克风进行通话录音。

作为最后的手段，开发者开始使用 Android 的无障碍服务，在运行 Android 10 及以上版本的设备上提供通话录音。谷歌现在宣布，它将不允许第三方应用程序使用可访问性 API 进行通话录音，这意味着第三方通话录音应用程序的终结。

谷歌更新后的 Play Store 政策展示了易访问性 API 的几个变化。其中一项变化将阻止第三方应用程序开发人员使用 API 进行通话录音。这一变化将于 5 月 11 日生效。

> 辅助功能 API 不是为远程呼叫录音而设计的，也不能被请求。

在最近的一次开发者网络研讨会上，谷歌澄清了这一变化只会影响第三方应用:

本文中的远程指的是通话录音，其中在另一端的人不知道正在进行录音。因此，如果该应用程序是手机上的默认拨号器，并且也是预加载的，则不需要辅助功能来访问传入的音频流，因此不会违反。由于这是对现有政策的澄清，新语言将从 5 月 11 日起适用于所有应用。”

简单来说，如果你的手机预装了通话录音功能，你没有什么可担心的——它会继续按预期工作。这一即将到来的变化将仅适用于 Play Store 上专门使用辅助功能 API 来启用通话记录的第三方应用程序。提供内置通话录音的谷歌手机应用不受这一变化的影响。

谷歌尚未澄清它打算如何实施这一即将到来的政策变化。目前还不清楚谷歌是否会在 5 月的最后期限后将不符合这一变化的第三方应用从 Play Store 中剔除。

* * *

来源: [Google Play 控制台](https://support.google.com/googleplay/android-developer/answer/11899428#accessibility_preview)， [Google Play 开发者政策更新](https://www.youtube.com/watch?v=d21mg8JxxU0&t=2990s)

Via: [Reddit](https://www.reddit.com/r/Android/comments/u81i7b/google_will_kill_call_recording_apps_once_and_for/)