# [更新:它回来了]无根像素发射器现在在谷歌 Play 商店与像素桥

> 原文：<https://www.xda-developers.com/rootless-pixel-launcher-google-play-store-pixel-bridge/>

**更新:9/11:** 自原文章发表后，无根 Pixel Launcher 被 Play Store 下架。现在它又可用了，除了必须侧装的 Pixel Bridge companion(如下)。

当我们谈到定制启动器时，人们通常会提到基于或类似于谷歌像素启动器的启动器。还有 [Lawnchair](https://www.xda-developers.com/hands-on-with-lawnchair-v2-a-customizable-pixel-launcher/) ，[精益发射器](https://forum.xda-developers.com/android/apps-games/app-lean-launcher-customisable-pixel-t3757408)，[无根像素发射器](https://www.xda-developers.com/rootless-pixel-launcher-3-6-theme-selection-notch/)，[无情](https://forum.xda-developers.com/android/apps-games/app-ruthless-pixel-launcher-based-t3755903)等等。无根 Pixel Launcher 特别有趣，因为它基于 Android 的开源 Launcher3，并与反编译的 Pixel Launcher 源代码合并。它是由阿米尔·扎伊迪开发的，自从最初的谷歌 Pixel 发布以来，他一直致力于该项目。Lean Launcher 和即将发布的 Lawnchair 实际上已经把它作为基础，并在其上添加了他们自己的功能。从某种意义上来说，无根 Pixel Launcher 只是一个稳定的软件基础，其他开发人员可以拿来添加。

不过这种方式有一个缺点:它使用 Pixel Launcher 的原始包名。这是因为它可以显示 Google Now 面板和“一览”功能，而无需使用任何配套应用程序。无根像素发射器 3.8 改变了这一点，因此它可以在谷歌 Play 商店上发布。

## 无根像素发射器 3.8 现在在谷歌 Play 商店

首先，无根的像素桥使得这个发射器能够到达谷歌 Play 商店。它使用了与[新星同伴](https://www.xda-developers.com/nova-google-companion-allows-google-now-integration-on-lollipop/)类似的方法，除了阿米尔·扎伊迪告诉我它与*任何*发射器兼容**。它也是完全开源的，因此开发人员可以学习如何在他们自己的启动器中实现对它的支持。安装过程如上所述——真的就这么简单。无根的 Pixel Bridge 所做的只是充当一个握手转发器，所以当 Google 对他们的 API 进行修改时，它仍然可以正常工作。开发人员只需要对他们的启动器进行修改，以适应这些 API 的变化。**

无根 Pixel Launcher 3.8 仍然基于 Android Oreo，未来的版本可能会随着 Android 9.1 的发布而计划。目前，没有真正的理由去经历 Android Pie 的 Pixel Launcher 的反编译和去模糊过程。没有足够的新功能来证明这一过程，所以相反，我们开始看到无根像素桥和其他一些小的变化和改进。

谷歌 Play 商店链接在下面。请注意，您不能从以前的版本中导入旧布局，您必须重新安装。这是因为签名密钥发生了变化，以适应 Play Store 版本。谷歌 Pixel 用户还必须等待 Magisk 模块为无根 Pixel Bridge 发布。该桥的行为就像谷歌 Pixel launcher 对谷歌应用程序的行为一样，这将与你设备上的*真实* Pixel Launcher 相冲突。

[**下载:无根像素桥 APK**](https://www.apkmirror.com/apk/amirzaidi/rootless-pixel-bridge/rootless-pixel-bridge-v2-release/rootless-pixel-bridge-v2-android-apk-download/)