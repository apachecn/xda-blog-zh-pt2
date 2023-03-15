# 为带有自动通知功能的 Gmail 通知添加“标记为已读”按钮

> 原文：<https://www.xda-developers.com/add-mark-as-read-button-gmail/>

虽然智能手机还没有完全取代台式机或笔记本电脑，但对许多人来说，它们已经成为执行某些操作的主要方法，如阅读和回复电子邮件。如果这就是你，并且你收到了很多邮件，你可能想找到更快的方法每天清理你的收件箱。Android 上的 Gmail 官方应用程序的用户多年来一直要求一个功能来做到这一点:Gmail 通知的“标记为已读”按钮。现在，你可以通过一个叫做 AutoNotification 的漂亮的第三方应用程序。

## Gmail 的标记为已读按钮

正如你在上面看到的，左边的原始 Gmail 通知显示了邮件内容，但只允许我存档(或删除，取决于你在 Gmail 应用程序中的设置)或回复邮件。在右侧，我们可以看到由 AutoNotification 创建的 Gmail 通知的克隆版，它具有所有相同的详细信息和按钮，但添加了一个额外的“标记为已读”按钮。

这个按钮做的正是你所期望的。它只是向 Gmail 发送一条“已读”消息，告诉它将这封邮件标记为已读。这是开发人员的视频演示:

这并不是第一个添加这一功能的应用程序。Play Store 上有一个老应用叫“ [MarkAsRead for Gmail](https://play.google.com/store/apps/details?id=com.samay.markasread2) ”基本上被放弃了，对我不起作用，只支持单一 Gmail 账户。另一方面，AutoNotification 由开发者不断更新，其标记为已读功能支持多个 Gmail 帐户。

我最初是在上个月给 Dias 先生发消息说要把这个功能添加到他的 AutoNotification 应用程序中，在过去一周左右的时间里，我一直在测试这个应用程序，没有出现任何问题。如果你和我一样，在不打开 Gmail 应用程序的情况下，没有一个按钮可以快速将新邮件标记为已读，那么试试最新的自动通知测试版。

### 如何下载

该功能可以在今天刚刚发布的**auto notification beta v 3 . 3 . 1 b**中找到。为了加入测试版，你必须在这里加入 [AutoApps Google+群](https://plus.google.com/communities/110193399489813640793)，才有资格在[注册这里列出的测试程序](https://play.google.com/apps/testing/com.joaomgcd.autonotification)。完成后，您可以从 Play Store 下载 AutoNotification。只要仔细检查它是 3.3.1b 版，否则它不会有 Gmail 标记为已读功能！

该功能需要在应用内购买**0.99 美元**才能在 7 天试用期后使用。如果你之前已经购买了 AutoNotification，比如试图在 Android Oreo 中[恢复通知重要性控件](https://www.xda-developers.com/notification-importance-controls-all-apps-android-oreo/)，那么你就不必在已经购买的完整许可之外再为这项功能付费。

### 它是如何工作的

实际上，该应用程序利用 Android 中的通知监听器服务来拦截来自所选谷歌账户的 Gmail 通知。该应用程序然后利用 [Gmail API](https://developers.google.com/gmail/api/) 根据原始电子邮件通知在您的通知上弹出的时间戳发送一封“已读”邮件，根据原始邮件的内容进行过滤，以便它有希望与正确的邮件相匹配。

这并不是 100%准确，因为在 Gmail 服务器记录您的邮件时间戳和它显示在您的通知上之间可能会有一些延迟，所以 AutoNotification 会发送一个它怀疑电子邮件已发送的时间范围。大多数情况下，这足以让它将正确的电子邮件标记为已读，但如果你的收件箱中充斥着相隔一分钟发送的连续电子邮件，则可能会出现这种情况。这就是该功能仍处于测试阶段的原因。