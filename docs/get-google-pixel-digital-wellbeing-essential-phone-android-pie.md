# 在 OnePlus 6/Android Pie 上的 Essential Phone 上获得 Google Pixel 的数字福利

> 原文：<https://www.xda-developers.com/get-google-pixel-digital-wellbeing-essential-phone-android-pie/>

**2018 年 8 月 7 日更新**:根据几个用户的说法，这个 mod 在 OnePlus 6 上也有效。

就在 Digital Wellbeing 之后，谷歌在谷歌 I/O 上推出的新的[反智能手机成瘾功能](https://www.xda-developers.com/android-p-beta-features/)，开始在最新的 [Android Pie 版本](https://www.xda-developers.com/android-pie-google-pixel-google-pixel-2/)上为谷歌 Pixel 和谷歌 Pixel 2 推出，我们设法在基本手机上安装并运行该功能，[今天也获得了 Android 9](https://www.xda-developers.com/essential-phone-android-pie-android-9/)。数字福利实际上很容易移植到运行 Android 9 的基本手机和其他非谷歌设备上，因为 APK 本身不需要任何改变——只需启用正确的平台功能，在正确的位置设置正确的权限，就可以了。只要你在 Android Pie 上的基本 PH-1、OnePlus 6 或其他非谷歌设备可以通过 Magisk 进行 root 访问(当前版本已经可以在 Android Pie 上运行了)，你所要做的就是安装一个 Magisk 模块，让它启动并运行。

**推荐阅读:**[Digital well being now live for the Google Pixel/Pixel XL&Google Pixel 2/Pixel 2 XL](https://www.xda-developers.com/digital-wellbeing-google-pixel-xl-google-pixel-2-xl/)

在我想出必要的步骤后，我请 XDA 的高级成员 [Dil3mm4](https://forum.xda-developers.com/member.php?u=9034316) 把这个过程变成一个 Magisk 模块，非常感谢他的帮助！我们还得到了 XDA 公认的开发商 Maxr1998 的帮助！这是模块，后面是我们如何让它工作的解释，供好奇的人参考:

[**下载 Android 版数字福利启用码**](https://androidfilehost.com/?fid=5862345805528068207)

## 我们如何在运行 Android Pie 的基本手机/OnePlus 6 上实现数字福利

从第二个 Android P 开发者预览版开始，该应用被预装在谷歌 Pixel 智能手机上，然而，它只是一个占位符，实际上并没有功能。今天，谷歌在谷歌 Play 商店开放了该应用的测试程序，并开始允许谷歌像素所有者下载占位符应用的更新。我们调出了更新 APK，并检查了它需要运行什么。它只需要:

1.  安卓派(安卓 9)
2.  `com.google.android.feature.WELLBEING`定义为平台特性(通过在`/system/etc/sysconfig`中添加一个定义它的 XML 来解决)
3.  `com.google.android.feature.PIXEL_EXPERIENCE`定义为平台特性(通过在`/system/etc/sysconfig`中添加一个定义它的 XML 来解决)
4.  作为特权系统应用安装，因为它需要一些权限(例如新的 Android Pie 权限`android.permission.OBSERVE_APP_USAGE`)
5.  由于 Android 8.0 Oreo 中引入的限制，需要定义特权应用程序权限(通过在`/system/etc/permissions`中添加定义权限的 XML 来解决)

因为#2-5 需要修改系统分区，所以在基本手机或 OnePlus 6 上获得数字福利需要 root 访问权限。对于那些不希望 SafetyNet 失败的人，我们制作了 Magisk 模块，这样你就不必为了让 Google Pixel 的数字福利功能在你的基本手机或运行 Android Pie 的 OnePlus 6 上工作而牺牲 Google Pay 或 Pokemon Go。

*本文进行了更新，以反映此 mod 也适用于 OnePlus 6。*