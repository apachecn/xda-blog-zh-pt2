# Tasker 更新增加了 Logcat 检测，允许许多新的自动化可能性

> 原文：<https://www.xda-developers.com/tasker-update-logcat-detection-automation/>

对于想要定制手机每个部分的高级用户来说，有几个必备的应用程序。MacroDroid、Automate 和 Llama 等应用程序都提供自动化功能，但在我看来，它们都无法与 Tasker 相比。虽然它可能没有最好的用户界面，但 Tasker 是我个人最喜欢的自动化应用程序，因为开发人员非常活跃，有多少插件可供使用，以及社区非常活跃。尽管 Android APIs 在每个新版本中都变得越来越受限制，但 Tasker 开发人员和社区已经找到了绕过这些限制的方法。例如，最新的 v5.9.beta.8 版本添加了一个新特性，它为可能的自动化用例开辟了一个全新的领域:logcat 检测。

**Logcat 检测**

上个月，Tasker 的开发者发布了一个新的测试版，该测试版在 Android 10 上启用了剪贴板监控。由于 Android 10 [阻止后台应用程序读取剪贴板](https://www.xda-developers.com/android-q-blocks-background-clipboard-access/)，你可能想知道这怎么可能。答案是通过阅读 logcat。 [Logcat 是一个 shell 工具](https://www.xda-developers.com/guide-sending-a-logcat-to-help-debug-your-favorite-app/)，它可以获取所有系统事件和应用程序贡献的其他事件的日志。每当写入新的剪贴板条目时，相应的系统日志将包含剪贴板文本。通过读取该日志，Tasker 能够检测当前剪贴板条目是什么。

通常情况下，应用程序不允许读取系统日志，它们也不能要求用户授予它们这样做的权限。这是因为敏感数据可能存在于日志中，并且允许任何应用程序读取日志的能力打开了与隐私和安全相关的整个蠕虫罐。然而，用户可以手动授予应用程序读取日志的权限。如果像 Tasker 这样的 app 声明了 READ_LOGS 权限，那么用户可以通过 ADB 手动授予该权限。当你安装最新的 Tasker 测试版时，它会要求你这样做。

那么你能对 Tasker 中新的 Logcat Entry 事件做些什么呢？开发者自己给你举几个例子:

这些都只是开发人员想出来的不同用例，但这远不是 logcat 检测可以做的事情的完整列表。

下面的视频演示了如何使用 Tasker 来捕获和过滤所需条目的 logcat:

logcat 检测的两个问题是，它的设置远非用户友好，而且如果开发人员调整他们的应用程序发送的日志，它随时都会发生变化。设置这个需要一些尝试和错误，但是一旦你设置好了，你可能就不需要经常修改你的配置了。

**新的快捷动作**

Tasker 的现任开发者其实是[而不是 app 的原开发者](https://www.xda-developers.com/tasker-joao-dias-autoapps-development/)。当前的开发人员过去主要在一套名为 AutoApps 的 Tasker 插件上工作，所以当他接管 Tasker 的开发工作时，他开始将一些插件的功能迁移到主 Tasker 应用程序中。最新的 Tasker 测试版通过添加一个新的快捷操作，从本质上摒弃了 AutoShortcut 插件。

* * *

新的 logcat 条目检测和快捷方式操作是最新测试版中最大的两个变化，但还有其他一些小变化，如改进的获取位置操作、变量预览以及对两个长期存在的错误的修复。你可以在这里阅读完整的变更日志[。你可以在 Google Play](https://www.reddit.com/r/tasker/comments/dsf5gj/dev_tasker_59beta8_the_game_changer/) 上注册[任务测试版，或者现在就下载 APK](https://play.google.com/apps/testing/net.dinglisch.android.taskerm)。