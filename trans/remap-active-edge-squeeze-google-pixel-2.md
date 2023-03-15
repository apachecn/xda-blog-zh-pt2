# 如何在谷歌 Pixel 2 上重新映射活动边缘/挤压

> 原文：<https://www.xda-developers.com/remap-active-edge-squeeze-google-pixel-2/>

自从谷歌 Pixel 2 和谷歌 Pixel 2 XL T1 智能手机发布以来，我们一直在寻找超越谷歌限制的定制手机功能的方法。我们开始研究的第一个功能是[的 Active Edge](https://www.xda-developers.com/source-pixel-xl-2-will-have-ambient-display-always-on-squeezing-while-screen-off-multiple-display-profiles-and-more/) ，这是谷歌对 [HTC U11 的可挤压框架功能](https://www.xda-developers.com/new-edge-sense-beta-u11-customization/)的继承。默认情况下，Active Edge 只允许你挤压手机来启动谷歌助手或静音来电，我们发现[不会是一个干净的解决方案](https://www.xda-developers.com/google-pixel-2-squeeze-hardcoded-assistant-remapping-difficult/)来重新映射 Active Edge 做任何你想做的事情。正如预测的那样，在谷歌 Pixel 2 上重新映射挤压功能的工作方法已经找到了。

谷歌硬编码 SystemUI，只允许当前助手应用设置为谷歌助手时 squeeze 工作。这意味着开发者将不得不使用辅助服务和读取系统日志的组合来检测用户何时挤压他们的手机，以便他们可以隐藏谷歌助手，而不是执行用户定义的操作。这正是 XDA 知名开发者 [flar2](https://forum.xda-developers.com/member.php?u=4684315) 对按钮映射器的最新更新所做的。

我们过去已经介绍过[按钮映射器](https://www.xda-developers.com/xda-spotlight-button-mapper-an-app-to-remap-your-phones-hardware-buttons/)应用程序，但是对于那些不熟悉的人来说，这个应用程序可以让你重新映射设备上的几乎任何按键，以执行你想要的任何操作。这样描述有点过于简单，因为这款应用还有很多其他功能，你绝对应该去看看。

无论如何，0.53 版本的最新更新带来了在谷歌 Pixel 2 和 Pixel 2 XL 上**重新映射挤压功能的能力。这个特别的功能将在**免费**中提供，尽管记住应用程序中的其他一些功能需要付费许可。**

上面的视频演示是 flar2 提供给我们的，所以他跳过了一些设置步骤，只是为了展示新功能。如果你想在你全新的谷歌 Pixel 2 或 Pixel 2 XL 上复制这一点，我们将在下面为你提供一个教程。

* * *

## 如何在谷歌 Pixel 2 上重新映射挤压/活动边缘功能

你需要做的第一件事是从 XDA 实验室或谷歌 Play 商店下载按钮映射器。

[appbox xda flar 2 . home 按钮]

请注意，您正在下载的版本是**版本 0.53** ，因为旧版本没有重新映射活动边缘的功能。接下来，确保**激活边缘在你的手机上被激活**。一旦你确认了这两件事，请遵循以下步骤:

1.  打开按钮映射器应用程序。通读设置页面，因为它们解释了按钮映射器能做什么和不能做什么。
2.  在底部，您应该会看到一个小工具栏(称为 snackbar ),它要求您启用按钮映射器的辅助功能服务。轻触 **Go** ，将带您进入按钮映射器的辅助功能服务页面。
3.  启用按钮映射器的**辅助功能服务**。
4.  你应该会自动返回到按钮映射应用程序。在**按钮**标题下，您会看到一个**活动边缘**的选项。选择它。
5.  轻触**自定义**。
6.  该应用程序会要求你将手机连接到电脑上并运行一个脚本。为了做到这一点，我们需要设置 Android 调试桥。
7.  如果您还没有，请进入“设置”->“系统”->“关于手机”,然后点击“**内部版本号**”7 次。您将看到一个弹出窗口，告诉您现在是开发人员。
8.  返回到设置->系统中，现在应该有一个**开发者选项**类别。输入这个，它可能会要求您输入 pin/密码。
9.  向下滚动，找到 **USB 调试**。启用它。
10.  按照上一个教程中的步骤在您特定的计算机操作系统上设置 ADB (您可以跳过“电话设置”部分，因为您已经启用了 USB 调试)。
11.  打开一个**命令提示符或终端**(取决于你的操作系统)并输入以下命令:`adb shell sh /data/data/flar2.homebutton/keyevent.sh`
12.  这将运行一个简短的脚本，该脚本将授予按钮映射器应用程序[Android . permission . read _ LOGS](https://developer.android.com/reference/android/Manifest.permission.html#READ_LOGS)。它需要这个权限来读取系统日志，我们将在下面详细解释原因。您只需授予此权限一次，除非您卸载应用程序或重置手机出厂设置。
13.  按钮映射器将要求您**重启应用程序**。点击按钮，让它重新启动应用程序。
14.  回到应用程序后，再次点击按钮标题下的“Active Edge”。您现在可以选择自定义并选择您想要的操作！恭喜，**你现在已经重新映射了谷歌 Pixel 2 挤压功能**！

* * *

## 说明

好吧，这里有点免责声明。这不是真正的重新映射 Active Edge，但希望它如此之快，以至于你不会注意到挤压手机时谷歌助手会弹出来。按钮映射器正在做的是使用辅助功能服务来检测谷歌助手何时将要弹出，然后它读取系统日志，同时过滤名为“ElmyraService”的东西。

我们在上一篇文章中讨论了 ElmyraService 如何表示活动的 Edge 服务，因此通过过滤系统日志中与之相关的行，Button Mapper 可以准确地知道您何时挤压手机。正如我所说的，这无论如何都不是一个完美的解决方案，因为这是一个相当粗糙的方法，涉及到授予敏感权限(READ_LOGS)，由于可访问性服务的[性质，可能会导致一些速度变慢，甚至可以由 Google 在未来的更新中进行修补(他们所要做的就是不写日志)。](https://www.xda-developers.com/working-as-intended-an-exploration-into-androids-accessibility-lag/)

Flar2 说，他在过去的一天里一直在使用它，它对他很有效。目前唯一的问题是避免谷歌助手在你挤压时弹出，为了实现这一点，他迫使设备在启动用户定义的动作之前进入主屏幕。他在按钮映射器中添加了一个实验选项，可以停留在当前应用程序中，而不会将你踢回主屏幕，但他说这还不是 100%一致。

尽管如此，这仍然是控制谷歌 Pixel 2 或谷歌 Pixel 2 XL 上可挤压框架的最佳(目前也是唯一)解决方案。通过按钮映射器，您可以让 Active Edge 执行打开相机、手电筒、网络浏览器等操作。可能性是无穷无尽的，选择什么完全看个人喜好。