# Android Oreo 8.0/8.1 的 Xposed 框架现已推出测试版

> 原文：<https://www.xda-developers.com/xposed-framework-for-android-oreo-beta/>

随着 Android Oreo 的更新，谷歌继续为所有用户完善 Android 体验。值得注意的是，这次更新带来了来自 Android TV 的画中画模式支持、[自动填充框架](https://www.xda-developers.com/android-os-autofill-framework-will-finally-resolve-a-long-standing-lag-issue-with-password-managers/)，它取代了对密码管理器的[落后的可访问性服务](https://www.xda-developers.com/working-as-intended-an-exploration-into-androids-accessibility-lag/)的需求，以及对你的通知进行更精细控制的通知通道。除了这些变化之外，一些以前只支持 root 的调整，比如[主题化你的设备](https://www.xda-developers.com/custom-themes-android-oreo-substratum/)不再需要 root，所以有更少的理由让你的手机 root。尽管如此，对于那些使用你的设备的人来说，你现在有了另一个可以使用的工具:**访问 Android Oreo (8.0/8.1)的 Xposed 框架**。

早在 10 月，XDA 资深知名开发者 [rovo89](https://forum.xda-developers.com/member.php?u=4419114) 发布了 Xposed 框架的更新，[带来了对 Android 牛轧糖(7.0/7.1)](https://www.xda-developers.com/official-xposed-framework-android-nougat/) 设备的支持。那时，安卓牛轧糖已经有一年多了，安卓 8.0 奥利奥也是[最近发布的](https://www.xda-developers.com/android-8-0-oreo-google-released/)。因此，虽然许多拥有 Android 牛轧糖设备的用户对这一发布欣喜若狂，但其他人觉得更新有点晚，因为他们已经转向奥利奥了。

但是在上个月戏弄了发布版之后，Xposed 框架现在已经赶上了 T2 最新的 Android 发布版。这意味着任何新发布的 Android Oreo 设备，如[谷歌 Pixel 2 & Pixel 2 XL](https://www.xda-developers.com/google-pixel-2-xl-announced-price/) 、索尼 Xperia XZ1 系列或[华为 Mate 10 系列](https://www.xda-developers.com/huawei-mate-10-pro-porsche-official/)终于可以试用 Xposed 了。另外，升级到 Android Oreo 的设备(不管是官方的还是非官方的)现在也可以尝试备受尊崇的 Xposed 框架和它的许多模块。

* * *

## 为 Android Oreo 安装 Xposed 框架

**由于这是第一个面向 Oreo 设备的 Xposed 版本，rovo89 将该版本视为测试版**。这意味着它可能有问题，事情可能会崩溃，某些模块可能无法工作，或者其他问题可能会出现。他说，在他的日常驱动程序(Google Pixel)上，它已经足够稳定了，其他开发者，如 XDA 公认的贡献者/开发者 [wanam](https://forum.xda-developers.com/member.php?u=3562083) 也测试了它，但你的里程数可能会有所不同。幸运的是，由于安装 Xposed 框架的先决条件是启动您的设备，这意味着您应该能够在安装之前进行备份。**如需卸载，请使用 xposed-uninstaller-20180108-*。因为它清理了一些额外的文件。**

此外，rovo89 表示，他知道不时会发生一些应用程序崩溃，尽管他声称这并没有损害他的用户体验，一旦找到根本原因，更新的测试版将解决这个问题。目前，rovo89 还**要求您只报告可重现的错误**(即由某些应用程序或操作触发的持续应用程序崩溃或引导)，因为随机崩溃事件更难捕捉和缩小范围。

安装过程一如既往地简单。你所要做的就是安装附加在 rovo89 论坛线程上的 Xposed 安装程序。您还需要将最新的框架 zip 刷新到您的设备上。框架 zip 可以通过自定义恢复(如 TWRP)刷新来安装。运行 Android 8.0 Oreo 的用户将需要安装 SDK 26 框架，而运行 Android 8.1 的用户将需要 SDK 27 框架。更新框架的源代码将会在 Oreo 离开测试阶段后发布。

[**下载 Xposed 安装程序 v3.1.4(见附件)**](https://forum.xda-developers.com/showthread.php?t=3034811)

[**下载 Android 8.0 Oreo 的 Xposed 框架安装程序 ZIP**](http://dl-xda.xposed.info/framework/sdk26)

[**下载 Android 8.1 的 Xposed 框架安装程序 ZIP 奥利奥**](http://dl-xda.xposed.info/framework/sdk27)

* * *

## 结论

Android Oreo 仍然是一个相当新的版本，所以很高兴看到 Xposed 框架已经支持它。一些最受欢迎的 Xposed 模块，如名为 [Amplify](https://www.xda-developers.com/amplify-xposed-module-block-wakelocks-save-battery/) 的电池节省模块和名为 [GravityBox](https://www.xda-developers.com/gravitybox-xposed-module-nougat/) 的定制模块瑞士军刀，被迅速更新以支持 Android 牛轧糖的 Xposed。

*放大曝光模块*

*重力盒曝光模块*

随着 Android Oreo 的 Xposed 框架的发布，我们预计这些模块将更新为支持最新的框架，因为一些模块可能需要调整。例如，rovo89 声明一些模块可能面临挑战，因为它们不能再在 system_server 进程中使用 XSharedPreferences。然而，模块开发人员应该能够找到变通办法——在这种情况下，模块可以在 initZygote()中加载它们的首选项。希望现在 Xposed 支持每一个现代 Android 版本，我们希望在不久的将来看到更多的模块开发。

您想支持 Xposed 框架项目吗？如果是，那么考虑向 rovo89 捐款，支持他所做的工作。

[**捐到 rovo89**](http://repo.xposed.info/donate)

**想下载 Xposed 模块吗？**我们建议关注我们的 x 曝光框架模块子论坛，或者下载 XDA 实验室应用程序并浏览我们的 x 曝光模块集合。

[**曝光模块论坛**](https://forum.xda-developers.com/xposed/modules)

[**下载 XDA 实验室**](https://www.xda-developers.com/xda-labs/)

请记住，许多模块目前可能无法工作，所以请做好准备，等待您喜欢的模块更新。我们将关注现有模块的进展和任何特别有趣的新模块的发布，所以如果你渴望尝试新的模块，一定要关注门户网站。