# 安卓奥利奥在电话中播放哔哔声通知

> 原文：<https://www.xda-developers.com/android-oreo-notification-phone-call/>

# 安卓奥利奥在打电话时会发出嘟嘟的通知声，让很多人很烦

多份报告披露了 Android Oreo 的一项新功能，当你在打电话时，它会在耳机扬声器中播放通知声音。

不是每个人都为下一版本的 Android 安装谷歌的开发者预览版。每一个通常都会带来一些变化，对于社区中的一些人来说，发现这些新特性是非常愉快的。一个这样的变化发生在第四代开发者预览版中，它允许当你在打电话时通过耳机扬声器播放通知声音。有些人希望这只是一个错误，会被删除，但看起来它已经进入了 Android Oreo 的第一版。

因为没有那么多人担心 Android 的一些功能会被破坏，所以没有那么多人知道它。但是自从第一次正式发布以来，[我们在](https://www.reddit.com/r/GooglePixel/comments/6veudi/dnd_while_on_phone_call_in_android_o/)[社区](https://www.reddit.com/r/GooglePixel/comments/6vfxwe/pixel_xl_oreo_incall_notifications/)看到了[对新功能](https://www.reddit.com/r/GooglePixel/comments/6vbz19/making_a_call_with_oreo_dnd_mode_vanished/)的多次抱怨。在第三代开发者预览版和早期版本的 Android 中，这种情况不会发生，因为当你正在打电话时，你的手机会自动进入勿扰模式。

现在情况不再是这样了，它已经被谷歌有目的地实现到软件**中。你可以[在这里](https://android.googlesource.com/platform/frameworks/base/+/android-8.0.0_r4/services/core/java/com/android/server/notification/NotificationManagerService.java#3870)找到它的提交，它在代码中被特别标记为“playInCallNotification”。这段代码在我们检查过的 Android 早期版本中并不存在，但是自从第四版开发者预览版发布以来，我们已经看到了相关的报道。我们中的许多人只是希望它被错误地实现，至少在设置或应用程序中有一个选项来禁用它。**

这不仅会让你在打电话的时候分心(如果是重要的电话，这就更成问题了)，而且当你在开电话会议并且开着免提的时候，这也很烦人。我们不确定谷歌对 Android Oreo 的想法是什么，但是让我们希望它被移除或者增加一个开关。