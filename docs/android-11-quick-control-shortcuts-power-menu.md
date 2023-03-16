# Android 11 DP2 在电源菜单中揭示了“快速控制”快捷方式

> 原文：<https://www.xda-developers.com/android-11-quick-control-shortcuts-power-menu/>

**更新 1 (3/20/2020 @美国东部时间下午 2:08):**Kieron Quinn 进一步完善了他的应用程序，以挂钩 Android 11 中的新控件 API。他还为我们提供了一台 APK，我们用它来录制新功能的视频。此外，我们还发现了此功能的官方文档。

当谷歌上个月发布 Android 11 开发者预览版 1 时，我们发现了一个新功能，我们相信它会将长按电源菜单转变为家庭自动化快捷方式的控制中心。现在随着 [Android 11 开发者预览版 2](https://www.xda-developers.com/android-11-developer-preview-2-google-pixel-announcement-changelog/) 的发布，我们设法让这个功能部分工作。

门户网站的朋友和公认的开发者 [Quinny899](https://forum.xda-developers.com/member.php?u=3563640) 在他的 Pixel 2 XL 上闪现了最新的 Android 11 预览版后，与我们分享了以下两张截图。在上个月分析了框架和 SystemUI 之后，他开发了一个可以与新的开发中的 API 挂钩的应用程序。他的应用程序上个月没有工作，但现在在这个版本中部分工作。

正如你所看到的，他提出了一个新的快捷方式，出现在电源菜单的“快速控制”部分。电源菜单本身也进行了改进，磁贴移到了屏幕顶部，为快速控制留出了大量空间。还有一个菜单按钮，当点击时，打开“添加控制”活动，让你选择你想在电源菜单中显示哪些应用程序的快捷方式。尚不清楚新的“[快速访问钱包](https://www.xda-developers.com/android-10-11-developer-preview-quick-access-wallet-google-pay/)”功能将适合这一新的电源菜单设计。

谷歌尚未正式推出这项新功能，但从我们之前的分析来看，我们认为谷歌将为家庭自动化快捷方式保留这一空间。我们在 framework.jar 的 Controls 服务中找到了一个“有效设备类型”列表，其中列出了风扇、咖啡机、空调、窗帘等可以通过这个 UI 控制的设备。应用程序开发人员可能需要为他们的智能家用电器的表面控制添加对该 API 的支持。我们可能会在[虚拟谷歌 I/O 2020 活动](https://www.xda-developers.com/google-io-2020-canceled/)期间听到更多关于这个 API 的消息，假设它不会像 [Cloud Next 2020](https://www.xda-developers.com/google-cloud-next-2020-online-only-event-coronavirus-fears/) 那样被推迟。

## 更新 Android 11 的视频和文档

当我们第一次在 Android 11 开发者预览版 1 中发现新的“控件”API 时，谷歌在 Android 开发者网页上没有任何关于该 API 的文档。随着 Android 11 开发者预览版 2 的发布，该文档[现在已经悄然发布](https://developer.android.com/reference/android/service/controls/package-summary)。奇怪的是，谷歌并没有在他们的官方博客中提及此事。文档确认了所有[支持的设备类型](https://developer.android.com/reference/android/service/controls/DeviceTypes)，基本上确认了快速控制用于家庭自动化快捷方式。XDA 承认开发人员 Quinny899 进一步完善了他的应用程序，在快速控制区域添加了一个亮度滑块。他的应用程序使用一个假的“灯泡”设备连接到控件 API，允许我们看到快速控件菜单是什么样子以及它是如何工作的。

即使文档现在是公开的，这基本上确认了 Android 11 的功能，我们仍然必须手动激活新的 UI。我无法想象谷歌会对电源菜单进行如此剧烈的改变而不谈论它，所以我怀疑谷歌会在一次虚拟的谷歌 I/O 会谈中明确谈论这个新的 API。