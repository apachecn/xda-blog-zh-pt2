# 新的 Tasker 测试版增加了安全设置权限、Android P 中的锁屏/截图动作等等

> 原文：<https://www.xda-developers.com/tasker-beta-secure-settings-permission-lock-screen-screenshot-action-android-p/>

谷歌 Play 商店最受欢迎的自动化应用 Tasker 最近经历了一次所有权变更。Tasker 广受欢迎的 AutoApps 插件的开发者 joo Dias 现在是应用程序的[所有者和开发者。他对应用程序](https://www.xda-developers.com/tasker-joao-dias-autoapps-development/)有[的伟大计划，他作为 Tasker 所有者的第一个测试是通过在 Play Store](https://www.xda-developers.com/tasker-autoapps-interview-joao-dias/) 上发布[基本不变的测试版来确保他的构建脚本有效。现在，他准备发布他的自动化应用程序的第一个正式测试版更新。joo Dias 领导下的 Tasker 的第一个测试版没有添加大量新功能，但它添加的功能非常重要。](https://www.xda-developers.com/tasker-google-play-beta-program/)

## 安全设置权限

首先，应用程序最终将`WRITE_SECURE_SETTINGS`权限添加到清单中。这不一定是一个功能，但它提供了控制设备安全/全局设置的能力，而不需要额外的插件，如 AutoTools 或 SecureTask。

更新 Tasker 后，您可以通过 ADB 发出以下命令来利用这一新权限:

```
 adb shell pm grant net.dinglisch.android.taskerm android.permission.WRITE_SECURE_SETTINGS 
```

现在，您可以创建写入设备上的`Settings.Secure`或`Settings.Global`表的动作。目前，这需要在 Tasker 中使用 Java 函数，因为该应用程序还没有专门的动作。例如，如果我想反转导航栏，以便交换后退和最近应用按钮:

```
 cr = CONTEXT.getContentResolver();
Secure.putString(cr, sysui_nav_bar, space,recent;home;back,menu_ime) 
```

如果您想疯狂自动化您的设备设置，您可以通过在 ADB 中发出以下命令找到可用参数的完整列表:

```
 adb shell settings list global
adb shell settings list secure
adb shell settings list system 
```

## Android P 辅助功能 API 更新

随着 Android P 的发布，带来了一些新的 API，对 Tasker 等自动化应用很有用。Android 的可访问性 API 中有两个新的全局动作:截屏和锁屏。前者非常直接，而后者的优势更微妙一些，这是我们[之前讨论过的](https://www.xda-developers.com/android-p-action-lock-screen/)。Tasker 现在支持这两个动作，如果你启用了它的辅助功能服务，并且你运行的是 Android P，这些新的动作可以在“动作”的“输入”部分找到。

## 运行时权限

下一个不是面向用户的功能，但它为应用程序符合新的 [Play Store 要求](https://www.xda-developers.com/play-store-updated-requirements-api-level-64-bit/)铺平了道路，这将迫使应用程序以更高的 API 级别为目标。通过添加运行时权限，自动化应用程序现在将请求用户在应用程序需要时授予它敏感权限。说到这个...

## Tasker 现在瞄准了 Android 7.1 牛轧糖

为了遵守新的 Play Store 规则，自动化应用程序现在将目标对准了新版本的 Android——7.1 牛轧糖。它最终会在未来瞄准奥利奥，但迪亚斯选择目前瞄准 7.1，以确保过渡顺利进行。不幸的是，由于这一变化，某些功能，如“通知脉冲”行动不再工作。

* * *

## 立即下载测试版！

[在本页](https://play.google.com/apps/testing/net.dinglisch.android.taskerm)注册测试版，然后从谷歌 Play 商店下载最新版本。测试版可能需要一段时间才会出现，所以请耐心等待！