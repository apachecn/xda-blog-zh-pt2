# Keepass2Android Beta 更新了 Android Oreo 中的自动填充框架支持

> 原文：<https://www.xda-developers.com/keepass2android-beta-autofill-android-oreo/>

Android 上有许多流行的密码管理器，但只有少数几个脱颖而出。LastPass 就是其中之一，但它是闭源的——你自己看不到代码。对于担心这一前景的人来说，最好的选择之一是 Keepass2Android，[桌面 Keepass 的一个端口](https://www.xda-developers.com/host-your-own-cross-platform-password-manager-with-keepass/)。它允许用户从云存储服务中存储和访问他们的密码，并具有指纹数据库解锁功能。

不幸的是，无论你使用哪种密码管理器，Android 上的大多数密码管理器都不符合标准。这是因为直到 Android Oreo，谷歌才开始支持密码自动填充——在 Nougat 和更老的版本上，LastPass 和 Keepass2Android 这样的管理器必须使用 Android 的可访问性服务，这往往会引入轻微的延迟。

[我们写道，由于可访问性服务的本质，这种滞后是故意的](https://www.xda-developers.com/working-as-intended-an-exploration-into-androids-accessibility-lag/)。但是密码管理器加剧了这种影响，它使用可访问性服务来检测输入字段。

Android 8.0 Oreo 中添加的自动填充框架解决了这个问题，它允许需要数据输入的应用程序请求自动填充框架，自动填充框架调用自动填充服务并发送所述数据。

现在，一个更新了库、构建系统、目标 SDK 和支持 Android Oreo 中自动填充框架的新版本 Keepass2Android 可供测试人员使用。对于 Android Oreo 用户来说，这是个好消息——应用程序的体验应该会明显更好。

如果 AutoFill API 没有任何问题，Keepass2Android 用户可以期待它在不久的将来进入稳定渠道。

* * *

[**来源:Philipp Crocoll(在 Google+)**](https://plus.google.com/107656019972447589496/posts/GUvWibm5ySR)