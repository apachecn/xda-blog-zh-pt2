# Chrome OS 将最终在开发者模式下支持 Android 的 ADB 访问

> 原文：<https://www.xda-developers.com/chrome-os-adb-access-android-apps/>

大约两年前，Chrome OS 首次获得了对 Android 应用程序的支持。去年，大多数 Chromebooks 都支持 Play Store。从那以后，我们看到了 Chrome OS 中 Android 应用程序的用户体验的许多改进。Chrome OS 增加了一些功能，如[浮动键盘](https://www.xda-developers.com/chrome-os-adding-floating-keyboard/)、[分屏](https://www.xda-developers.com/chrome-os-split-screen-mode-android-apps/)、[锁屏通知](https://www.xda-developers.com/chrome-os-lock-screen-notifications/)等等。谷歌 Chrome 的触摸优化版本也在开发中。

然而，这并不意味着操作系统已经实现了功能对等。Android 仍然比 Chrome 操作系统拥有更多的功能，目前，它是一个触摸优化程度更高的操作系统。Chrome OS 最近为 Android 应用程序添加了[真正的多任务处理，现在，Chromium Gerrit 中的新承诺表明，该操作系统最终将支持开发者模式下 Android 的 ADB 访问。](https://www.xda-developers.com/chrome-os-64-android-apps-simultaneous/)

ADB (Android Debug Bridge)是 Android 不可或缺的工具。它允许用户完成大量的任务，否则没有 root 用户是不可能完成的。像[Andromeda](https://www.xda-developers.com/andromeda-substratum-50-percent-sale/)(sub tum 的无根插件)这样的应用使用 ADB 在没有根的 Android Oreo 上安装自定义主题。到目前为止，Chrome 操作系统中的 Android 缺乏这种访问权限，这意味着许多高级任务根本无法执行。

Chrome OS 将很快支持开发者模式下 Android 应用的 ADB 访问。提交号 952470 现在已经被合并为 a15200e 。标题是:“ **arc:添加一个守护进程将 ADB 小工具暴露给 Android”。**描述如下:

> #### 这一改变使得 Android 可以在开发者模式下通过 USB 使用 ADB。

> #### CQ-依赖=CL:953091，CL:953656，CL:955675，CL:*585579，CL:*585580
> 
> BUG=b:70349025
> 
> TEST = `adb shell '在经过大量修改的 soraka 上工作
> 
> 测试=平台 _ 文件权限
> 
> TEST=cheets_ContainerSmokeTest
> 
> TEST=cheets_SELinuxTest
> 
> TEST=cheets_ContainerMount

另外，[提交号 953091 现在已经合并为 ad921f4](https://chromium-review.googlesource.com/c/chromiumos/overlays/chromiumos-overlay/+/953091) 。标题为:“ **arc-adbd:添加 arc-adbd 服务**”。以下是描述:

> #### 这一更改增加了。arc-adbd 服务的 ebuild。这仅在以开发人员模式运行时启用。

> #### CQ 依赖=CL:952470
> 
> BUG=b:70349025
> 
> TEST = `adb shell '在经过大量修改的 soraka 上工作

由于承诺现在已经合并，Chrome 操作系统将很快支持通过 adb shell 为 Android 访问 ADB。这将仅在用户的 Chromebook 以开发人员模式运行时启用。对于希望在 Chrome 操作系统上调试 Android 应用程序的开发人员来说，这将非常有用。

有趣的是，这些 Chromebook 的测试命令提到了“大规模修改的 soraka”，这是一款未经宣布的可拆卸 chrome book，我们在过去的中已经报道过[。然而，我们仍然不知道它的发布时间框架。](https://www.xda-developers.com/detachable-chromebooks-soraka-poppy-wake-on-voice/)