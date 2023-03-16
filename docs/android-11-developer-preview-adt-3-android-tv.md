# 谷歌为其 ADT-3 安卓电视盒子发布了安卓 11 开发者预览版

> 原文：<https://www.xda-developers.com/android-11-developer-preview-adt-3-android-tv/>

去年年底，[谷歌宣布了用于 Android TV 的](https://www.xda-developers.com/google-android-10-android-tv-adt-3-developer/) Android 10 和与之配套的新 ADT-3 开发者设备。ADT 设备完全面向开发人员，他们保证会收到来自谷歌的更新和安全补丁。今天，谷歌宣布了 ADT-3 盒子的 Android 11 开发者预览版。

Android TV 的 Android 11 开发者预览版不包括任何视觉更新或面向用户的变化，但在表面下有很多事情正在发生。它带来了一系列隐私、性能、可访问性和连接特性。此外，Android TV 应用程序现在可以使用许多新的 API。

我们在二月份的第一个 Android 11 开发者预览版中写了关于新开发者特性的文章。有几个对 Android 电视设备特别重要。其中最值得一提的是低延迟视频解码，它允许应用程序检查和配置特定编解码器的低延迟播放。这对于像[体育场](https://www.xda-developers.com/google-stadia-elder-scrolls-online-windbound-cris-tales-premiere-edition-99/)这样的实时流媒体服务非常重要。

Android TV 的另一个重要特性是 HDMI 低延迟模式。这允许应用程序检查和请求外部显示器和电视上的自动低延迟模式(通常称为“游戏模式”)。在这种模式下，显示器或电视会禁用图形后处理，以最大限度地减少延迟。

我们还发现，Android 11 增加了对[一系列新游戏控制器](https://www.xda-developers.com/android-11-84-new-gaming-controller-mappings/)的支持，这对于使用 Android TV 玩游戏来说非常方便。Android 11 为 Xbox、Razer、Mad Catz 等增加了 84 个新映射。控制器映射允许 Android 将按钮恰当地关联到正确的按键事件。因此，如果你点击“A”按钮，它将转化为游戏中的[“A”键事件](https://developer.android.com/reference/android/view/KeyEvent#KEYCODE_A)。

如前所述，Android TV 的 Android 11 开发者预览版严格来说是面向开发者的。下图仅适用于 ADT-3 开发设备。闪存后，ADT-3 设备上的所有用户数据都将被擦除。一旦设备被刷新到 Android 11，你将无法回到之前的 Android 10 版本。

1.  下载系统镜像([链接](https://dl.google.com/dl/developers/android/rvc/images/adt/adt3-user-rp1a.200521.001-factory-542bfe28.zip))并解压文件。
2.  插入适用于 Android TV 的 ADT-3 开发套件并启用开发人员选项。
3.  在解压后的文件夹中运行 *flash-all.sh* ，对 ADT-3 设备进行手动系统镜像安装。

flash-all 脚本使用 fastboot 和 adb 工具来升级系统。推荐使用最新版本的 fastboot 开发者可以在 [Android SDK 平台-工具包](https://developer.android.com/studio/releases/platform-tools.html)中找到。

* * *

**来源:[谷歌](https://android-developers.googleblog.com/2020/06/android-11-dp-on-android-tv.html)**