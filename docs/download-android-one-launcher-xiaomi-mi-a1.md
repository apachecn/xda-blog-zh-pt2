# 在启用 Google Feed 的情况下，从小米 Mi A1 下载 Android One 启动器

> 原文：<https://www.xda-developers.com/download-android-one-launcher-xiaomi-mi-a1/>

2017 年年中，安卓开发者阿米尔·扎伊迪(在 Reddit 上被称为[阿米尔兹](https://www.reddit.com/user/AmirZ))发布了谷歌像素启动器的[无根端口，将谷歌 Now 面板添加到无根设备的主屏幕上。它是同类产品中第一个这样做的，并带来了新一波第三方发射器，如与 Google Now 集成的](https://www.xda-developers.com/developer-ports-the-pixel-launcher-with-the-google-now-panel-for-unrooted-devices/) [Lawnchair](https://www.xda-developers.com/lawnchair-launcher-free-play-store/) 和新版 [Nova Launcher](https://play.google.com/store/apps/details?id=com.teslacoilsw.launcher&hl=en) 。本周，AmirZ 从小米 Mi A1 上提取了 Android One 启动器(预装在 Android One[设备上的 Android 主屏幕)，并分享了他如何做到这一点的细节。](https://www.android.com/one/)

Android One Launcher 和谷歌 Pixel Launcher 没有太多区别。前者有一些用户界面的变化，包括外观略有不同的应用程序 dock，重新设计的应用程序抽屉，以及位于新位置的谷歌搜索栏。但差异主要是审美上的。

至于 AmirZ 如何做出改变，方法非常简单，基本上与 XDA 资深成员 [paphonb](https://forum.xda-developers.com/member.php?u=6018897) 如何让谷歌 Pixel Launcher 与 Google Now 面板一起工作的方法相同。因为 Android One Launcher 保留了与原始版本相同的包名，所以它可以从[谷歌应用](https://play.google.com/store/apps/details?id=com.google.android.googlequicksearchbox&hl=en)接收信息，这允许它访问和显示 Google Now 面板。问题是，它不能在任何设备上工作——如果没有 Android 系统作为可调试应用程序构建的启动器，它就不能工作。所以 AmirZ 的修改版本做了一些事情，包括允许应用程序由 Android 自己管理日志。这是在 [AndroidManifest.xml](https://developer.android.com/guide/topics/manifest/manifest-intro.html) 文件中定义的，该文件包含了应用程序的许多参数:

```
 <manifest xmlns:andro
    ...
    <application android:icon="@drawable/icon"
        android:debuggable="true" 
```

一旦做出了改变，AmirZsimply 就用一个新的密钥(因为他无法获得谷歌的 Android One Launcher 原始密钥)重新签署了应用程序，并对其进行了重新打包。

你可以从下面下载修改过的启动器，但是你需要确保你的设备上没有安装谷歌 Pixel 启动器或者 Android One 启动器。

* * *

[**下载 Android One Launcher port by AmirZ**](https://www.androidfilehost.com/?fid=817906626617958389)