# 开发者为联想幻影 Solo 发布基本的 2D 白日梦虚拟现实启动器

> 原文：<https://www.xda-developers.com/2d-daydream-vr-launcher-lenovo-mirage-solo/>

独立的[联想 Mirage Solo](https://www.xda-developers.com/lenovo-mirage-solo-headset-daydream-worldsense/) Daydream VR 耳机实际上能够启动二维应用程序和游戏，但该设备默认情况下没有提供这样做的方法。你必须使用一种繁琐的变通方法，包括在 PC 上从 Play Store 远程安装应用程序，然后在 Mirage Solo 上打开设置，然后打开你想要启动的应用程序设置页面，*然后*启动应用程序的 Play Store 详细信息页面，然后*最后*点击“打开”以实际启动你想要的应用程序。由 [*UploadVR*](https://uploadvr.com/android-daydream-app-standalone-how-to/) 概述的完整步骤向你展示了这是多么的乏味。幸运的是，一个开发者发布了一个 2D 应用启动器，让你不用经历这个痛苦的过程就可以启动其他 2D 应用。

简单提醒一下，Mirage Solo 是第一款采用谷歌的 [WorldSense](https://www.youtube.com/watch?v=aJD34uGPQf8) 技术来跟踪你的位置和[Project seura](https://www.xda-developers.com/seurat-google-vr-open-source/)技术来实现高保真 VR 场景的 Daydream VR 耳机。它提供 6 个自由度的跟踪和船舶与高通骁龙 835 片上系统。(相比之下，Oculus Go 提供 3 个自由度的跟踪功能，并搭载高通骁龙 821，尽管其零售价为 199 美元，而 Mirage Solo 的售价为 450 美元。)

一位名叫 MikeDG 的开发者发布了开源 [KISS Launcher](https://kisslauncher.com/) 的修改版。(他修改的源代码可以在这里查看[。](https://github.com/mikedg1/KISS))他们所做的修改允许 KISS Launcher(‘SIKK Launcher’)从 Daydream VR Launcher 上发射。启动后，您可以通过键入名称来过滤列表或使用控制器滚动列表来轻松搜索已安装的 2D 应用程序。以前启动的应用程序会自动添加到主屏幕上以便快速访问，这些应用程序可以被收藏，因此它们会被钉在主屏幕上。

这是开发者提供的一段视频，他用启动器打开了 WWE 应用程序:

据开发者称，这款应用的优势如下:

*   启动 Google 相册并选择自动备份，这样您就可以轻松备份截图和屏幕录像。
*   快速启动蓝牙设置来配对新的蓝牙设备。开发者表示，配对蓝牙耳机对他们有效，多个用户报告配对游戏手柄也有效。
*   当然，你可以比以前更快地启动你的 2D 应用。

查看 *UploadVR* 玩 PUBG Mobile 作为一个例子，你可以在联想 Mirage Solo 上用 2D 应用程序和游戏做一些疯狂的事情。

在你摆弄你的 Mirage Solo 上的 2D 应用和设置之前，有几件事你应该知道:

*   **不要禁用蓝牙。**您的 VR 遥控器依靠蓝牙与耳机进行通信。如果关闭蓝牙，您将无法控制您的设备。
*   **启用 USB 调试，设置 ADB。**如果你*碰巧搞砸了什么，那么如果你在电脑上安装了亚行，你就可以解决大部分问题。(例如，如果您不小心禁用了蓝牙，但您有 ADB，那么您可以通过以下命令打开蓝牙:`svc bluetooth enable`)。*
**   bug:home 键有时候只会启动当前应用。开发人员不确定为什么会发生这种情况，但表示一个简单的重新启动就可以解决问题。*

 *你准备好试试这个发射器了吗？你可以从下面的链接下载。不过，你需要侧装，因为开发者声称 Play Store 的高标准阻止他甚至尝试在线提交这个应用程序。你可以从 ADB 下载 APK，或者通过谷歌浏览器从原始线程下载。

[**下载联想 Mirage Solo Daydream VR 耳机**](https://drive.google.com/open?id=1ihn4z7NwRLyu3BV2qaTB9dRmRRL-yRSy) 的改良 KISS Launcher

[**下载镜像**](https://www.androidfilehost.com/?fid=890278863836289470)

*本文更新了开发者提供的启动器的真实截图。**