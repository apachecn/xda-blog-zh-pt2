# Android 4.4.2 KOT49H 中的源代码提交揭示 Flash SMS 攻击修复和应用程序操作移除

> 原文：<https://www.xda-developers.com/source-code-commits-in-android-4-4-2-kot49h-reveal-flash-sms-attack-fix-and-app-ops-removal/>

就在几个小时前，我们讨论了 Android 4.4.2 的[源代码是如何进入 AOSP](http://www.xda-developers.com/android/android-4-4-2-kot49h-source-code-released-factory-images-for-nexus-4-5-7-and-10/ "Android 4.4.2 KOT49H Source Code Released, Factory Images for Nexus 4, 5, 7, and 10") 的。现在，FunkyAndroid 的优秀人员[再次](http://www.xda-developers.com/android/browse-every-new-aosp-code-commit-in-android-4-4-1/ "Browse Every New AOSP Code Commit in Android 4.4.1")创建了一个详尽的变更日志，详细记录了 4.4.1 和 4.4.2 之间的所有提交。

从 4.4.1 升级到 4.4.2 的 Nexus 设备所有者将证明增量 OTA 的规模很小。因此，只有四个源代码提交区分了这两个版本。但是不要害怕，因为这些变化实际上是重大的。如果你还没有更新，他们肯定会占用你几分钟的时间。

在这些修复中，4.4.2 带来了一个解决之前覆盖的低风险 Flash SMS 漏洞的解决方案。尽管他们开始用错误的方式[“修复”问题](http://www.xda-developers.com/android/google-pulls-hushsms-after-flash-sms-dos-info/ "Google Pulls HushSMS after Flash SMS DoS Info")，我们还是很高兴看到一个合理的解决方案出现。还有一个修复 OOBE 拒绝服务崩溃后，收到 0 字节的 WAP 服务信息，以及减少摄像头记录。

除了修复之外，我们[不久前报道的备受喜爱的 App Ops 程序](http://www.xda-developers.com/android/app-ops-brings-granular-permissions-control-to-android-4-3/ "App Ops Brings Granular Permissions Control to Android 4.3")被进一步隐藏了。因此，无法再通过以前的方式访问它。这种改变完全是有意的，因为谷歌总是打算保留程序进行内部调试。[正如谷歌框架工程师](https://plus.google.com/+DannyHolyoake/posts/FkfBxA5i3iG) [Dianne Hackborn](https://plus.google.com/105051985738280261832/posts) 所说:

> 这个用户界面(应该很清楚)不是最终用户界面。它是为了开发目的而存在的。它本不打算公开的。该架构用于越来越多的事情，但它不打算作为一个大的低级 UI，由一大堆无差别的旋钮组成，您可以旋转。例如，它现在用于每个应用程序的通知控制，用于在新的位置 UI 中跟踪何时访问位置，用于新的当前 SMS 应用程序控制的某些方面，等等。

要开始，请访问[FunkyAndroid kot 49e Changelog](https://funkyandroid.com/aosp-KOT49E-KOT49H.html)并检查这些提交。完整的(和微小的)变更日志可以在这篇文章的底部找到。你对 4.4.2 的更新有什么想法？谷歌最终修复了短信和 OOBE 崩溃的错误，你高兴吗？尽管 Dianne 做了解释，但你是否仍然对 App Ops 的进一步隐藏感到有点恼火？请在下面的评论中告诉我们。

*【来源[FunkyAndroid](https://funkyandroid.com/aosp-KOT49E-KOT49H.html)| Via Android police】*

FunkyAndroid 报道的完整变更日志:

> [986567d](https://android.googlesource.com/platform/build/+/986567d)  : "KOT49H"
> 
> [d470407](https://android.googlesource.com/platform/build/+/d470407)  : "KOT49G"
> 
> [5de4753](https://android.googlesource.com/platform/build/+/5de4753) : .1 变为. 2
> 
> [a7e544d](https://android.googlesource.com/platform/build/+/a7e544d)  : KOT49F
> 
> 接收到 0 字节 WAP 推送后修复 OOBE 崩溃/DoS。
> 
> [3574026](https://android.googlesource.com/platform/packages/apps/Camera2/+/3574026) :减少展平偏好设置的日志记录
> 
> [d00f7cd](https://android.googlesource.com/platform/packages/apps/Mms/+/d00f7cd) :使用 0 类短信的 Android 拒绝服务攻击
> 
> [37f06a4](https://android.googlesource.com/platform/packages/apps/Settings/+/37f06a4) :将片段放入特定活动的白名单