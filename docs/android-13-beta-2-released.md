# Android 13 Beta 2 推出了新的预测性背部手势

> 原文：<https://www.xda-developers.com/android-13-beta-2-released/>

Android 13 的第一个开发者预览版于今年 2 月发布，最近它发布了第一个测试版。现在在谷歌 I/O，该公司宣布第二个测试版已经可以下载，用户可以从今天开始在他们的谷歌 Pixel 智能手机上试用。

与仅面向开发者的“开发者预览”版本不同，Android 13 的测试版面向希望尝试下一版本 Android 的普通用户。谷歌特别关注普通用户对新版安卓系统的普遍反馈。因此，虽然你可能仍然应该对在你的日常驱动中安装它保持警惕，但是这个版本应该比以前的版本更稳定一点。

安卓 13 测试版 2 最显著的特点包括:

*   预测性背部手势
*   用于指定支持的应用程序语言的资源文件
*   使用精确报警的新许可

* * *

## Android 13 什么时候发布？

对于 Android 更新，谷歌通常会揭示一个“平台稳定性”里程碑，以便开发者可以知道谷歌打算何时交付最终的 SDK/NDK API，以及最终的内部 API 和面向应用的系统行为。谷歌打算在 2022 年 6 月达到平台稳定，在正式发布前至少计划几周。Android 12 于 2021 年 8 月达到平台稳定性，最终版本于当年 10 月发布[。谷歌发布了](https://www.xda-developers.com/android-12-launched/)[更多关于发布时间表](https://developer.android.com/about/versions/13/overview)的细节，你可以查看一下。

* * *

## Android 13 Beta 2 有什么新功能？

### 预测性背部手势

浏览应用程序可能很烦人，尤其是使用后退按钮的时候。并不总是清楚滑动返回是否会关闭你所在的应用程序，或者导航到你打开的上一个活动。这就是为什么谷歌推出了“预测性背部手势”，这种手势可以在用户真正完成之前向他们显示他们的滑动将带他们去哪里。应用程序开发人员也可以很容易地将它集成到他们的应用程序中。

你可以在 Android 13 Beta 2 中启用这一功能，方法是执行以下操作。

1.  在你的设备上，进入**设置>系统>开发者选项**。
2.  选择**预测后退动画**。
3.  启动您更新的应用程序，并使用后退手势来查看它的运行情况。

**更新:**谷歌告诉我们，你还不能实际测试这个。开发人员可以实现它，但“预测性背景动画”在全面上市前不会上线。

### 用于指定支持的应用程序语言的资源文件

开发者[现在可以指定他们的应用](https://developer.android.com/about/versions/13/features/app-languages#use-localeconfig)将支持什么语言，这样用户就可以根据每个应用选择语言。

### 使用精确报警的新许可

谷歌推出了 [`USE_EXACT_ALARM`](https://developer.android.com/reference/android/Manifest.permission#USE_EXACT_ALARM) 权限，不过你的应用需要符合以下两个标准之一才能申请并在谷歌 Play 商店获得批准。

*   你的 app 是闹钟 app 或者时钟 app。
*   您的应用程序是一个日历应用程序，显示即将发生的事件的通知。

* * *

## 错误修复和其他解决问题

### 开发者报告的问题

*   修复了一些设备在安装 Android 13 Beta 1 后无法连接到无线运营商网络的问题。([问题编号 230538853](https://issuetracker.google.com/issues/230538853)
*   修正了当从快速设置磁贴中选择时，二维码扫描有时不工作的问题。([问题编号 230513882](https://issuetracker.google.com/issues/230513882)
*   修正了用户解锁设备后应用图标偶尔会不出现的问题。([问题编号 230851024](https://issuetracker.google.com/issues/230851024)

### 其他已解决的问题

*   修复了蓝牙耳机有时无法接听电话或播放通话音频的问题。
*   修复了如果安装超过 300 个应用程序，Pixel 6 和 Pixel 6 Pro 设备将崩溃并重新启动的问题。
*   修复了启用蓝牙时 Pixel 6 和 Pixel 6 Pro 设备会不断重启的问题。
*   修复了 Android 密钥库中的一个导致一些应用程序在启动时崩溃的回归问题。
*   修复了一个问题，在某些情况下，系统会错误地显示一个应用程序的空通知组。
*   修正了在设置抽屉中长按蓝牙导致界面崩溃的问题。
*   修正了一个问题，在收到 OTA 更新后，设备有时会在启动时卡在谷歌标志上。
*   修正了当 USB-C 耳机插入时暂停设备会导致设备崩溃和重启的问题。

* * *

## 如何在你的谷歌 Pixel 设备上下载并安装 Android 13 Beta 2

你可以很容易地[下载 Android Developer Beta 2](https://www.xda-developers.com/how-to-download-android-13/#beta2) ，如果你不确定如何安装 Android 13 ，请务必查看我们关于[如何安装 Android 13](https://www.xda-developers.com/how-to-install-android-13/)的指南。

谷歌正式发布了 Pixel 6 Pro、Pixel 6、Pixel 5a 5G、Pixel 5、Pixel 4a (5G)、Pixel 4a、Pixel 4 XL 或 Pixel 4 的测试版更新。您可以在 Android Studio 的 Android 模拟器中使用 64 位系统映像，也可以使用 GSI。

* * *

你对最新的测试版有什么想法？你会在你的设备上安装它吗？你的体验如何？请在下面的评论中告诉我们！