# Xposed 框架得到非官方移植的 Android 馅饼:安装风险自担

> 原文：<https://www.xda-developers.com/xposed-framework-unofficial-port-android-pie/>

Xposed 框架是一个很好的工具，可以用来修改你的 Android 智能手机或平板电脑。该框架与 ART(Android 运行时)挂钩，让应用程序(称为 Xposed 模块)在目标应用程序的原始方法之前、期间或替代原始方法执行自己的方法。因此，Xposed 模块可以比 Magisk 模块修改更多的内容，因为 Magisk 模块只是替换了目标文件。该项目的官方开发者，XDA 资深公认开发者 [rovo89](https://forum.xda-developers.com/member.php?u=4419114) ，尚未宣布他是否有任何计划在 Android 9 Pie 上支持 Xposed 框架。然而，由于官方项目是开源的，第三方开发者已经将 Xposed 移植到任何基于 Magisk 的 Android Pie 设备上。

这个非官方端口是由 Reddit 用户[/u/the perfect 西瓜](https://www.reddit.com/r/xposed/comments/aka36a/news_xposed_for_android_pie/)在/r/Xposed subredit 上引起我们注意的。该端口的形式是一个名为 EdXposed 的 Magisk 模块，它使用一个名为 Riru 的东西作为其核心。根据 Riru 的 GitHub 页面，Riru Magisk 模块提供了一种将代码注入受精卵过程的方法。

我在运行 Pixel Experience 定制 ROM 的谷歌 Pixel 3 XL 和 OnePlus 6 上使用 Magisk 18.0 测试并确认了这一点，但它也可以在旧版本的 Magisk 上工作。由于这是作为 Magisk 模块安装的，它应该能够通过 SafetyNet 认证检查(正如我上面所展示的)，因为它是一个无系统的 mod。因此，你应该能够玩口袋妖怪 GO 或使用谷歌支付。我可以在 Google Pay 中进行购买，但 Pokemon GO 对我来说似乎失败了。您的里程可能会有所不同。

我只想重申一下，这**不是来自原开发者的 Xposed 框架的官方构建，也不是开源的**。这是框架的一个非官方端口，所以支持 Android Pie 的 Xposed 模块不是很多，如果有的话。模块开发者可能会推迟更新他们的应用程序，直到正式发布，但有些人可能会继续更新他们的模块。请留意我们的 Xposed 论坛，看看是否有任何很酷的模块被制作或更新，现在在 Android Pie 上运行 Xposed 在技术上是可能的。

警告:由于这个非官方端口的完整源代码不可用，在你的设备上安装这个软件可能会有风险。在我们的论坛[这里](https://forum.xda-developers.com/xposed/android-9-0-xposed-solutions-t3889513)和[这里](https://forum.xda-developers.com/xposed/tai-chimagisk-t3886673)有很多关于这个非官方港口的讨论。虽然我们可以确认它的功能，但我们不能确认它的安全性。

[**曝光论坛**](https://forum.xda-developers.com/xposed)

## 如何为 Android 9 Pie 安装 EdXposed

1.  下载并安装 [Riru 核心 Magisk 模块](https://github.com/RikkaApps/Riru/releases/download/v11/magisk-riru-core-v11.zip)。
2.  下载并安装[EDX exposed Magisk 模块](https://github.com/solohsu/EdXposed/releases/download/v0.2.9.6/magisk-EdXposed-v0.2.9.6_beta-release.zip)。
3.  重启你的手机。
4.  安装 XDA 资深会员 [DVDandroid](https://forum.xda-developers.com/member.php?u=5345056) 的[曝光安装工具 APK](https://androidfilehost.com/?fid=11410963190603845164) 。

## 面向安卓牛轧糖和安卓奥利奥

官方 Xposed 框架最高支持 Android 8.1 Oreo。我们之前已经在这里写了 Android 7.0/7.1 牛轧糖[和 Android 8.0/8.1 奥利奥](https://www.xda-developers.com/official-xposed-framework-android-nougat/)[的发布。](https://www.xda-developers.com/xposed-framework-for-android-oreo-beta/)