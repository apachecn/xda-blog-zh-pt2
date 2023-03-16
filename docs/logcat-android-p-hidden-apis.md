# 如何查看 Android P 中有哪些隐藏的 API 应用在使用

> 原文：<https://www.xda-developers.com/logcat-android-p-hidden-apis/>

2 月下旬，我们发现 Android 开源代码中的提交表明[谷歌将限制应用程序访问 Android 软件开发工具包(SDK)中未记录/隐藏的 API](https://www.xda-developers.com/google-undocumented-hidden-apis-android-p/)。这家搜索巨头后来证实了这些变化；在 [Android P](http://xda-developers.com/tag/android-p) 中，API 限制已经扩展到涵盖 SDK 的 Java 语言接口，从很少使用的接口开始，最终扩展到其他非 SDK 方法和字段。当应用程序使用非 SDK 接口时，第一个 Android P 开发者预览版会显示警告，但不清楚正在访问哪些隐藏的 API。幸运的是，Logcat 使它变得更容易。

[**Logcat**](http://xda-developers.com/tag/logcat) ，一个 Android 调试桥( [ADB](http://xda-developers.com/tag/adb) )的命令行工具，它可以转储 Android 系统消息的运行日志，可以用来查看 Android P 中哪些隐藏的 API 应用程序正在使用。正如 XDA 成员高级 [Telperion](https://forum.xda-developers.com/member.php?u=3694505) 所发现的，用字符串“访问隐藏的”过滤 Logcat 会暴露正在运行的应用程序最近访问的内部方法和服务的列表。

设置 Logcat 最简单的方法之一是从谷歌下载适用于你的电脑操作系统的 ADB 二进制文件，为你的手机安装合适的 USB 驱动程序，并在 Android 的**开发者选项**菜单中启用 **USB 调试**。([华为手机默认禁用 Logcat](https://www.xda-developers.com/huawei-phones-disable-logcat-heres-how-to-restore-access/)；要启动并运行它，请打开拨号器应用程序，输入代码*** # * #2846579# * # ***，选择**后台设置**，并勾选对话框中的每个设置。)我们推荐使用 [Matlog](https://play.google.com/store/apps/details?id=com.pluscubed.matlog) ，这是一款低开销、易于使用的应用程序，由 XDA 初级会员[pluscused](https://forum.xda-developers.com/member.php?u=6820962)开发。它可以从源代码编译，也可以从谷歌 Play 商店下载。

[app box Google play com . plus cued . matlog]

要添加滤镜，点击 Matlog 右上角的三点菜单，选择**滤镜**，点击**添加滤镜。**然后输入**“访问隐藏”**(不带引号)并选择**确定。**

虽然大多数应用程序访问隐藏的 API 相对无害，但谷歌限制 Android P 中非 SDK 接口的决定旨在防止滥用那些可能危及用户隐私和安全的 API。卢森堡大学的研究人员进行的一项研究发现，许多恶意应用程序使用私有的内部 API 方法将广告代码注入任何应用程序，包括系统服务。

这也是谷歌打击安卓流氓应用的更广泛努力的一部分。Android P 限制后台应用程序访问设备[摄像头](https://www.xda-developers.com/android-p-background-apps-camera/)和[麦克风](https://www.xda-developers.com/android-p-audio-recording-limitations-privacy/)，谷歌此前威胁[将滥用 Android 可访问性 API](https://www.xda-developers.com/google-threatening-removal-accessibility-services-play-store/)的应用程序从谷歌 Play 商店除名，这些服务旨在使 Android 应用程序对某些残疾人更容易使用，其方式不符合官方指导方针。