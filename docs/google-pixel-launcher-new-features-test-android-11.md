# 谷歌在 Android 11 中测试新的 Pixel Launcher 功能

> 原文：<https://www.xda-developers.com/google-pixel-launcher-new-features-test-android-11/>

谷歌的 Pixel Launcher 可能没有 Lawnchair、Nova Launcher 或 Action Launcher 等第三方替代产品的功能多，但它的简单和干净的设计为它赢得了许多粉丝。该启动器预装在谷歌 Pixel 设备上，很少接收更新。当谷歌发布新的 Pixel 设备或主要的 Android 更新时，我们通常会看到新的功能出现在启动器中，但[第一个 Android 11 开发者预览版](https://www.xda-developers.com/android-11-developer-preview-1-google-pixel/)并没有带来任何新的 Pixel 启动器功能。然而，我们知道自从我们发现了一个[新的“热门”功能](https://www.xda-developers.com/pixel-launcher-android-11-hints-showing-suggested-apps-home-screen-dock/)的迹象后，谷歌一直在研究这个发射器。现在，XDA 的高级成员 paphonb，Lawnchair 团队的开发人员之一，也是一位经验丰富的 Pixel Launcher 建模师，发现了其他几个可能会加入谷歌 Launcher 应用程序的新功能。

Paphonb 修改了 Android 11 开发者预览版的最新 Pixel Launcher build，以便推出几个正在开发的功能。这些功能包括最近应用概述中的新操作，在应用抽屉中隐藏单个应用建议的能力，以及新创建文件夹的自动命名。

**最近应用概述中的新动作**

在 Android 9 Pie 中，谷歌将最近应用处理程序的代码从 SystemUI 移到了股票 AOSP 启动器 [Launcher3](https://android.googlesource.com/platform/packages/apps/Launcher3/) 。在这个过程中，谷歌还推出了水平滚动的更高质量的最新应用概述卡，允许用户从概述卡中选择文本和图像的服务(仅限 Pixel 设备)，以及在概述卡下显示一行建议应用的服务。

现在在 Android 11 中，谷歌正在测试用一组 3 个动作取代最近应用概述中的应用建议行。这些操作包括“选择”、“截图”和“共享”“选择”按钮对 paphonb 不起作用，但我们可以猜测它的作用。它可能会突出显示概览卡中可以选择的所有文本和图像。至于其他两个按钮，屏幕截图按钮捕捉应用程序的焦点图像，而分享按钮捕捉屏幕截图，然后打开分享菜单，这样你就可以快速分享它。

 <picture>![Pixel Launcher recent apps overview test in Android 11 DP1](img/594cfba4170af4fa89881fcc9efc9c98.png)</picture> 

Screenshot by paphonb

**隐藏个人应用建议**

谷歌的应用推荐是基于你最近最常打开的应用。虽然可以通过进入 Pixel Launcher 设置中的建议子菜单来完全隐藏这一行，但不可能阻止某些应用程序显示在这一行中。然而，这种情况可能很快就会改变。Paphonb 分享了一个截图，显示了一个新的“不建议应用程序”动作，当长按建议应用程序行中任何应用程序的图标时。这个动作目前不起作用，但是很明显它会做什么。

 <picture>![Pixel Launcher in Android 11 Hide App Suggestions](img/9a79810cfa5a71aa44950c7cc2d1747c.png)</picture> 

Screenshot by paphonb

**自动命名文件夹**

Pixel Launcher 可能很快就能够自动为新创建的文件夹提供名称，这些文件夹是通过将一个应用程序图标拖放到另一个图标上而创建的。目前，你可以通过点击文件夹底部的“未命名”文本来手动命名文件夹，但谷歌可能会通过检测你正在分组的应用类型来节省你的精力。例如，在下面的视频中，paphonb 演示了当他将邮件和 Gmail 分组在一起时，Pixel Launcher 自动将一个新创建的文件夹命名为“Communication”。他还展示了当他把 Telegram 和脸书放在一起时，把一个新创建的文件夹命名为“Social”。

我们不知道 Pixel Launcher 是如何确定用户将哪种应用程序分组在一起的，但很可能谷歌正在使用 Play Store 上最受欢迎的应用程序的名称和类型的长列表。

在最新的 Pixel Launcher 版本中，用户还无法使用这些功能，谷歌可能永远不会发布它们。不过，你可以期待谷歌 launcher 的修改版会有类似的功能。如果谷歌决定在未来的更新中启用这些功能，我们会让你知道。您可以通过以下链接关注我们关于 Android 11 版本的最新帖子:

**[安卓 11 XDA 新闻](https://www.xda-developers.com/tag/android-11/)**