# Fingerface Xposed 模块可以在任何应用程序中解锁 Pixel 4 的面部

> 原文：<https://www.xda-developers.com/use-google-pixel-4-face-unlock-any-app/>

**更新 1 (11/1/19 @美国东部时间下午 2:24):**线上出现了项目的一个新分叉。

[谷歌 Pixel 4](https://www.xda-developers.com/google-pixel-4-specs-features-pricing-availability/) 可能不是第一款具有安全面部识别硬件的 Android 智能手机(之前是 OPPO Find X 和华为 Mate 20 Pro)，但它是第一款具有面部解锁功能的 Android 设备，该功能在 Android 的 BiometricPrompt API 下被认为是安全的。这意味着 Pixel 4 是第一款让你不仅可以用脸解锁手机，还可以验证应用程序或支付的 Android 智能手机。然而，应用程序开发者[必须更新他们的应用程序](https://www.xda-developers.com/google-pixel-4-users-wait-developers-add-face-unlock-support/)才能使用 BiometricPrompt，所以每个银行和密码管理器应用程序都需要一些时间来支持新的面部解锁。由于 Pixel 4 没有指纹扫描仪，使用旧 API 的应用程序将简单地退回到要求您手动输入密码。幸运的是，有一种方法可以解决这个问题，只要你愿意用 Magisk 作为 Pixel 4 的根并安装 Xposed 框架。

XDA 初级成员 [SemonCat](https://forum.xda-developers.com/member.php?u=5384808) 开发了一个名为“Fingerface”的暴露模块，它代理旧的指纹 API，而不是调用新的生物计量提示 API。这意味着每当使用旧指纹 API 的应用程序要求您扫描指纹时，新的生物计量提示对话框将出现，让您扫描面部。这是一个简单而粗糙的解决方法，但总比在所有应用程序中手动输入长密码要好。

这是来自开发者的一个快速屏幕记录，显示了一个应用程序(在本例中为 Magisk Manager)要求指纹认证，但却收到了面部认证:

在我看来，这很好地展示了 Xposed 框架的威力。Xposed 允许模块挂钩到其他应用程序的方法中，在原始方法之前、期间或替代原始方法执行它们自己的方法。这正是这个模块正在做的事情；当 PackageManager 检查设备是否支持指纹硬件时，FingerFaces [总是返回“true”](https://github.com/SemonCat/Fingerface/blob/master/app/src/main/java/com/edison/fingerface/ModPackageManager.kt#L23)，并且它还[挂钩到](https://github.com/SemonCat/Fingerface/blob/master/app/src/main/java/android/hardware/fingerprint/MyFingerprintManager.java)FingerprintManager API(现已弃用),该 API 被应用程序用来在其 authenticate 方法中调用 BiometricPrompt。将这种攻击转化为 Magisk 模块并不容易，因为它将涉及到替换框架的每个设备和每个构建的模块，但开发者说他正在努力。

我应该指出，目前在谷歌 Pixel 4 上安装这个模块并不容易。首先，Pixel 4 还没有 TWRP 支持，所以你必须手动安装 Magisk。这意味着你必须[下载工厂镜像](https://www.xda-developers.com/google-pixel-4-xl-factory-images-kernel-source-code/)，提取启动镜像，使用最新的 Magisk 管理器修补启动镜像[，然后快速启动刷新修补后的启动镜像。要安装 Xposed，您必须安装 Riru Core Magisk 模块，然后安装 EdXposed，这是 Xposed 框架的非官方继任者。关于如何做的说明可以在](https://www.xda-developers.com/magisk-v20-stable-release-android-10-support/)[这里](https://forum.xda-developers.com/pixel-4-xl/how-to/xposed-discussion-thread-t3992607)找到。最后，您可以安装 Fingerface 模块。

有些人可能会出于安全考虑嘲笑这个模块，但是这个模块是开源的，从快速浏览来看，它似乎只做了它应该做的事情。此外，这种模式的存在对 Android 10 或 Pixel 4 本身的安全性没有任何影响，因为它需要用户在解锁引导加载程序后手动获得 root 访问权限。最后，这个 mod，像我们论坛上的大多数其他 mod 一样，旨在供那些重视便利和更多功能的人使用，尽管有解锁引导加载程序和 root 访问的额外风险。

如果你对这个 mod 感兴趣，你可以从下面的谷歌 Play 商店链接下载。如果你从 Play Store 获得，它的价格是 0.99 美元，但由于该应用程序是开源的，你也可以自己编译它。[如果您对此应用程序有任何问题或反馈，请访问 XDA 论坛主题](https://forum.xda-developers.com/pixel-4-xl/themes/xposed-fingerface-faceid-backward-t3993139)。对于阅读这篇文章的任何应用程序开发人员，谷歌[发表了一篇关于通过 AndroidX 生物特征库实现生物特征 API 的博文](https://android-developers.googleblog.com/2019/10/one-biometric-api-over-all-android.html)。更新你的应用，这样用户就不必使用这种肮脏的黑客！

* * *

## 更新 1: TopJohnWu Fork

XDA 认可开发者 topjohnwu，Magisk 的开发者本人，决定分叉这个项目来清理代码。

因为这个应用已经是开源的，它的代码看起来无害，所以照原样运行它没有任何害处。然而，如果你想尝试一个更有声誉的开发者的版本，那么你可以从 [topjohnwu 的 GitHub](https://github.com/topjohnwu/Fingerface) 下载。