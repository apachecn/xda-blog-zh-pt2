# Android Toast 消息可被滥用来授予可访问性或设备管理权限

> 原文：<https://www.xda-developers.com/android-toast-message-overlay-attack/>

Android 是一个非常开放的平台，有一个非常棒的开发者社区。这些开发者中的许多人会开发应用程序、定制 rom 等等。一些组织也参与安全测试，例如 Palo Alto Networks Unit 42。这个小组发现了 Android Toast 消息系统中的一个漏洞，该漏洞允许攻击者创建一个伪覆盖来欺骗用户在他们不知情的情况下授予危险的权限。这已经在[九月安全更新](https://www.xda-developers.com/android-security-bulletin-september/)和 Android Oreo 中修复了**，所以请放心，如果你的手机仍然每月收到安全补丁，或者你有 Android Oreo 设备，你就不会容易受到这种攻击。**

所有其他 Android 设备都容易受到这种攻击。其工作方式是，它利用 Android 中的 toast 通知来绕过“在顶部绘制”ie 的要求。覆盖许可，这就是“[斗篷和匕首](https://www.xda-developers.com/cloak-and-dagger-exploit-uses-overlays-and-accessibility-services-to-hijack-the-system/)”漏洞利用的工作原理。研究人员利用这一漏洞对用户进行社交工程设计，向他们的攻击应用程序授予可访问性服务，允许他们读取所有屏幕内容、按键输入等。在设备上。然后，他们使用相同的方法诱使应用程序用户授予管理员访问权限，而他们完全不知道自己刚刚授予的访问权限。这使得攻击者可以安装应用程序，监控设备，也为勒索软件的潜在威胁打开了方便之门。

## Android Toast 消息覆盖攻击解释

但是它实际上是如何工作的呢？概念验证背后的[开发者分享了他们攻击的实际源代码，其中包含了漏洞背后更多的技术解释。但是我们将简要解释这种利用是如何以及为什么工作的。](https://researchcenter.paloaltonetworks.com/2017/09/unit42-android-toast-overlay-attack-cloak-and-dagger-with-no-permissions/)

首先，你需要考虑什么是祝酒词。它们已经在 Android 上存在多年了，你可能每天都会在你的设备上看到很多。祝酒词是屏幕底部的小信息，通常出现在一个灰色气泡中，带有一条信息。

该漏洞利用 toast 消息在屏幕上创建一个覆盖图，而实际上并不请求或需要 **SYSTEM_ALERT_WINDOW** 权限，这应该是任何应用程序在屏幕上绘制的一个要求。相反，它通过 toast 通知推动覆盖，创建按钮，这些按钮看起来像是合法地授予良性权限或接受无意义的提示，但实际上是授予设备管理员或可访问性对应用程序的访问权限。它在 toast 覆盖图中创建了两个视图。

由于权限检查失败，所有这些都可以完成。Android 系统(Oreo 之前和 9 月之前的安全更新)实际上并不检查通过 Android Toast Overlay 系统输入的内容，而是在不检查的情况下授予权限。这很可能是因为 Google 没有预见到通过 toast 覆盖图提供视图的可能性。

### Android 7.1 试图修复 Android Toast 覆盖攻击

在 Android 7.1 中，谷歌似乎试图阻止这一漏洞。toast 消息有一个超时限制:每个 UID，一个应用程序的进程 ID，只能有一个 toast 消息。这很容易通过重复循环和显示更多的 toast 覆盖图来绕过，因此给用户一种这是一致的 UI 的错觉。如果没有创建循环，3.5 秒后覆盖将消失，用户将看到应用程序实际上要求用户做什么-授予设备管理或访问权限。

### 成功攻击的后果

当授予应用程序设备管理员或可访问性权限时，很容易被各种恶意攻击利用。勒索软件、键盘记录器和设备擦拭器都可以利用这一漏洞创建。

应用程序不需要任何权限就可以显示 toast 消息，但显然恶意应用程序仍然需要 BIND_ACCESSIBILITY_SERVICE 和 BIND_DEVICE_ADMIN，以便有效利用这种 toast 覆盖攻击。因此，如果您的设备还没有打补丁，那么对付这种攻击的最佳防线就是检查应用程序在安装时在其 AndroidManifest 中定义的权限。如果您安装了一个应用程序，但不确定为什么该应用程序需要辅助功能服务或设备管理权限，请立即卸载它并联系开发者。

令人担忧的是，Android 如此简单的一部分——低级的 toast 消息——可以被利用来对用户进行社交工程，以授予危险的权限。我们希望制造商尽快在设备上推出 9 月份的安全补丁，以保护数百万容易被这种漏洞利用的人。