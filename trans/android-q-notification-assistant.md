# Android Q 增加了新的通知助手 API 来管理通知

> 原文：<https://www.xda-developers.com/android-q-notification-assistant/>

**更新 1(美国东部时间 5/8/19 @ 00:52AM):**谷歌在谷歌 I/O 2019 发布的 Android Q beta 3 中移除了对 NotificationAssistant API 的公共访问。更多细节见下文。

在 Android 8.0 Oreo 之前，谷歌[就已经开发了](https://android.googlesource.com/platform/frameworks/base/+/android-8.0.0_r1/core/java/android/service/notification/NotificationAssistantService.java)新的通知助手 API。随着[第一个 Android Q beta](https://www.xda-developers.com/android-q-dp1-google-pixel-2-google-pixel-3/) 的发布，谷歌将 API 公之于众，[也为其发布了文档](https://developer.android.com/reference/android/service/notification/NotificationAssistantService.html)。在第二个 Android Q 测试版中，现在可以将默认的通知助手从 Android Services Library 系统应用程序更改为您选择的任何第三方应用程序。下面是对新 API 及其功能的初步介绍。

首先，如果你在 3 月份在谷歌 Pixel 上安装了 Android Q beta，你可能会短暂地看到智能回复和按钮出现在每个通知中。负责插入智能回复的应用程序是默认的通知助手，尽管谷歌很快通过服务器端更新禁用了通知助手的智能回复功能。我们重新激活了该特性，向您展示该 API 的能力，如下图所示。

正如你所看到的，通知助理为来自电报应用的消息添加了上下文按钮。它或者向我显示智能回复，或者在 URL 的情况下，显示在适当的应用程序中打开 URL 的链接。根据文档，通知助理可以在发布之前或之后调整优先级或向任何现有通知添加按钮。[与长期存在的通知监听器 API](https://www.xda-developers.com/add-mark-as-read-button-gmail/) 不同，通知助手在对通知进行调整时会保留现有的通知。如果通知支持内嵌回复，通知助手应用程序可以添加按钮来发送响应，这正是平台默认的通知助手所做的。由于 API 是通用的，通知助理可以向通知添加按钮，即使不是来自消息应用程序，也可以触发您想要的任何操作。

 <picture>![Notification Assistant in Android Q](img/35272302c3f9974135b87f74e3d95318.png)</picture> 

Changing the default Notification Assistant in Settings > Apps & notifications > Notifications > Notification Assistant. The Notification Assistant can also be programmatically changed by writing to Settings.Secure.enabled_notification_assistant.

Tasker 和 AutoApps 的开发者 joo Dias 正在更新他的 auto notification plugin for Tasker，可以让你对任何通知添加自定义的快速回复。这是他制作的一个视频，展示了支持通知助理 API 的新自动通知版本:

我可以看到这个 API 对自动化应用很有用，但我不认为很多人会改变默认的通知助手。一旦谷歌在默认的通知助手中启用上下文操作和智能回复，人们就没有理由使用第三方的通知助手了。不过，像 Tasker 这样的自动化应用程序的粉丝可能会发现 Android Q 中的这个新 API 很有用。

## 更新 API 的文档已经被删除

在 Google I/O 2019 上发布了[第三个 Android Q beta](https://www.xda-developers.com/android-q-beta-3-released/) 之后，Tasker 开发者联系我，通知我 Google 移除了 NotificationAssistant 功能的公共 API。检查 [API 差异](https://developer.android.com/sdk/api_diff/q-beta3-incr/changes/pkg_android.service.notification.html)证实了这一点。我们也和 I/O 的谷歌员工谈过，他们被告知这个 API 不是面向公众的。如果这个 API 的可用性有任何变化，我们将更新这篇文章。