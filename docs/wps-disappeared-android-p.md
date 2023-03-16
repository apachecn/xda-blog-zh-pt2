# Wi-Fi Easy Connect 是 Android Q 对 WPS 的替代

> 原文：<https://www.xda-developers.com/wps-disappeared-android-p/>

**更新 2(美国东部时间 6/9/19 @下午 3:08):**WPS 已经被弃用，但谷歌在 Android Q 中提供了一个替代方案，名为“Wi-Fi Easy Connect”。

**更新 1(美国东部时间 2018 年 7 月 17 日晚上 7 点 10 分)**:一名谷歌员工刚刚在问题跟踪器上发表评论，称[功能将在未来的 Android 版本中可用](https://issuetracker.google.com/issues/79404939#comment10)。

随着 Android P 的出现，我们都很高兴看到最终版本给我们带来了什么。我们可以期待看到性能的提升和新的功能，比如手势导航和新的用户界面。然而，我们也可以期待无数的安全增强，其中一些可能会激怒用户。正如 [*AndroidPolice*](https://www.androidpolice.com/2018/07/09/android-p-doesnt-support-wps-may-deprecated-google/) 最先报道的，看起来谷歌可能会在 Android P 发布时取消 WPS (Wi-Fi 保护设置)支持。对于那些不知道的人，WPS 允许你只需按下路由器上指定的按钮就可以将设备连接到路由器。一些配置要求您在设备上输入 PIN 码。

由于这种基于 PIN 的身份验证，WPS 本质上是不安全的，暴力攻击对它来说是常见的。WPA2 [可能会被破解](https://www.xda-developers.com/wpa2-wifi-protocol-vulnerability-krack/)，但如果你能破解 WPS pin，你甚至不需要使用那样的攻击。但是我们怎么知道在 Android P 中对它的支持被取消了呢？许多与协议相关的字符串已被标记为不推荐使用，没有实际记录的更改。一名谷歌员工回应说，已经通知了开发团队，但这并不意味着这不是故意的。试图访问 WPS 将返回一个一般性错误，这使得这看起来非常故意。

那么，对于那些在日常生活中可能需要 WPS 的人来说，接下来该怎么办呢？这是一个旧的安全标准，而且非常不安全。虽然它可能在家里有用，但它是一个不应该出现在商业环境中的协议。这也没什么大不了的，因为用户可以在智能手机上输入网络密码。可能不方便，但肯定不会阻止人们上网。你可以点击查看这个问题的[错误跟踪报告。如果谷歌有回应，我们会更新这篇文章。](https://issuetracker.google.com/issues/79404939)

* * *

## 更新 1:谷歌回应问题跟踪者

一名谷歌员工对 WPS 消失的问题跟踪报告做出回应，称“问题已经解决，将在未来的 Android 版本中可用。”我们不确定该功能是否会在最终的 P 版本或 Android Q 中回归。我们将努力澄清这一点，如果我们收到任何新信息，将更新本文。

* * *

## 更新 2:一个新的选择- Wi-Fi 轻松连接

虽然 WPS 被弃用，但 Android Q 引入了对 [Wi-Fi Easy Connect](https://www.wi-fi.org/discover-wi-fi/wi-fi-easy-connect) 的支持，以简化向网络添加新设备。根据[文档](https://developer.android.com/preview/features#wifi-easy)，应用程序可以通过使用 ACTION _ PROCESS _ WIFI _ Easy _ Connect _ URI 意图来集成 Easy Connect，这需要用户通过扫描二维码或发现蓝牙 LE 或 NFC 广告来提供 URI。轻松连接不需要位置或 Wi-Fi 权限。