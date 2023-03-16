# [更新:修复] PSA:最新的 Play Store 更新破坏了付费应用程序的许可证验证

> 原文：<https://www.xda-developers.com/latest-play-store-breaks-license-verification-paid-apps/>

# [更新:修复] PSA:最新的 Play Store 更新破坏了付费应用程序的许可证验证

最新版本的谷歌 Play 商店打破了许多付费应用的许可验证，看看这意味着什么。

2018 年 7 月 3 日更新:谷歌发布了一个更新，修复了这个问题。详情请见文末注释。

谷歌向开发者提供了许多工具来保护他们的应用程序，并确保盗版者不能轻易下载他们的应用程序的高级版本。其中一个工具是 LVL，即许可证库**验证库**库**。Play Store 上的许多应用程序都使用它，比如 Substratum 和我们自己的 [XDA 导航手势应用](https://www.xda-developers.com/navigation-gestures-update-app-launch-android-p/)。但有一个主要问题:在谷歌 Play 商店的最新版本 10.7.17 及以上版本中，对这个库的访问似乎被中断了。**这导致许多购买应用程序的人突然看到他们的应用程序告诉他们，他们的付费许可证不再有效。****

 <picture>![google play store](img/9cb2587f5f7adb6d3b49bbd685b6d3b0.png)</picture> 

One user faced this issue when launching Substratum // Source : XDA Junior Member [theninjew](https://forum.xda-developers.com/member.php?u=7503978)

XDA 承认开发者[flar 2](https://forum.xda-developers.com/member.php?u=4684315),[前内核管理器](https://play.google.com/store/apps/details?id=flar2.exkernelmanager)的开发者，证实这个 bug 已经影响了他个人的应用程序，他也报告说在他女儿的设备上看到了许多应用程序的 bug。他表示，付费的 Toca Boca 应用程序，如 [Toca Life: School](https://play.google.com/store/apps/details?id=com.tocaboca.tocaschool) 和 [Toca Life: City](https://play.google.com/store/apps/details?id=com.tocaboca.tocacity) 无法打开，因为它们陷入了空白屏幕和旋转进度条。flar2 确认降级到谷歌 Play 商店 v10.6.x 解决了该问题。另一个面临这个问题的开发者是 XDA 认可的开发者 arter97，Open GApps 团队[已经承认](https://github.com/opengapps/opengapps/issues/644)闪回早期版本可以修复这个问题。

然而，对于大多数应用程序来说，问题不会立即显现出来。EX Kernel Manager 会在首次启动时检查许可证，之后它和许多其他应用程序会在本地缓存许可证。这些应用程序的用户不会注意到任何问题，直到重新检查许可证，此时验证将失败。

现在谷歌问题跟踪器上有一个帖子[，尽管谷歌还没有回复。我们敦促用户不要评论它，因为它通知了链中的每个人。这是一个至关重要的 bug，需要谷歌尽快修复。我们已经联系了谷歌进行评论，如果有回音，我们会更新这篇文章。](https://issuetracker.google.com/issues/110978499)

## 更新 1:谷歌正在调查

一名谷歌员工回应了问题追踪报告，称他们正在调查问题。

## 更新 2:谷歌推出了一个补丁

谷歌[在这里](https://issuetracker.google.com/issues/110978499#comment48)证实，已经发布了一个更新来修复这个问题。你可以从[这里](https://www.apkmirror.com/apk/google-inc/google-play-store/google-play-store-10-7-19-release/google-play-store-10-7-19-all-0-pr-202990317-android-apk-download/)下载更新后的谷歌 Play 商店应用(版本 10.7.19)。