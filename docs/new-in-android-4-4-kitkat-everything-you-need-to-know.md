# Android 4.4 KitKat 的新功能:你需要知道的一切

> 原文：<https://www.xda-developers.com/new-in-android-4-4-kitkat-everything-you-need-to-know/>

所以期待已久的[谷歌 Nexus 5](http://forum.xda-developers.com/google-nexus-5) 是[终于来了](http://www.xda-developers.com/android/google-nexus-5-finally-released-go-get-yours-now/ "Google Nexus 5 Finally Released! Go Get Yours Now!")。随着新设备的出现，出现了新版本的 Android:4.4 版“KitKat”。大约两个月前，谷歌[宣布了他们最新版本 Android 的名字](http://www.xda-developers.com/android/google-announces-android-4-4-kitkat/ "Google Announces Android 4.4 KitKat")。然而，没有说太多关于操作系统，以及什么将是不同于 4.3 果冻豆。这与 Nexus 5 的硬件形成了鲜明的对比，后者似乎在很久以前就已经是板上钉钉的事情了。无论如何，现在设备和操作系统都是可用的。因此，所有剩下的细节都暴露出来了。

昨晚，[我们报道了](http://www.xda-developers.com/android/kitkat-to-target-wearables-ease-fragmentation-and-improve-support-for-nfc-and-lower-end-devices/ "Android 4.4 KitKat to Target Wearables, Ease Fragmentation, and Improve Support for NFC and Lower End Devices")一些(当时)传言将在今天正式发布中包含的关键特性。这个故事主要集中在影响碎片的变化，对新传感器类型的支持，以及改进的 NFC 支持。由于 KitKat 和 Nexus 5 的正式发布以及一些[内部的侦查工作](http://www.xda-developers.com/android/new-runtime-compiler-in-android-4-4/ "BREAKING: New Runtime Compiler in Android 4.4 to Possibly Bring Better Performance in Future Releases")，今天许多这些和更多的功能以及许多新功能都得到了证实。

### 更好的 Google Now 集成

股票启动器将会把 Google Now 放在前面和中间。我的意思是，它就在你的主屏幕上，只需向左滑动一下。在 Nexus 5 上，你可以在主屏幕上的任何地方简单地说“好的，Google Now ”, Google Now 就会开始听你说话。

“OK，Google Now”功能类似于我们在 Moto X 和最新的 Droid 设备上看到的功能。然而，这与以前的产品相比用处不大，因为设备必须开机并在主屏幕上才能工作。

### 内置打印支持 [![print](img/4cd1df22a0c2eaca37034b9ff46942f7.png)](http://www.xda-developers.com/wp-content/uploads/2013/10/print.jpg)

售后打印解决方案能够利用谷歌云打印已经有一段时间了。然而，现在打印已经内置在操作系统中，不需要任何额外的应用程序。

### 更快的多任务处理

Android 4.4 旨在通过优化内存管理和提高触摸屏响应能力来提高多任务处理性能。这一点，加上减少核心应用程序内存占用的努力，应该意味着系统将更好地利用可用的计算资源。

### 全屏沉浸模式

Android 通过允许内容利用所有可用的屏幕空间，使整体体验“更具吸引力”。以前，这仅在视频播放器等特定类型的应用中是可能的，在这些应用中不需要用户输入。

现在，任何应用程序都可以通过淡出两个系统栏来利用整个屏幕。以前，任何用户交互都会返回隐藏栏。然而现在，这些条可以被设置为只在屏幕顶部滑动时才重新出现。这使得任何类型的应用程序都可以利用这一特性，即使在需要用户输入时也是如此。

### 低端设备支持

KitKat 经过了简化，每个主要组件都减少了内存占用，新的 API 旨在帮助应用程序开发人员创建更快、更节省内存的应用程序。这包括新的 API*activity manager . islowramdevice()*，它允许您调整应用程序的行为，以匹配目标设备的内存限制。此外，还削减了核心系统进程，并将新服务配置为以小组形式连续运行，以避免更高的内存需求。

这扩展了昨天的消息，即 Android 4.4 将更适合内存有限的设备。如 Android 开发者网站所述:

> 构建下一代 Android 设备的原始设备制造商可以利用**有针对性的建议和选项**来高效运行 Android 4.4，即使是在低内存设备上。Dalvik JIT 代码缓存调优、内核 samepage 合并(KSM)、交换到 zRAM 以及其他优化有助于管理内存。新的配置选项允许 OEM 调整进程的内存不足级别、设置图形缓存大小、控制内存回收等。

也就是说，尽管声称与低端硬件兼容，但我们发现谷歌选择不将 GSM Galaxy Nexus 更新到 4.4 非常奇怪。谷歌提到这是因为该设备超出了 18 个月的产品生命周期，但我们不禁认为这并没有为其他设备提供商树立一个非常好的榜样。

### 改进的渲染性能

由于渲染引擎的变化，使用 RenderScript 的应用程序将受益于 4.4 中的调整。在这些变化中，Android 的 SurfaceFlinger 从 OpenGL ES 1.0 更新到 OpenGL ES 2.0。这通过使用多重纹理带来了额外的性能，并通过颜色校准和更高级的效果改善了视觉效果。

### 改进的 NFC 支付支持:主机卡仿真

昨天，我们提到 NFC 支付功能将扩展到没有 NFC 安全元件的设备。现在，我们知道这是如何可能的。Android 4.4 引入了对[主机卡仿真](http://developer.android.com/about/versions/kitkat.html#44-hce)的支持，标准 NFC 硬件可以仿真基于 ISO/IEC 7816 的智能卡，这些智能卡使用非接触式 ISO/IEC 14443-4 (ISO-DEP)协议进行传输。这使得任何具有 NFC 硬件的设备都能够使用点击支付功能。也就是说，并不是每个设备都有支持。目前，似乎只有带有美国 SIM 卡的设备才有资格。

### 提高安全性

Android 4.4 现在在强制模式下使用 SELinux，以阻止 SELinux 域内潜在的策略违规。KitKat 还对加密算法进行了改进，增加了对另外两种算法的支持。关于 Android 4.4 中新安全特性的更多信息可以在 Pulser_G2 的 [Android 4.4 安全增强概述](http://www.xda-developers.com/android/android-4-4-security-enhancements/ "Android 4.4 KitKat Security Enhancements")和他对 [*dm-verity* 及其含义](http://www.xda-developers.com/android/google-taking-aim-at-device-modders-in-android-4-4-kitkat/)的广泛评论中找到。

### 短信提供商

应用程序开发人员现在可以使用共享的短信提供商和新的 API 来处理设备消息，以及消息存储和检索。新的 API 使用新的 *SMS_Deliver* 意图，允许应用程序开发人员通过用户的默认消息应用程序路由消息，从而实现无缝的跨应用程序体验。

### 新的传感器模式和改进的连接性

最后，KitKat 增强了连接选项和传感器支持。硬件传感器批处理是一种新的优化，可以显著降低传感器活动期间的功耗。这非常适合低功耗和长时间运行的传感器用例，如地理健身应用等。还增加了对步数检测和步数计数传感器的支持，尽管这取决于硬件。

4.4 也增加了对红外增强器的支持，带来了新的 API 和系统服务。这将允许应用程序开发人员在支持的设备上更好地利用 IR Blasters，而不需要特定于设备的编码。

最后，蓝牙在支持 HID over GATT (HOGP)方面有了很好的改进，它为应用程序提供了一个选择硬件的低延迟链接，并允许应用程序与附近的设备交换消息。

### 安卓设计

在设计方面也做了不少改变。这些包括淡化整个 UI 的蓝色调，以及一些更微妙的变化。下面是一个精彩的概述，详细介绍了 KitKat 中的一些新设计特性:

//www . YouTube . com/embed/6 qhkv-bs LDS

虽然我们没有像之前预期的那样听到任何关于可穿戴设备的消息，但我们肯定在这个万圣节得到了值得的款待。资源消耗、响应能力、沉浸感以及整体契合度和完成度的增强带来了巨大的更新。我们对 Android 4.4 KitKat 带来的东西感到兴奋，我们更渴望看到操作系统的未来。

Android 4.4 最让你兴奋的是什么？请在下面的评论区告诉我们！

在 [Android KitKat 网站](http://www.android.com/versions/kit-kat-4-4/)上可以找到 4.4 中可用的新终端用户功能的完整列表，在 [Android 开发者网站](http://developer.android.com/about/versions/kitkat.html)上可以找到更多以开发者为中心的功能。