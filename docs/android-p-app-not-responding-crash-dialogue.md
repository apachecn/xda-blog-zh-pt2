# Android P 现在会崩溃应用程序，而不是在它们没有响应时告诉你

> 原文：<https://www.xda-developers.com/android-p-app-not-responding-crash-dialogue/>

# Android P 现在会崩溃应用程序，而不是在它们没有响应时告诉你

Android P 现在会崩溃应用程序，而不是告诉你它们没有响应(这就是所谓的应用程序没有响应或 ANR 对话)。这是一种针对开发质量差的应用的策略，可能会奏效。

在 Android P 的所有[新增加的](https://www.xda-developers.com/everything-new-android-p-developer-preview-2/)中，包括[新导航手势](https://www.xda-developers.com/android-p-iphone-x-gestures-official/)、[切片](https://www.xda-developers.com/slices-app-actions-android-p-google-assistant/) API 和[新生物识别 API](https://www.xda-developers.com/android-p-new-biometrics-api/) ，还有一些其他的变化也可能以更微妙的方式产生影响。其中之一是取消了前台应用程序的 ANR 对话框。当有东西阻止主 UI 线程响应时，就会出现 ANR 对话框。当 Android Oreo 或更低版本出现这种情况时，ANR 对话会显示给用户，让他们知道。现在，在 Android P 中，应用程序会在没有任何用户通知的情况下崩溃。

为什么不告诉用户实际发生了什么就让应用程序崩溃呢？这对用户来说不一定是一种好处，但它迫使开发人员特别注意某些问题，并确保问题得以避免。我们鼓励开发人员不要在前台线程中运行任何东西。在下面链接的源视频中，谷歌讨论了避免这个问题的潜在解决方案，包括 [AsyncTask API](https://developer.android.com/reference/android/os/AsyncTask) 。Android 最近对后台服务的限制意味着过渡到服务可能不是一个好主意。如果你有兴趣了解更多解决这个问题的方法，我们建议你听听下面的演讲:

谷歌的做法有道理，但是否过分了？这可能会给人一种 Android 应用崩溃频率降低的感觉，但如果用户看不到通知，那么开发者就必须关注他们的崩溃工具，如 Firebase 崩溃报告，而不是直接的用户反馈。如果您是最新 P beta 版本的开发人员，您可以通过启用开发人员选项中的设置来恢复这些崩溃对话。

这并不是 Android P 中关于应用程序在后台的可见性的唯一变化。Android Oreo 引入了持续通知，当[某些应用在后台运行](https://www.xda-developers.com/hide-app-running-background-notification-android-oreo/)时，如果该应用没有足够高优先级的通知，但 Android P 现在完全摆脱了该通知。唯一的区别是 ANR 对话框没有放置一个持久通知那么烦人。

* * *

[**Via:/r/AndroidDev**](https://www.reddit.com/r/androiddev/comments/8ix4p7/beware_android_p_will_crash_your_app_on_anr_app)