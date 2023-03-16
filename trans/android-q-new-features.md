# 以下是谷歌宣布的 Android Q 新功能

> 原文：<https://www.xda-developers.com/android-q-new-features/>

人们期待第一个 Android Q 测试版会在本周发布，而谷歌已经发布了 T1(比预期晚了一点)。与前几年相反，谷歌并没有从“开发者预览”开始。这被称为 Android Q Beta 1。我们已经[谈论了很多关于 Android Q](https://www.xda-developers.com/tag/android-q/) 的新功能，但是谷歌在这个测试版中分享了一些大功能的细节。

## 隐私保护

正如我们之前谈到的，隐私是 Android Q 的一大焦点。这是谷歌在更新细节中提到的第一件事。用户可以更多地控制应用程序何时可以获得位置，这是一个新的选项，即“仅在应用程序正在使用时允许”你不必担心应用程序会在后台侦测到你的位置。

隐私不仅仅是位置共享。允许应用程序访问共享文件的控制越来越多，新的运行时权限可以控制对照片、视频和音频的访问。应用程序必须使用系统文件选择器进行下载，开发者可以使用外部存储上的共享区域。你可以[在这里](https://developer.android.com/preview/privacy/scoped-storage)了解更多信息。

Android Q 将阻止应用程序在后台启动某项活动并接管你的屏幕。谷歌鼓励开发者使用高优先级通知来代替。其他隐私功能包括对 IMEI 和序列号等设备标识符的有限访问。默认情况下，MAC 地址在连接到不同的 Wi-Fi 网络时也会被随机化。

## 可折叠

Android Q 包括对时尚的可折叠手机外形的更多支持。对 onResume 和 onPause 函数进行了修改，以支持多重恢复，并在应用程序获得焦点时通知它。他们还改变了[resizableActivity](https://developer.android.com/guide/topics/ui/multi-window#resizeableActivity)manifest 属性的工作方式，以帮助开发人员管理应用程序在可折叠大屏幕上的显示方式。Android 模拟器现在支持这些新的多显示器类型。

## 共享快捷方式

Android Q 通过分享快捷方式让分享变得更简单。这让用户可以直接跳转到另一个应用程序来分享内容。开发人员可以发布启动特定活动的共享目标，这些目标显示在共享 UI 中。分享快捷方式的工作方式类似于[应用程序快捷方式](https://www.xda-developers.com/android-app-shortcuts-chrome-os-dev-channel/)，因此谷歌正在扩展[快捷信息 API](https://developer.android.com/reference/android/content/pm/ShortcutInfo) 以使两者的整合更加容易。该 API 还将允许 Android Q 之前的设备使用 Direct Share 中的功能。

Android 的共享菜单长期以来一直被抱怨落后和烦人。这次更新可能最终会解决这些问题，但我们必须看看它是如何工作的。由于新的 share API 使用的是推模式而不是拉模式，谷歌声称它的速度更快，因为它不必每次调用时都填充菜单。

## 设置面板

新的设置面板 API 使得直接在应用程序的上下文中显示关键的系统设置成为可能。这利用了 Android Pie 中包含的[切片](https://www.xda-developers.com/settings-slices-google-pixel-android-pie/)特性。设置面板是一个浮动的 UI，可以从应用程序调用来显示系统设置和切换。他们给出了一个浏览器能够显示带有连接设置的面板的例子。

## 连通性

Android Q 增加了蓝牙、蜂窝和 Wi-Fi 网络扫描的位置保护。他们现在要求精确定位许可。谷歌还增加了新的 Wi-Fi 标准支持，WP3 和 OWE，以提高家庭和工作网络以及开放/公共网络的安全性。现在可以通过启用高性能和低延迟模式来请求自适应 Wi-Fi。谷歌表示，这将有助于游戏和语音通话等领域。

在 Android Q 中，应用程序可以请求动态深度图像，这些图像由 JPEG、深度元素的 XMP 元数据以及嵌入在相同文件中的深度和置信度图组成。这将使得在应用程序中提供专门的模糊和散景效果成为可能。谷歌表示，未来这些数据还可以用于创建 3D 图像或支持 AR 摄影。动态深度是一种开放的格式，他们正在与原始设备制造商合作，使其在尽可能多的设备上可用。

Android Q 包括对一些新的音频和视频编解码器的支持。它支持开源视频编解码器 AV1、使用 Opus 的音频编码和 HDR10+。 [MediaCodecInfo API](https://developer.android.com/reference/android/media/MediaCodecInfo) 引入了一种更简单的方法来确定 Android 设备的视频渲染能力。这使得始终选择最佳视频质量进行渲染变得更加容易。

### ANGLE on Vulkan

谷歌正在为所有基于 Vulkan 的设备开发一个标准的、可更新的 OpenGL 驱动程序。Android Q 在 Vulkan 之上增加了对[角度](https://chromium.googlesource.com/angle/angle/+/master/README.md)的实验支持。ANGLE 允许使用 OpenGL es 的应用程序和游戏利用 Vulkan 的性能和稳定性，并从独立于供应商的 ES 实现中受益。Android Q 正在计划支持 OpenGL ES 2.0。

目标是使 Vulkan 成为一个广泛支持的图形开发 API。谷歌正在与原始设备制造商合作，使 Vulkan 1.1 成为所有运行 Android Q 及以上版本的 64 位设备的要求。

## 艺术表演

Android Q 继续改进 ART 运行时，以帮助应用程序更快地启动和使用更少的内存。Google Play 现在提供基于云的个人资料和 apk。

这些是匿名的、聚合的 ART 配置文件，让 ART 甚至在应用程序运行之前就对其进行预编译，为整个优化过程提供了一个重要的启动。基于云的配置文件对所有应用都有好处，并且已经可以用于运行 Android P 和更高版本的设备。

Android Q 优化了 Zygote 进程，提前启动应用程序的进程，并将其移动到安全容器中，以便立即准备就绪。他们还将分代垃圾收集添加到 ART 的并发复制(CC)垃圾收集器中。

* * *

你可以在 [Android 开发者博客](https://android-developers.googleblog.com/2019/03/introducing-android-q-beta.html)阅读更多关于 Android Q 的内容。谷歌 Pixel、Pixel XL、Pixel 2、Pixel 2 XL、Pixel 3 和 Pixel 3 XL [的 OTA 和工厂图片可在此](https://www.xda-developers.com/android-q-dp1-google-pixel-2-google-pixel-3/)下载。你也可以[在这里](https://www.google.com/android/beta)注册安卓测试计划。请继续关注更多关于 Android Q 的信息！