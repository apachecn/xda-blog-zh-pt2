# 如何在您的 Android Oreo 设备上检查 Project Treble 支持

> 原文：<https://www.xda-developers.com/project-treble-android-oreo/>

[在今年的谷歌 2017 年 I/O 大会之前，我们第一次了解到了关于 Project Treble 的](https://www.xda-developers.com/googles-project-treble-modularize-android-so-oems-can-update-devices-faster/)。Treble 是迄今为止 Android 平台最重大的底层变化。为了大大简化，它将供应商实现从 Android 框架中分离出来，以避免长时间等待更新。Project Treble 目前由运行 Android 8.0 Oreo 的谷歌 Pixel 和谷歌 Pixel XL 支持。我们还从最初的公告中了解到，未来，所有搭载 Android 8.0 的设备**(比如，即将推出的[三星 Galaxy S9](https://www.xda-developers.com/source-galaxy-s9-snapdragon-845-oreo/) 和刚刚宣布的索尼 Xperia XZ1 系列)都将提供三重支持。谷歌最近还宣布，他们正在与原始设备制造商合作，将 Project Treble 带到一些现有的旗舰产品中。**

如果你有一款预计会更新到 Android 8.0 Oreo 的旗舰设备，你将如何确定它是否支持 Project Treble？除非发行说明直接告诉你，他们很可能不会告诉你，因为这是一个低级的变化，你必须找到另一种方法。幸运的是，有一个非常非常简单的方法来确定 Android 奥利奥设备是否支持 Treble。

在本教程中，我们将向您展示如何判断您的设备是否支持 Project Treble 。显然，为此，你需要官方的，库存的 Android 8.0 奥利奥，因为 7.0 和更低版本不支持 Treble。提醒一下，如果你有谷歌 Pixel、谷歌 Pixel XL 或任何搭载 Android 8.0 的设备，那么这些设备肯定会支持 Treble。

* * *

## 了解你的 Android 8.0+设备是否支持 Project Treble(终端)

与我们之前完成的大多数 adb/terminal 教程不同，本教程不需要 root，因为我们只是获得一个 build.prop 值。但是，您确实需要 Termux(或任何其他终端应用程序)继续发展。

右图向您展示了它应该是什么样子。一旦在应用程序中设置好，只需输入以下命令:

```
 getprop ro.treble.enabled 
```

它将返回一个布尔值，如果你的设备支持高音则为真，如果不支持则为假。

## 了解您的 Android 8.0+设备是否支持 Project Treble (ADB)

首先，您需要在您的设备上设置 Android 调试桥，以便开始运行。跟随[这篇教程](https://www.xda-developers.com/install-adb-windows-macos-linux/)，因为它有你在 Windows、Linux 和 macOS 上运行所需的一切！然后，你需要连接你的设备，或者通过 USB 调试或者 WiFi 调试(我们推荐后者，但是任何一种都可以)。无论你选择哪一个，一定要检查它是否使用“adb 设备”连接。右图向您展示了它应该是什么样子。

然后，我们将继续启动 ADB 中的 Android 终端。为此，请使用:

```
 adb shell 
```

然后，使用以下命令:

```
 getprop ro.treble.enabled 
```

shell 将返回一个布尔值。如果它返回真，那么恭喜你:你的设备支持项目高音！

* * *

## 说明

这其实很简单。Project Treble 并不是一个你可以在设置、设备信息或其他地方看到或配置的值，但是如果你的设备支持它，build.prop 中的一个偏好设置会让任何应用程序知道这个事实。这可能是因为谷歌 Play 商店需要读取这个标志，以便为像[图形驱动程序](https://www.xda-developers.com/android-o-users-will-update-graphics-drivers-through-play-store/)和其他供应商相关的东西提供更新。所有支持高音的设备都需要此标志。build.prop 文件位于系统分区中，但是它的值在没有 root 用户的情况下也是可读的，这使得本教程成为可能。

然而，这并不意味着你可以在你的设备上简单的添加这个标志到你的 build.prop 来启用 Treble，因为它不会做任何事情。正如我们上面所说的，它需要 OEM 实现，因为它几乎完全是 Android 底层的返工，谷歌实际上正在与 OEM 合作，将 Project Treble 引入现有设备。

因此，这不是一个定制的 ROM 开发者可以像一个常规特性一样简单地烘焙到他们的 ROM 中的东西。如果一家原始设备制造商拒绝与谷歌合作，把它带到他们的设备上，他们可以只推出一个简单的 Android 8.0 更新，而不是三倍。致力于现有手机三重支持项目的原始设备制造商名单也没有透露。因此，在手机开始搭载 Android 8.0 之前(所有运行奥利奥的新设备都需要 Treble 项目)，这将是实际了解您更新的 Android 8.0 设备是否支持 Treble 的唯一方法。