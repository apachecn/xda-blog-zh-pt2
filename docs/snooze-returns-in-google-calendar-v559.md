# 随着谷歌日历 v5.5.9 的发布，打盹提醒将最终回归

> 原文：<https://www.xda-developers.com/snooze-returns-in-google-calendar-v559/>

许多人使用并依赖谷歌日历来帮助组织他们的生活。然而，有许多事情我们想模糊地记录下来，但却不太适合在日历上标出。

每周提醒、目标或需要完成的次要任务最好与你的主日历分开处理，这就是为什么谷歌日历增加了[任务](https://support.google.com/calendar/answer/106237?hl=en)和[提醒](https://support.google.com/calendar/answer/6285327?co=GENIE.Platform%3DAndroid&hl=en)来适应更多的用例。谷歌日历提醒功能的粉丝可能会注意到，你过去可以暂停提醒通知。

不幸的是，由于某种原因，当谷歌日历升级到 5.0 版本时，[功能似乎已经消失了。我们不确定为什么当 Calendar 收到其完整的材料设计时，该功能不可用，但我们希望它最终会在未来的版本中回归。今天，谷歌日历 v5.5.9 正在推出，APK 文件的拆除强烈暗示了**提醒打盹功能**的回归。](https://www.reddit.com/r/androidapps/comments/2lhm9f/new_google_calendar_50_app_removed_the_snooze/)

*免责声明:我们从一个应用程序的 APK 文件中挖掘出的证据并不确定。谷歌可能会选择在未来的版本中不加任何提示地推出这些功能。*

* * *

嗯，我过会儿再做

在 APK 的文件中，我们发现了字符串和实际代码，它们将用于实现该功能(这意味着，它不仅仅是为未来的版本做准备，而是应该已经完全发挥作用)，这些都是以前版本的谷歌日历应用程序中没有的。下面的字符串清楚地指向了该功能的回归，但它似乎不会像谷歌日历 5.0 之前那样发挥作用

`<string name="task_snooze_failed_message">Failed to snooze the reminder</string>`

<string name="task_snooze_label">打盹</string>

<string name="task_snooze_message" formatted="false">提醒因 <g example="Today">%s</g> 、 <g example="11:20am">%s</g> 、T5 而暂停</string>

<string name="task_snooze_next_week">下周</string>

<string name="task_snooze_short">10 分钟后</string>

本周晚些时候

<string name="task_snooze_title">小睡至……</string>

<string name="task_snooze_today">今天晚些时候</string>

<string name="task_snooze_tomorrow">明天</string>

<string name="task_snooze_weekend">这个周末</string>

事实上，如果您注意到这些字符串中有迹象表明您将能够选择多次，直到通知将被暂停。以前，您只能在 15 分钟的默认时间内暂停通知(不幸的是，这是不可调整的)。该功能不仅会有回报，而且我们相信它会得到改进。

此外，我们之所以相信这个特性会很快出现，是因为在反编译的 APK 中存在一些类和方法，比如 **SnoozeActivity.smali** ，尤其是**snoozefindtimeasynctask . smali**，它们都直接表明了手动选择暂停通知的时间的能力。

然而不幸的是，日历中的返回暂停功能似乎没有谷歌收件箱中的[暂停功能强大，该功能允许你选择一个](https://gmail.googleblog.com/2015/01/snooze-in-inbox-because-not-everything.html)[特定位置](https://support.google.com/inbox/answer/6067583?hl=en)，直到提醒被暂停。然而，对于那些仍然喜欢使用 Gmail +谷歌日历而不是谷歌收件箱的人来说，这个更新绝对是受欢迎的。

* * *

*谷歌日历 v5.5.9 可以在 [APKMirror](http://www.apkmirror.com/apk/google-inc/calendar/calendar-5-5-9-125657303-release-release/) 下载。*