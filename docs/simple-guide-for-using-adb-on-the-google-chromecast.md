# 在谷歌 Chromecast 上使用 ADB 的简单指南

> 原文：<https://www.xda-developers.com/simple-guide-for-using-adb-on-the-google-chromecast/>

如果说谷歌 Chromecast 有起有落，那是一种保守的说法。在它发布后不久，我们[了解到了一种找到设备](http://www.xda-developers.com/android/chromecast-secure-boot-exploit-and-root/ "Chromecast Secure Boot Exploit and Root")的方法，这要归功于破碎图像签名验证。然而，没过多久，[这个漏洞被堵住了，OTA 更新设备上的 root 访问也被移除了](http://www.xda-developers.com/android/latest-google-chromecast-ota-blocks-root-method/ "Latest Google Chromecast OTA Blocks Root Method")。自那以后，我们还看到了一个应用程序[在任何 Android 设备上模拟 Chromecast 功能](http://www.xda-developers.com/android/turn-your-extra-android-device-into-a-chromecast-receiver-with-cheapcast/ "Turn Your Extra Android Device into a Chromecast Receiver with CheapCast")，以及一个应用程序[逆向工程协议](http://www.xda-developers.com/android/play-almost-any-video-on-your-chromecast-with-aircast/ "Play Almost Any Video on Your Chromecast with AirCast")以绕过谷歌的白名单限制。然而，在 XDA，我们是超级用户。此外，电力用户还希望获得亚行贷款。

现在，多亏了 XDA 资深会员 [death2all110](http://forum.xda-developers.com/member.php?u=2975319) ，那些有幸通过使用[备用系统映像](http://forum.xda-developers.com/showthread.php?p=44194208#post44194208)保留 root 权限的人现在可以通过本指南轻松访问亚行。首先，您需要将根 Chromecast 和 telnet 放入带有 PuTTY 或任何其他 telnet 客户端的设备中。几个命令和一个 *wget* (下载 adbd)之后，你就可以启用 adbd 了。接下来，您只需 *chmod* 新下载的 adbd 拥有适当的权限，然后执行它。最后，您使用*ADB connect【Chromecast 本地 IP 地址】*从客户端计算机连接到您的 chrome cast。

该指南有很多图片，甚至还有视频演示，以确保你不会被卡住。基本上，如果你已经扎根了，那就再简单不过了。前往[教程线程](http://forum.xda-developers.com/showthread.php?t=2407250)开始学习。