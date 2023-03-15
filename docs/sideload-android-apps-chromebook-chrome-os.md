# 你很快就可以在 Chromebook 上下载安卓应用了

> 原文：<https://www.xda-developers.com/sideload-android-apps-chromebook-chrome-os/>

# 你很快就可以在 Chromebook 上下载 Android 应用，而无需开发者模式

很快，在 Chrome 操作系统和 Chromebook 设备上下载应用程序而无需启用开发者模式就可能实现。这是根据 Chrome 操作系统代码提交的。

从一开始，对应用程序侧加载的支持就是 Android 的一个标准功能，它让用户可以安装从[谷歌 Play 商店](https://www.xda-developers.com/adultswine-malware-pornography-kids-games-apps/)下载不到的软件。在 Chrome OS 和 Chromebooks 上，自平台上推出 Android 应用支持以来，应用侧加载就已可用，但目前需要启用**开发者** **模式**。然而，根据 Chrome OS 中发现的代码提交，这可能很快就会改变。

该提交引用了一个来自用户的公开错误报告，该用户请求在 Chrome OS 上提供侧加载功能，而无需启用**开发者**模式:

> #### 添加 ARC 侧装设备策略。
> 
> #### 为企业管理员添加简单的布尔设备策略
> 
> 控制允许 Chrome OS / ARC 用户的 APK 侧装。
> 
> #### BUG=761329

正在进行的功能，以及 Android Oreo 的可靠来源，似乎是谷歌集体努力的一部分，旨在使设备上的侧装应用程序更容易，而不损害安全性。但更容易的 Chrome 操作系统侧装不会马上出现在消费设备上 commit 引用了企业 Chromebooks，如企业和学校中的 Chromebooks。当该功能上线时，Chrome OS 管理员将能够通过一个简单的开关来打开和关闭设备群上的 APK 侧加载。

目前还不确定谷歌是否会在不久的将来向普通消费者 Chromebooks 推出侧装支持。但是很有可能。谷歌对 Android Oreo 中的应用程序侧加载行为进行了重大改变，取消了臭名昭著的**未知来源**切换。以前，侧装应用程序需要进入手机的**安全**设置菜单，并切换**“允许未知来源的应用程序”**选项。现在，有了一个新的、更加用户友好的可靠来源机制，允许用户手动授予单个应用程序的安装权限。

希望 Chrome OS 也能效仿。

* * *

[**来源:Chrome Story**](https://www.chromestory.com/2018/01/sideload-android-apps-without-developer-mode/)