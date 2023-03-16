# 谷歌 Play 商店准备增加应用内评论

> 原文：<https://www.xda-developers.com/google-play-store-in-app-review/>

如果你在社交媒体上关注任何知名的独立 Android 应用开发者，你可能会看到他们至少有一次抱怨过 Play Store 的评级。不过，这是可以理解的，因为评级，虽然[有时完全没有意义](https://twitter.com/franciscof_1990/status/1148376562775023616)，可以成就或摧毁一个应用程序的成功。在 Google Play 中，对产品有问题的用户比对产品没有问题的用户更有可能留下(负面)评论，这对于许多有评级系统的在线市场来说都是如此。为了解决这个问题，许多开发商鼓励客户如果对产品满意，就离开 Play Store 评论。目前，用户在 Google Play 上给应用评级的唯一方法是导航到 Play Store 列表，但谷歌可能正在开发一种让用户通过应用内对话框给应用评级的方法。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些功能目前还没有在 live build 中实现，可能会在未来的版本中随时被 Google 拉出来。

## 谷歌 Play 商店新增应用内审核代码

Play Store 应用程序的 15.9.21 版本于本周开始推出，并由 OpenGApps 的开发者上传至 [APKMirror](https://www.apkmirror.com/apk/google-inc/google-play-store/google-play-store-15-9-21-release/) 。我们解码了这个 APK，发现了一个名为“`com.google.android.finsky.inappreviewdialog.InAppReviewActivity`”的新活动从名称判断，这似乎是一个允许用户在不离开应用程序的情况下对应用程序进行评级的对话框。目前，启动活动会在底部弹出一个简单的“提交”按钮，点击它不会做任何事情。

这是因为谷歌还没有真正实现这种应用内审查流程。名为 in_app_review_dialog_fragment、in _ app _ review _ dialog _ rate _ review _ layout 和 in _ app _ review _ dialog _ thank _ you _ layout 的 3 个新布局文件当前为空。我们不会发现这个应用内评论流程是什么样子的，直到后来的 Play Store 版本填充了这些布局。我们检查了代码，发现提到了一些相关的标志，但我们没有学到任何有用的信息。

## 滥用的可能性？

谷歌本可以在几年前增加应用内审查流程，但评级滥用的可能性阻止了他们这样做。如果应用程序可以在 Play Store 之外进行审查，那么我们可能会看到一些技巧，如使用辅助服务来打开对话框，对应用程序进行评级，然后在用户不注意的时候离开。或者，一个应用程序可以使用覆盖来改变原始对话框，欺骗用户给出比他们预期更高的评级。

然而，自 Android 早期以来，谷歌一直在大力打击这些潜在的滥用渠道。例如，Android Q [阻止后台活动启动](https://www.xda-developers.com/android-q-security-privacy-features/)，最近的 Android 版本还强制带有前台服务的应用程序显示持久通知。用于叠加的 SYSTEM_ALERT_WINDOW API 将最终被 Android Q 的新 Bubbles API 完全取代[。我不知道谷歌将如何验证通过 Play Store 新的应用内审查对话框提交的评级的完整性，但我相信如果不考虑这些问题，他们不会开发这样的功能。我会留下进一步的猜测，当该功能更接近推出。](https://www.xda-developers.com/android-q-system-alert-window-deprecate-bubbles/)

我希望谷歌能借此机会打击那些提供虚假应用内评论对话框的应用——你知道，那些告诉用户如果他们对 Play Store 用户评分规则进行评分就联系开发者的应用已经有一段时间没有更新了，但如果应用内评论流成为现实，我们可能会看到新的规则被添加进来。

* * *

*感谢 PNF 软件为我们提供了使用许可 [JEB Decompiler](https://www.pnfsoftware.com/?aid=xdadev) ，这是一款针对 Android 应用的专业级逆向工程工具。*