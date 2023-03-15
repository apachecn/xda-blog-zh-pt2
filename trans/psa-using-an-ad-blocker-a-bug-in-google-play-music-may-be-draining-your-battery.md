# PSA:使用广告拦截器？Google Play 音乐中的一个 Bug 可能会耗尽您的电池。

> 原文：<https://www.xda-developers.com/psa-using-an-ad-blocker-a-bug-in-google-play-music-may-be-draining-your-battery/>

我们中的许多人在我们的 Android 设备上使用广告拦截器，无论是为了减少带宽使用，避免跟踪还是简单地摆脱视觉干扰。广告拦截器的工作方式很简单:它们拦截所有对提供广告或允许分析和跟踪的已知域名的请求。

当网络请求失败时会发生什么？嗯，通常**不会**发生的是让应用程序永远重试请求，希望它最终会工作。这正是 Google Play 音乐应用程序中一个罕见的错误可能导致的，这可能会导致一些**严重的 CPU 使用和电池消耗**(以及你的设备发热)。这就是试图每秒发出大约 200 个网络请求的效果:

```

06-11 22:20:17.957 17958 18144 W GoogleTagManager: Exception sending hit: ConnectException
06-11 22:20:17.957 17958 18144 W GoogleTagManager: Connection refused
06-11 22:20:17.960 17958 18144 W GoogleTagManager: Exception sending hit: ConnectException
06-11 22:20:17.960 17958 18144 W GoogleTagManager: Connection refused
06-11 22:20:17.963 17958 18144 W GoogleTagManager: Exception sending hit: ConnectException
06-11 22:20:17.963 17958 18144 W GoogleTagManager: Connection refused
06-11 22:20:17.966 17958 18144 W GoogleTagManager: Exception sending hit: ConnectException
06-11 22:20:17.967 17958 18144 W GoogleTagManager: Connection refused
06-11 22:20:17.970 17958 18144 W GoogleTagManager: Exception sending hit: ConnectException
06-11 22:20:17.970 17958 18144 W GoogleTagManager: Connection refused
06-11 22:20:17.973 17958 18144 W GoogleTagManager: Exception sending hit: ConnectException
06-11 22:20:17.973 17958 18144 W GoogleTagManager: Connection refused
06-11 22:20:17.976 17958 18144 W GoogleTagManager: Exception sending hit: ConnectException
06-11 22:20:17.976 17958 18144 W GoogleTagManager: Connection refused
06-11 22:20:17.987 17958 18144 W GoogleTagManager: Exception sending hit: ConnectException
06-11 22:20:17.987 17958 18144 W GoogleTagManager: Connection refused

```

这个错误似乎是因为 Google Play Music 跟踪了各种用户发起的行为，如打开艺术家的页面或播放歌曲。如果你阻止了 googletagmanager.com(**AdAway 默认了；大多数要阻止的域名来源也包括它，因为它用于分析和跟踪**，你可能会受到这个 bug 的影响。要检查您是否是，请遵循以下步骤:

1.  强制停止 Google Play 音乐应用程序。
2.  打开 Google Play 音乐。
3.  搜索艺术家(如“里克·阿斯特利”)。
4.  轻按艺术家的缩略图以打开他们的页面。
5.  检查您的 logcat，看看它是否被垃圾邮件与上述行。

并非所有版本或用户都会受到这个错误的影响，但是我们能够在最新版本(7.8.4818-1)上重现它。R.4063206)在我们的一些设备上。据我们所知，这是一个相当模糊的错误,虽然我们不确定它的确切原因，但对受影响的用户来说，后果非常重要，不容忽视。缓解这个问题的一个解决方法(直到 Google Play 音乐团队注意到并修复它)是通过使用您的广告拦截器的“白名单”功能来停止拦截 googletagmanager.com。

Android 用户对看似无法追踪的电池耗尽、过热和随机变慢的原因并不陌生。能够追踪并消除根本原因总是好的，所以如果你是受影响的用户之一，我们希望这个指南对你有所帮助。如果您使用广告拦截器并经历随机流失，您现在也知道如何识别和解决可能的原因。

* * *

有过使用广告拦截器的类似经历吗？你多久遭受一次随机排水？请在评论中告诉我们。