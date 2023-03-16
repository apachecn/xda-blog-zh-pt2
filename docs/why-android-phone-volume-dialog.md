# Android 的音量对话框是否需要太长时间才能消失？原因如下。

> 原文：<https://www.xda-developers.com/why-android-phone-volume-dialog/>

你有没有注意到当你按下音量按钮时出现的音量对话框过了一会儿才自动消失？当你第一次使用 Android 手机时，音量对话框会在几秒钟后自动消失，无需你的干预。然后，在过去几天、几周或几个月的某个时候，除非你轻击屏幕，否则需要很长时间才能消失。如果你正在经历这个问题，并且它激怒了你，你并不孤单。

在这篇文章中，我们将解释发生了什么以及为什么会发生，这样你可以自己解决问题，或者把这篇文章发给开发人员，让他们来解决问题。让我们首先确切地描述一下问题是什么，这样很清楚我们指的是您所面临的相同问题。

## 问题是

你按下 Android 智能手机或平板电脑上的音量按钮来改变音量，但出现的音量对话框需要很长时间才能自行消失，除非你点击屏幕让它消失。音量对话框自己能保持多长时间？整整 20 秒。

*学分:/u/ [糖果](https://www.reddit.com/user/ConeCandy)*

Reddit 的/r/[Google pixel](https://www.reddit.com/r/GooglePixel/comments/97pdac/why_does_android_pies_volume_pop_up_need_to_stay/)subred dit 上的一个流行帖子让许多用户插话说他们正面临这个问题。然而，并不是每个人都有这个问题。一些用户表示，他们的音量对话框只在屏幕上停留了 3 秒钟，这是正常现象。那么是什么导致了这个问题呢？对于该线程中的大多数用户来说，原因是一个名为 Signal Spy 的应用程序——尽管该线程中的一些用户说其他应用程序也导致了这种行为。

信号间谍是一个很受谷歌项目无线服务用户欢迎的应用。Project Fi 用户喜欢这个应用程序，因为它支持分析您当前的网络连接，并支持 Sprint 和 T-Mobile 之间的自动切换。最棒的部分？它不需要根访问权限就可以在网络之间切换。Signal Spy 使用无障碍服务(该服务使用 Android 的无障碍 API，通常用于帮助残疾用户，但也用于数百种常规应用)通过输入拨号器代码快捷方式在运营商之间自动切换。

Signal Spy 在 Project Fi 上自动切换运营商的能力非常有用，但这也是 Android 音量对话问题发生的原因。Signal Spy 与其他应用程序(如 LastPass、指纹手势、Zoho Vault、亚马逊助手和其他导致此问题发生的应用程序)之间的一个共同点是，它们**使用辅助服务**。进入设置- >辅助功能，逐个关闭每个辅助功能服务，是解决这个问题的一种方法。那么，为什么只有一些应用程序的可访问性服务会导致这个问题的发生呢？例如， [Tasker](https://play.google.com/store/apps/details?id=net.dinglisch.android.taskerm) 就没有面临这个问题，我们自己的[导航手势](https://play.google.com/store/apps/details?id=com.xda.nobar)应用也没有。你和其他许多使用[谷歌问题跟踪器](https://issuetracker.google.com/issues/37081594)的人可能会认为这是一个 bug，但实际上不是- **这完全是设计好的**。

## 解释

正如我们在开发导航手势应用程序时发现的那样，当辅助功能服务将[accessibilityFeedbackType](https://developer.android.com/reference/android/accessibilityservice/AccessibilityServiceInfo.html#feedbackType)设置为**而不是 FEEDBACK_GENERIC** 时，问题就出现了。当我们设置辅助功能服务使用 FEEDBACK_HAPTIC 时，音量对话框会在屏幕上停留 20 秒。当我们将其设置为 FEEDBACK_GENERIC 时，音量对话框会在屏幕上停留 3 秒钟。

出现这种情况的原因是因为 AOSP 的[音量对话框实现](https://android.googlesource.com/platform/frameworks/base/+/master/packages/SystemUI/src/com/android/systemui/volume/VolumeDialogImpl.java)中的两个方法。名为 computeFeedbackEnabled 的第一个方法检查是否有任何“非通用”的可访问性服务。如果为真，则将布尔型 mFeedbackEnabled 设置为真。在第二种方法 computeTimeoutH 中，如果 mFeedbackEnabled 返回 true，则卷对话框的超时设置为 20 秒，否则设置为 3 秒。

[这些](https://android.googlesource.com/platform/frameworks/base/+/5adeabc61d41f89af7f9e01e9f07136618547b9b) [方法](https://android.googlesource.com/platform/frameworks/base/+/f09838be846f59483f36dc3d96f13064362ea37e)是在 Android 6.0 棉花糖版本中添加的，因此这个音量对话框问题会影响自 Android 棉花糖以来的所有 Android 版本，包括 Android 牛轧糖、Android 奥利奥和 Android Pie。我们不完全确定*为什么添加这些方法，因为提交描述不清楚。如果我不得不冒险猜测为什么会有这种行为，我会说这是为了帮助有某些残疾的用户处理语音或其他输入的音量对话框，因为默认的 3 秒超时对他们来说太短了。如果 Android 检测到用户正在使用某种类型的辅助服务，它会自动延长音量对话框的停留时间，这样用户就有更好的机会与之交互。无论如何，很明显，这个问题**不是 bug** ，而是完全由设计**造成的**。不幸的是，这意味着除了说服谷歌改变这一决定或说服应用程序开发人员不要在他们的可访问性服务中使用非通用反馈类型之外，这个问题没有“解决方案”。*

Signal Spy 的开发人员已经确认他们已经在下一个测试版中解决了这个问题，所以如果你遇到了这个问题并想知道是否已经解决，你应该让应用程序开发人员参考这篇文章，这样他们就会意识到这个问题(因为许多人并没有意识到)。)如果 Android 的未来版本改变了这种行为，我们会让你们都知道。至少你现在意识到了这个问题以及导致这个问题的原因，所以你可以找出是哪些应用程序导致了你的这个问题。