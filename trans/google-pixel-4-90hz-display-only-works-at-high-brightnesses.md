# 【更新 1:即将修复】谷歌 Pixel 4 的 90Hz 显示屏只能在高亮度下工作

> 原文：<https://www.xda-developers.com/google-pixel-4-90hz-display-only-works-at-high-brightnesses/>

**更新 1(美国东部时间 10/23/19 @下午 3:20):**谷歌表示，他们将为 Pixel 4 进行软件更新，以便在更多亮度条件下启用 90Hz。

谷歌 Pixel 4 和 Pixel 4 XL 于上周发布，这两款手机遭到了严重泄露，谷歌通过官方披露对这些泄露负有责任。我们并不期待花哨的功能，因为大多数功能已经公开——其中许多功能[谷歌甚至没有在 Pixel 4 的主题演讲](https://www.xda-developers.com/google-pixel-4-what-you-missed/)上谈论——但是，新款 Pixel 智能手机上更流畅的 90Hz 显示屏是我们许多人期待的关键功能之一。虽然手机源代码中的参考资料[在正式发布前至少一个月放弃了 90Hz 显示屏](https://www.xda-developers.com/google-pixel-4-90hz-display-android-10-source-code/)，但最近发现了一些有趣的东西。

**[像素 4 XDA 论坛](https://forum.xda-developers.com/pixel-4) / [像素 4 XL XDA 论坛](https://forum.xda-developers.com/pixel-4-xl)**

就像一加 7 Pro 和新的一加 7T 系列一样，90Hz 的刷新率并不适用于所有场景，只适用于特定的用例或支持的应用程序。显然，谷歌正在使用一种算法来智能地将 Pixel 4/4 XL 显示器的刷新率降低到 60Hz，例如当你观看视频或阅读静态内容时，当你滚动时，它会自动返回。

然而，Android 开发者[Brian Sefcik](https://www.linkedin.com/in/briansefcik/) 发现了这方面的一个奇特行为，并得到了我们主编[mishal Rahman](https://www.xda-developers.com/author/mishaalrahman/)的证实。他们确定 Pixel 4 的显示屏**会根据显示屏的亮度**自动在 90Hz 和 60Hz 刷新率之间切换。

通过 ADB 使用 Logcat 工具，Mishaal 确认了当亮度低于 75%时，Pixel 4 的显示屏会自动调低至 60Hz。目前还不清楚谷歌为什么将设置与亮度挂钩，我们希望很快找到确切的原因。有趣的是，只要有强烈的环境照明，即使亮度很低，像素也能以 90Hz 运行。

值得注意的是，无论是一加 7 Pro 还是 T2 华硕 ROG 手机 II T3 都没有表现出这种行为。这种行为很可能是故意的，而不是一个错误，但我们不确定这是否是谷歌试图避免投诉 Pixel 4/4 XL 上的平滑显示屏过快耗尽小电池。

### 在像素 4 上强制 90Hz 刷新率

同时，如果你有一个像素 4/4 XL，并希望总是享受 90Hz 的显示，你可以通过强制开发者设置中的选项来设置显示器永久保持在 90Hz。这将继续工作，无论你使用手机的亮度。

* * *

## 更新:软件更新即将到来

谷歌向 [*The Verge*](https://www.theverge.com/2019/10/23/20929090/google-pixel-4-screen-smooth-display-refresh-rate-lighting-conditions-software-update) 发布了一份关于 Pixel 4 上 90Hz 显示情况的声明。他们重申，在消费内容和导航 UI 时，显示器的设计频率为 90Hz，但为了节省电池，他们可以在某些情况下将其降低到 60Hz。

然而，在某些情况下，我们将刷新率设置为 60Hz。这些情况包括:当用户打开电池保护时，某些内容，如视频(因为它主要以 24 或 30fps 拍摄)，甚至各种亮度或环境条件。我们不断评估这些参数是否能带来最佳的整体用户体验。我们之前已经计划了将在未来几周推出的更新，包括在更高亮度的条件下启用 90hz。

我们不确定这个更新是否会给客户更多的控制，或者只是默认包含更好的变量。请继续关注此更新推出时的更多信息。我们也在等待更新，以使[睁眼设置](https://www.xda-developers.com/google-pixel-4-what-you-missed/)面部解锁。