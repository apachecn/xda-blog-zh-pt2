# 数字健康准备让您安排聚焦模式

> 原文：<https://www.xda-developers.com/digital-wellbeing-schedule-focus-mode/>

谷歌的数字健康工具于去年年中推出，作为像素专属，但现在可以在许多不同的原始设备制造商的智能手机上使用。自其首次发布以来，数字健康工具增加了一些功能，如[谷歌 Chrome 网站使用跟踪](https://www.xda-developers.com/android-q-google-chrome-digital-wellbeing/)、[家庭链接集成](https://www.xda-developers.com/digital-wellbeing-integration-family-link-parental-controls/)、[应用从启动器暂停](https://www.xda-developers.com/digital-wellbeing-update-pixel-launcher-app-timer-android-q/)，以及最近的[聚焦模式](https://www.xda-developers.com/focus-mode-digital-wellbeing/)来暂停分散注意力的应用。一段时间以来，我们已经通过 Play Store 或其他平台上的其他应用程序看到了“聚焦模式”的变体，但谷歌的实现很方便，因为它是内置的。现在，随着数字福利应用程序 1.0.268678005.beta 版的推出，我们发现了一些证据，表明该功能可以让你安排何时暂停令人分心的应用程序。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些特性目前还没有在实时构建中实现，并且可能会被开发人员在未来的构建中随时引入。

目前，Digital Wellbeing 有两种方法可以阻止你打开浪费时间的应用程序:通过应用程序计时器自动打开(基于屏幕时间的使用)或通过聚焦模式切换手动打开。在不久的将来，你将可以设置在焦点模式下暂停应用程序的时间。例如，您可以设置聚焦模式，在正常工作时间内阻止浪费时间的行为。

以下字符串是在最新的测试版中为调度焦点模式添加的。

```
 <string name="focus_mode_schedule_set">Set</string>
<string name="focus_mode_set_schedule">Set schedule</string>

```

此外，更新中还添加了新的活动 com . Google . Android . apps . well being . focus mode . schedule . focus mode schedule Activity 和新的布局 focus _ mode _ add _ schedule _ list _ item、focus _ mode _ schedule _ fragment _ contents、focus_mode_schedule_list_item 和 focus _ mode _ schedule _ list _ item _ contents。然而，该活动当前在启动时崩溃。不过，除了我们之前发现的“[屏幕时间目标](https://www.xda-developers.com/digital-wellbeing-screen-time-goal/)”之外，我们应该很快就会看到这个特性。到时候我们会通知你的。

* * *

*感谢 PNF 软件为我们提供了使用许可 [JEB Decompiler](https://www.pnfsoftware.com/?aid=xdadev) ，这是一款针对 Android 应用的专业级逆向工程工具。*