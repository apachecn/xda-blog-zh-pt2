# Android Pie 对 WiFi 扫描的限制正在削弱一些网络工具

> 原文：<https://www.xda-developers.com/android-pie-throttling-wi-fi-scans-crippling-apps/>

**更新 2(美国东部时间 2019 年 5 月 29 日上午 9 点 04 分)**:一名谷歌员工表示，从 Android Q Beta 5 开始，一个用于切换 WiFi 扫描节流的新开发选项将可用。

**更新 1(美国东部时间 2019 年 5 月 28 日凌晨 01:18)**:谷歌已经证实，对前台 Wi-Fi 扫描的更改将保留在 Android Q 中。

每个人都对 Android Pie 记忆犹新，我们才刚刚开始体验谷歌最新更新带来的一些变化。与其他移动操作系统相比，Android 一直被批评电池续航能力差，但这是一把双刃剑。当然，Android 比其他系统使用了更长的电池寿命，但它允许更多独特和多样化的应用程序专属于该平台。[谷歌已经做了很多](https://www.xda-developers.com/app-standby-buckets-android-p/)来帮助[提高安卓系统的整体电池使用寿命](https://www.xda-developers.com/xda-external-link/doze-mode-an-in-depth-look/)，但是 WiFi 扫描的最新变化干扰了许多网络应用。

因此，随着 Android Pie 的推出，谷歌对应用程序使用该平台 WiFi 扫描功能的频率进行了限制。[谷歌在他们的问题跟踪器中对报告](https://issuetracker.google.com/issues/79906367#comment15)做出了回应，并确认 Android 的最新更新限制了前台应用程序和所有后台应用程序的这一功能。对于前台应用程序，该功能被限制为每 2 分钟 4 次扫描，而后台应用程序被限制为每 30 分钟仅 1 次扫描。

从表面上看，这似乎是减少一些不必要的电池使用的好方法，但在某些情况下，这有负面影响。例如， [WiFi 分析器](https://play.google.com/store/apps/details?id=com.farproc.wifi.analyzer)和 [WiGLE](https://play.google.com/store/apps/details?id=net.wigle.wigleandroid) (一款驾驶应用)等流行的网络应用需要比你的标准应用更频繁地访问 WiFi 扫描。这种变化基本上使这些类型的应用程序变得无用，因为它将它们的扫描速率降低了至少 30 倍，即使它们是在前台使用的活动应用程序。

正如您所看到的，这些异常情况对一些流行的网络应用程序产生了负面影响。谷歌在这个问题上一直很活跃，甚至解释了如何确定节流。到目前为止，谷歌自己还没有提供解决方案，但他们已经开始了，[将这个问题推迟到未来的 Android 版本](https://issuetracker.google.com/issues/79906367#comment21)中“考虑”。

* * *

## 更新 1:还在安卓 Q

根据谷歌问题追踪器上的一条[评论](https://issuetracker.google.com/issues/79906367#comment29)(via[*AndroidPolice*](https://www.androidpolice.com/2019/05/27/android-started-heavily-throttling-wi-fi-scanning-in-pie-google-confirms-its-here-to-stay/))来看，Wi-Fi 节流将会持续下去。但是，Android Q 允许用户使用以下 ADB 命令关闭本地设备上的节流:

```
 adb shell settings put global wifi_scan_throttle_enabled 0 
```

不管评论怎么说，发送这个命令不需要 root 访问权限。

* * *

## 更新 2:切换即将到来的 Q Beta 5

一名谷歌员工在谷歌问题跟踪线程中发布了一条评论,称即将进行切换。从计划于 2019 年第三季度[发布的 Android Q Beta 5 开始，开发者选项中将会有一个关闭扫描限制的开关。您不需要使用前一篇文章更新中提到的 ADB 命令。](https://www.xda-developers.com/android-q-beta-release-schedule/)