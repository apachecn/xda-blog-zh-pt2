# 以下是我们从源代码中了解到的 Android 11 的所有隐藏变化

> 原文：<https://www.xda-developers.com/hidden-changes-android-11-source-code/>

在为其 Pixel 设备系列发布 Android 11 的第一个稳定版本后不久，谷歌[开始向 AOSP 上传 Android 11 源代码](https://www.xda-developers.com/android-11-source-code-aosp/)。我们一直在代码中挖掘，寻找我们在[之前的报道](https://www.xda-developers.com/tag/android-11/)中可能遗漏的隐藏功能，下面是我们的发现:

## 虚拟助理的新音量流

Andriod 11 [为虚拟助手引入了新的流类型](https://android.googlesource.com/platform/frameworks/base/+/b64fac77b551480c0cd51b0ee21c7c9d66af3374%5E%21/):AUDIO _ STREAM _ ASSISTANT。新的流是*“打算由一个虚拟助理使用，如谷歌助理，Bixby 等。音频流有自己的音量别名，音量不会因其他流的音量变化而改变。*

目前，虚拟助理应用程序通常通过媒体音量流发送音频，由其他媒体应用程序共享。有了新的流，Android 11 应该允许虚拟助理应用程序的开发者通过这个新的流发送音频，让用户独立于其他媒体应用程序设置助理音量。

## Android 11 中的时钟插件

在 Android 10 中，我们发现了关于[锁屏时钟定制](https://www.xda-developers.com/android-q-lock-screen-clock-customization/)的工作，它提供了 3 种不同的选项:默认、文本、气泡和模拟。这项功能本来可以在 Pixel Themes 应用程序(“风格&壁纸”)中作为一个名为“时钟”的独立选项卡提供，但是，它没有在最终的 Android 10 版本中推出。

虽然该功能在 Android 11 稳定版中仍然不可用，但谷歌已经[重新启用了](https://android.googlesource.com/platform/frameworks/base/+/5db44f0ece5c641f6be625381f53ce0b54174c18)自定义时钟功能。但由于谷歌在 Android 10 中移除了文本时钟，并在 Android 11 中移除了模拟时钟和气泡时钟，因此目前没有其他时钟选项可用。

我们怀疑谷歌要么只为原始设备制造商启用了该功能，要么该公司可能正在开发新的定制时钟，以便在 Pixel 5 和 Pixel 4a 5G 上与更新的 Pixel Themes 应用程序一起推出。

## 冻结缓存的应用程序

在 Android 11 Beta 2 中，我们[发现了一个正在开发的新功能](https://www.xda-developers.com/android-11-beta-2-new-features/#gallery-3:~:text=Suspended%20execution%20for%20cached%20apps)，名为“暂停缓存应用的执行”当时，我们了解到该功能将存在于开发人员选项中，但我们没有足够的信息来了解它如何工作或如何启用它。

不过，从源代码中，[我们可以看到](https://android.googlesource.com/platform/frameworks/base/+/bdaf16e72aedf06f007c1a8b288c68ee470277d1)该特性旨在*“在缓存时冻结应用程序，并在从缓存中移除或终止后解冻它们。冻结的应用程序不会使用任何 CPU 周期，从而减少了可能试图在缓存时运行的不当进程的功耗。”*

XDA 公认开发者 [*luca020400*](https://forum.xda-developers.com/member.php?u=5778309) 说这个功能需要更新的 cgroups(一个 Linux 内核功能)，所以在目前的设备上无法工作。它可以是针对 OEM 的特征，或者可以在 Pixel 5 上实现。

## 通知阴影模糊

在 Android 11 开发者预览版 3 中，我们设法启用了一个隐藏的[开关来启用窗口模糊](https://www.xda-developers.com/android-11-developer-preview-3-changes/#gallery-10-302302:~:text=Window%20blurs,-A%20hidden)。然而，当时这种开关不起作用。XDA 公认的开发商 [*luca020400*](https://forum.xda-developers.com/member.php?u=5778309) 现在[设法让它工作](https://twitter.com/luca020400/status/1303702842855878656)。

他在华硕 ZenFone 6 上闪现了 Android 11 GSI，并通过更改系统属性启用了该功能。该功能在下拉通知面板后启用 Kawase 模糊效果，这是高斯模糊的一种近似。

## Android 11 中扩展通知的深度新闻支持

在[第二个 Pixel 功能下降](https://www.xda-developers.com/pixel-feature-drop-second-features-list/#tagbar-list:~:text=VOIP.-,Long%20press%20improvements)中，谷歌增加了“改进的长按选项”，让你在 Pixel Launcher、Google Photos 和 Google Drive 中牢牢按住屏幕，以显示上下文菜单。这是访问上下文菜单的另一种方式，它是为那些可能不知道他们可以通过长按屏幕来访问它的人设计的。

该特性利用了 Deep Press API，该 API 使用 ML 模型来推断用户何时在屏幕上更用力地按压。在 Android 11 中，你现在可以在通知面板中的通知上做一个[深按来展开它们。](https://android.googlesource.com/platform/frameworks/base/+/4716913d96b821b757e40a1e1a96b492e5c5ebac)

## 什么是 Gabeldorsche？

Android 11 的开发者选项有一个名为“启用 Gabeldorsche”的开关，描述为“启用蓝牙 Gabeldorsche 功能堆栈”谷歌终于发布了 Gabeldorsche 的文档，这似乎是对 Android 蓝牙协议栈的彻底重写。希望重写将导致更低的延迟和更高的稳定性。如果你有兴趣了解更多，现在就可以查看 Gabeldorsche 蓝牙栈[架构](https://cs.android.com/android/platform/superproject/+/master:system/bt/gd/docs/architecture/architecture.md?q=Gabeldorsche)和[风格指南](https://cs.android.com/android/platform/superproject/+/master:system/bt/gd/docs/architecture/style_guide.md?q=Gabeldorsche)。请注意，GD 蓝牙栈还没有准备好推出，很可能会在 Android 12 或更高版本中推出。

## 什么是增强型连接？

[Android 11 开发者预览版 2](https://www.xda-developers.com/android-11-developer-preview-2-changes/#gallery-4:~:text=New%20%E2%80%9CEnhanced%20Connectivity%E2%80%9D%20toggle) 增加了另一个神秘的开发者选项，名为“增强连接”，但没有任何关于其功能的描述。感谢源代码，我们现在已经了解到，该功能将“允许连接热功率管理器在蜂窝吞吐量低于设定阈值时主动关闭 5G，以节省功率。”

## 多音频焦点

早在 5 月份，我们报道了一个名为 [App Volume Control](https://www.xda-developers.com/app-volume-control-individual-volume-levels-android/) 的根应用，它可以让你控制 Android 应用的单个音量。这是必要的，因为 Android 没有像 Windows 那样的原生音量混合器，所以你不能混合多个应用程序同时播放音频的音量。Android 有“音频焦点”的概念，一次只能有一个应用程序有焦点。

具有音频焦点的应用程序决定其他播放音频的应用程序会发生什么——闪避(降低音量)或暂停播放。这意味着用户无法控制他们最喜欢的音乐应用程序是否总是在他们打开的任何应用程序中播放，如果该应用程序取消了音频焦点并选择暂停播放。在 Android 11 中，看起来谷歌正在开发一个[多音频聚焦功能](https://android.googlesource.com/platform/frameworks/base/+/4e984e55033439223fb45e91a561b85e57248067)，这将允许应用程序同时播放音频，而不会暂停或回避彼此。

## 更快的共享表

除了 Android 10 中的[增强功能，谷歌还对 Android 11 中的份额表进行了一些改进。例如，图标的](https://www.xda-developers.com/android-10-share-menu-faster-quantified/)[加载现在被缓存](https://android.googlesource.com/platform/frameworks/base/+/563d7b9d17c913198554aad2d37e60c1d3ffc196)，这意味着它们出现得更快。 [Scroll jankiness 也有所减少](https://android.googlesource.com/platform/frameworks/base/+/706316db0fec414785dfa870ae20592cd3bf09e1)通过缓存 ViewHolder 中的 itemViewType，缓存 shouldDisplayLandscape 的结果来减少滚动时的 IPC 调用次数，缓存 work profile 用户句柄。

## 更好的内存管理

谷歌推出了[新的 OOM 调整器设计](https://android.googlesource.com/platform/frameworks/base/+/android11-release/services/core/java/com/android/server/am/OomAdjuster.md) (OOM =内存不足，即当空闲内存量接近耗尽时，系统应该做什么)。OOM Adjuster 调整有 3 个因素:进程状态(确定一个进程是在前台还是后台)，OOM Adj 分数(由低内存杀手守护进程或 lmkd 使用，以确定当内存不足时应该终止哪个进程)，以及调度程序组(调整 CPU 进程组和线程优先级)。

系统服务器为 4 种不同的 Android 进程调整这 3 个因素:活动、服务、内容提供商和广播接收器。OOM Adjuster 旨在避免在*“会导致用户可察觉的服务中断”的情况下终止进程*

## Android 11 Go 版改进

低 RAM 设备(读作:Android Go Edition)现在可以支持[多用户、托管配置文件](https://android.googlesource.com/platform/frameworks/base/+/bd16014d0b211fb369abc1f928751b65e2644930)和[通知监听器](https://android.googlesource.com/platform/frameworks/base/+/bc79dcd87b95f4332d9319dd2230f18f49dcf9cb)。对于多用户和管理配置文件，谷歌只取消了阻止它们在低 RAM 设备上工作的运行时限制，因此原始设备制造商仍需要进行一些配置更改才能让它们工作。不过，通知监听器(被授权拦截通知的应用程序，如 Pushbullet)应该可以在没有原始设备制造商输入的情况下工作。

## WCG 壁纸支持

10 位(宽彩色)图像[现在可以在 Android 11 中设置为壁纸](https://android.googlesource.com/platform/frameworks/base/+/287d8283f4f232a0a31ef038e61b1c2340ef660b%5E%21/)。以前，应用这样的壁纸总是会让他们转化为 sRGB。有趣的是，转换过程中的一个错误导致了今年早些时候臭名昭著的诅咒壁纸崩溃。

## 卷密钥定制

谷歌似乎正在开发一个 API 来检测音量键的单按、双击或三击。我们已经发现了两个名为“[支持音量键](https://android.googlesource.com/platform/frameworks/base/+/4bf177f046e5fe43c775e497e4f2495eda06e302%5E%21/)的定制”和“[支持单击/双击/三击](https://android.googlesource.com/platform/frameworks/base/+/34e68a43d3d366acf8453c53d51fa2b149510bee%5E%21/)的定制”的提交，这两个提交指向了 Android 11 中这个未记录的更改。要启用该功能，长/单/双/三次按键将根据按键事件的时间长度和模式进行区分。

使用辅助服务的应用程序，如 flar2 的 [ButtonMapper](https://play.google.com/store/apps/details?id=flar2.homebutton) 应用程序，已经可以拦截音量按钮按压的 KeyEvent，并使用自己的逻辑来确定用户进行了哪种按压。看起来谷歌现在正在为这种定制编写原生支持，但我们不确定它是否将用于支持 Pixel 设备上的功能，或者它只是在考虑 OEM 的情况下编写的。没有证据表明该功能将被用于改变音乐曲目，它可能只是用于安全相关的功能，例如，检测何时按下音量键三次以发送 SOS。有趣的是，Android [已经有一个隐藏的 API](https://www.xda-developers.com/skip-music-tracks-android-volume-keys-no-root/) 来检测音量键的长按。

## 通过数字福利自动解锁工作档案

在[Digital well being 1 . 0 . 327635162](https://www.xda-developers.com/digital-wellbeing-prepares-add-work-profile-scheduler-pause-apps-automatically/)中，我们发现了一个新的工作调度功能的字符串，该功能将在预定时间到达时自动禁用工作配置文件。在 Android 11 中，数字福利现在可以[自动解锁工作档案](https://android.googlesource.com/platform/frameworks/base/+/a8c58f06d06e1a69b0f3555678f51f679da8ea30)，为这一功能的到来铺平了道路。

* * *

如果你想了解更多关于 Android 11 中引入的所有变化，请查看我们关于第一个 [Android 11 稳定版本](https://www.xda-developers.com/android-11-stable-google-pixel-oneplus-xiaomi-realme-oppo/)和[开发者关注的变化](https://www.xda-developers.com/android-11-features-developers-new-apis/)的帖子。要在您的设备上安装最新的更新，您可以查看下面链接的 Android 11 更新跟踪器。

**[Android 11 更新跟踪器](https://www.xda-developers.com/android-11-update-tracker/) || [小米 Android 11 跟踪器](https://www.xda-developers.com/xiaomi-android-11-update-list-download-install/) || [一加 Android 11 跟踪器](https://www.xda-developers.com/oneplus-android-11-official-oxygenos-11-beta-stable-tracker-download-install/)**