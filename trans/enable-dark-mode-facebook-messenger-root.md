# 现在如何在 Facebook Messenger 中启用黑暗模式[Root]

> 原文：<https://www.xda-developers.com/enable-dark-mode-facebook-messenger-root/>

# 现在如何在 Facebook Messenger 中启用黑暗模式[Root]

如果你不能等待官方发布，并希望在脸书的信使启用黑暗模式，我们有一些好消息给你。

Facebook Messenger 的重新设计已经进行了很长时间。正式推出([这次是真的](https://www.xda-developers.com/facebook-shows-off-simpler-messenger-redesign-with-dark-mode/))仅仅在几天前开始，用户的意见非常不同。我个人喜欢新的界面，但这只是我的看法。如果你记得的话，几个月前脸书[也展示了一个黑暗模式](https://www.xda-developers.com/facebook-messenger-redesign-dark-mode/)。不幸的是，黑暗模式还不是最终版本，所以它没有被重新设计。好消息是我们已经找到了一种非正式的方法。

显然，该应用程序的最新测试版包括黑暗模式，但它还没有启用。我们电报组的用户 ***@VincentJoshuaET*** 找到了用 root 启用的方法。事不宜迟，让我们开始吧。请记住，您应该已经有了 Magisk(或任何其他的根解决方案),以便遵循下面概述的步骤。

1.  首先，前往 APKMirror 的这个链接，下载并安装 Facebook Messenger 的最新测试版
2.  在确保您已经安装了最新的 Messenger 测试版之后，您需要为您的设备下载一个终端应用程序。我推荐使用 [Termux](https://play.google.com/store/apps/details?id=com.termux)
3.  打开 Termux 并键入 *su* 然后按回车键。它应该要求超级用户权限，你应该授予
4.  现在你是超级用户了，输入*am start-n " com . Facebook . orca/com . Facebook . ab test . gkprefs . gksettingslisteactivity "*并按回车键。应该会出现下面的屏幕
5.  点击“搜索看门人”并输入“黑暗”。应该会出现一些结果。点击每一个说“不”的选项来启用它们。当你完成时，所有的结果都应该说“是”
6.  现在关闭应用程序和终端，打开 Facebook Messenger。点击左上角的个人资料图片。向下滚动一点，你应该会看到一个选项来激活黑暗模式。如果看不到该选项，您可能需要强制关闭该应用几次。

按照说明操作后，我能够在第一次尝试时启用黑暗模式，但您的里程数可能会有所不同。如果你不想下载 APK，你也可以通过 Play Store 列表注册 Messenger beta 程序，但是我不能这么做。我们希望 Facebook Messenger 的黑暗模式在未来几周内正式推出。