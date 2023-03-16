# Cloverplay 为 Stadia 和 Microsoft xCloud 添加了触摸屏控制

> 原文：<https://www.xda-developers.com/cloverplay-touch-screen-controls-google-stadia-microsoft-xcloud/>

由于新冠肺炎，越来越多的人呆在家里，这是学习新技能、写简历、看最新节目或玩新游戏的最佳时机。如果你渴望在这段停机时间玩一些视频游戏，而你还没有游戏 PC 或最新的游戏机，那么你可能会对谷歌、微软和英伟达的云游戏流媒体产品感兴趣。对于那些使用[谷歌 Stadia](https://www.xda-developers.com/tag/google-stadia/) 或[微软 xCloud](https://www.xda-developers.com/tag/microsoftxcloud/) 的人来说，我们想把你们的注意力带到由 XDA 成员 [refi64](https://forum.xda-developers.com/member.php?u=5569318) 开发的一个很酷的新应用上。这款名为 Cloverplay 的应用程序带来了触摸屏控件，覆盖在 Stadia 和 xCloud 的 Android 应用程序之上。

正如你在下面的截图中看到的，Cloverplay 可以让你在 Android 手机上从 Stadia 或 xCloud 玩游戏，而不需要物理控制器。该应用程序提供了一组屏幕控制，模拟谷歌 Stadia 控制器(用于 Stadia)和 Xbox One S 控制器(用于 xCloud)的按钮按压和操纵杆输入。为了证明这一点，开发者发布了一些截图，显示了在*最终幻想 XV* (在谷歌 Stadia 上)和*完全精确战斗模拟器*(在微软 xCloud 上)中的触摸屏控制

我们之前报道过一个名为“ [TouchStadia](https://www.xda-developers.com/touchstadia-use-on-screen-controls-google-stadia-chrome-android/) 的工具，它也可以实现谷歌云游戏服务的触摸屏控制。虽然 TouchStadia 可以在没有 root 访问权限的情况下工作，但它只能在通过移动浏览器玩 Stadia 游戏时工作。相比之下，Cloverplay 可以与谷歌 Stadia 官方应用程序配合使用，也可以与微软 xCloud 配合使用。开发者将 Cloverplay 相对于 TouchStadia 的优缺点总结如下:

*   TouchStadia 与 Cloverplay 相比的优势:
    *   适用于任何设备。(你可以在 Android 上使用 Xtadia 让 Stadia 在未经批准的设备上运行，但这需要 Xposed 才能工作。)
    *   不需要 root 访问权限。
    *   如果您使用支持扩展的浏览器(例如 Yandex ),则可与 Stadia+结合使用。
    *   支持自定义控件布局。
*   Cloverplay 相比 TouchStadia 的优势:
    *   允许您使用官方应用程序(这往往会产生略好的性能 IME)。
    *   配合 xCloud 使用。
    *   非常易于使用(不需要复制脚本或定制扩展)。
    *   操纵杆是可见的，不会引起额外的延迟。
    *   支持体育场特定的助手和截图按钮。

这是开发人员演示 Cloverplay 的一段屏幕记录:

据开发人员称，Cloverplay 使用 root 访问权限，通过 uinput 设置虚拟操纵杆。至于辅助功能服务，应用程序似乎用它来创建一个覆盖图[TYPE _ Accessibility _ OVERLAY](https://developer.android.com/reference/android/view/WindowManager.LayoutParams#TYPE_ACCESSIBILITY_OVERLAY)。

该应用程序可在 XDA 实验室下载。主应用程序的价格为 1.99 美元，但有一个为期 2 天的试用版，你可以下载，看看它是否值得你这么做。开发者表示，他们最初没有选择将该应用提交给 Google Play，因为他们认为 Google [会因滥用辅助功能服务](https://www.xda-developers.com/google-threatening-removal-accessibility-services-play-store/)而删除该应用。然而，据我所知，谷歌还没有删除任何使用辅助功能服务的应用程序。在我们将此事告知开发者后，他们已将 app 提交至 Play Store 进行审核。

有关 Cloverplay 的更多信息，请访问以下链接的网站。如果你有反馈或想问问题，请查看该应用在 XDA 上的论坛帖子。你也可以在 GitHub 上查看该应用的源代码。

**[Cloverplay 网站](https://cloverplay.app/)** ||| **[XDA 论坛线程](https://forum.xda-developers.com/android/apps-games/alpha-cloverplay-screen-controls-stadia-t4083177)| | |[GitHub 上的源代码](https://github.com/refi64/cloverplay)**

[appbox xda com . refi 64 . clover play]

[appbox xda com . refi 64 . clover play . trial]