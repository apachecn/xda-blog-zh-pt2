# 谷歌的 Android Flash 工具使得刷新 AOSP 版本变得更加容易

> 原文：<https://www.xda-developers.com/google-android-flash-tool-project-treble-gsi/>

当谷歌发布 Android 8 Oreo 时，他们对 Android 操作系统框架和供应商驱动程序 Linux 内核之间的交互方式进行了重大改变。这个项目被命名为 Project Treble，它使得 Android 智能手机可以启动一个普通版本的 Android，称为通用系统映像(GSI)，而不需要对启动或供应商映像进行许多修改。谷歌每个月都会发布一个最新的 GSI，以符合最新的 Android 安全补丁级别，但他们也不断地从 AOSP 源代码树构建新的 GSI。到目前为止，刷新这些版本需要快速启动命令的知识，但谷歌正在用 Android Flash 工具刷新这些 AOSP 版本，比以往任何时候都更容易。

今天在 [Android 开发者博客](https://android-developers.googleblog.com/2020/01/flashing-android-open-source-project-builds.html)上宣布，Android Flash 工具允许开发者从谷歌的持续集成仪表板中刷新 AOSP 版本。这个仪表板是去年推出的，它允许开发人员轻松下载包含最新 AOSP 变化的图像，而无需每次手动编译 AOSP。致力于向 AOSP 提交变更的开发人员会发现这个工具很有用，但是其他想要测试 AOSP 最新版本的开发人员也会发现这个工具很方便。

要开始使用 Android Flash 工具，只需在任何支持 [WebUSB](https://caniuse.com/#search=Webusb) API 的网络浏览器上访问下面链接的网站。这个工具本质上是浏览器中的快速启动，所以它可以省去你手动下载图像并用快速启动命令刷新图像的麻烦。到目前为止，谷歌将该工具限制在 Pixel 2、Pixel 3、Pixel 3a、Pixel 4 和 HiKey 参考板上，因此您需要其中一个设备才能继续。如果你有一个这样的设备，你需要先解锁引导程序，然后才能刷新一个支持的版本。如果你还没有解锁引导程序，该工具会在它闪烁之前提示你解锁——只是要警告你这样做将会擦除*你手机上的所有*数据。最后，如果你使用的是 Windows PC，你需要安装 Android USB 驱动程序才能继续。

**[安卓 Flash 工具](https://flash.android.com/)**

如果你想恢复库存的 AOSP GSI，你也可以访问谷歌的“[更新和软件修复](https://pixelrepair.withgoogle.com/carrier_selection)页面，指导你恢复库存图像。该页面还有一个使用 WebUSB API 的工具，这意味着它就像刷新 AOSP 版本一样容易。

* * *

*更新 1 @美国东部时间下午 7:10:这篇文章被更新以反映 Android Flash 工具仅支持精选 Pixel 手机和 HiKey 参考板。*