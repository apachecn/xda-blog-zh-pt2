# 谷歌 Play 商店将不再显示更新应用的通知

> 原文：<https://www.xda-developers.com/the-google-play-store-will-no-longer-show-notifications-for-updated-apps/>

**更新 2 (06/29/2020 @美国东部时间上午 9:25):**谷歌 Play 商店的应用程序更新通知似乎正在返回。

**Update 1(02/28/2020 @ 01:54AM ET):**我们在新版本的谷歌 Play 商店中发现字符串，表明更新通知可能会返回。滚动到底部了解更多信息。下面保留了 2020 年 1 月 16 日发表的文章。

上个月末，我们遇到了谷歌 Play 商店的问题，它阻止了一些新发布的应用在搜索中出现。这个 bug 只在搜索新的应用程序时显示相关的搜索结果，尽管它们肯定是在平台上运行的。此后不久，谷歌解决了这个问题，用户再次能够在商店中查找新的应用程序。当时，一些用户还报告了 Play Store 上的另一个错误，即停止在通知阴影中显示应用程序更新通知。在 Play Store 版本 17.4 向用户推出后不久，[就注意到了这个漏洞，从那以后，越来越多的用户开始在 Reddit 和谷歌的](https://www.reddit.com/r/GooglePixel/comments/dywpf1/no_more_play_store_notifications/)[支持论坛](https://support.google.com/accounts/thread/7833555?hl=en)上分享这些问题。

现在，根据 Android Police 最近的一份报告，Google Play 商店中缺失的通知似乎是有意为之。谷歌发言人联系了该出版物，对该问题进行了进一步澄清，并透露缺失的更新通知是一个功能，而不是一个错误。尽管这个问题在去年 12 月早些时候被[短暂修复过，但在本月早些时候又重新出现了。截至目前，该公司还没有关于取消 Play Store 通知的进一步消息。希望查看应用更新状态的用户现在必须导航到 Play Store 中的我的应用&游戏部分，手动检查更新。请注意，谷歌不会在应用更新成功后推送通知。](https://www.reddit.com/r/GooglePixel/comments/e5pgvb/play_store_notifications_for_app_updatesapps_auto/)

**Via: [安卓警察](https://www.androidpolice.com/2020/01/14/play-store-notifications-no-longer-showing-up-for-updated-apps/)**

* * *

## 更新 1: Play Store 的应用更新通知可能会回来

应用程序更新时，谷歌 Play 商店不再显示任何通知。这一变化并没有得到很好的接受，因为很多人确实想知道他们手机上的哪些应用程序最近收到了更新。这可能是谷歌计划恢复通知的原因。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些特性目前还没有在实时构建中实现，并且可能会被开发人员在未来的构建中随时引入。

正如在谷歌 Play 商店 v19.0.12 中发现的，与应用程序更新通知相关的字符串已经被添加回来，这表明该功能可能会被恢复。

```
 <string name="updates_completed_notification_channel">Updates completed</string>
<string name="updates_completed_notification_channel_description">Notify when an app is finished updating</string> 
```

仅仅因为我们在新版应用中发现了这些字符串，这并不能保证该功能一定会回归。但是，这些字符串的存在是重新添加特性的先决条件。我们希望谷歌已经改变了主意。

*感谢 PNF 软件为我们提供了使用许可 [JEB Decompiler](https://www.pnfsoftware.com/?aid=xdadev) ，这是一款针对 Android 应用的专业级逆向工程工具。*

* * *

## 更新 2:回来了

谷歌似乎终于恢复了一个非常恼人的决定。在今年早些时候故意禁用 Play Store 的应用程序更新通知后，后来发现谷歌可能会恢复它们。这似乎正在发生，因为一些用户再次看到了通知和相关设置。像往常一样，推出似乎是服务器端的交换机，所以我们能做的就是等待。希望这不是一个简单的小测试，谷歌真的为每个人带来了他们。许多人求助于第三方应用来弥补功能的删除。

**来源:[推特](https://twitter.com/etonawa/status/1277286252585406469) | Via: [安卓警察](https://www.androidpolice.com/2020/06/29/google-appears-to-be-caving-in-and-bringing-back-play-store-app-update-notifications/)**