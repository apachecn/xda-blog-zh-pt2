# AOSP 出现环境显示常开模式

> 原文：<https://www.xda-developers.com/ambient-display-always-aosp/>

# AOSP 出现环境显示常开模式

在源代码中发现了更多的证据，证明谷歌正在为 Android 开发一个始终在线的环境显示功能。

就在几年前，当 LG 发布 LG G5 和三星发布 Galaxy S7 时，我们看到了对永远显示功能的推动。LG 的实现并不高效，因为它使用的是 LCD 面板而不是 AMOLED，但它仍然表明这是 OEM 想要推动的一项功能，即使是在 LCD 面板上。上个月，我们发现了一些证据，表明谷歌一直在为 Pixel 的[Android O developer preview 3 build](https://www.xda-developers.com/google-is-working-on-an-always-on-ambient-display-mode-for-the-pixel/)开发一种始终在线的环境显示模式。

当我们从这款设备反编译这个更新的 SystemUIGoogle.apk 文件时，我们发现了一个名为“tuner_doze_always_on”的新可调参数(doze 指的是环境显示，而不是电池节省功能)。我们尝试用这个 APK 文件的重新编译版本手动启用它，但我们无法让设备用它启动。当时我们没有任何关于该功能的额外线索，但后来一位接近我们的[消息人士谈到了 Pixel 2 XL 的这一功能](https://www.xda-developers.com/source-pixel-xl-2-will-have-ambient-display-always-on-squeezing-while-screen-off-multiple-display-profiles-and-more/)。

根据我们收到的信息，谷歌将利用该设备的有机发光二极管显示屏的节能功能，并随之推出永远在线的环境显示功能。我们不确定它会有什么样的特性，或者是否会像我们在其他实现中看到的那样受到限制。但很明显，谷歌一直在研究这样一个功能，现在我们有了一些额外的证据来证明这一点。

在挖掘 AOSP 源代码时，我们发现了一个带有“[ambient display:Add always on prototype](https://android.googlesource.com/platform/frameworks/base/+/ebea7a7e56937fbbb18cb0bfcd871af2ee4605fe)”描述的提交。目前还不清楚这项功能的开发有多早，因为它的字符串显示“调谐器的环境显示始终开启”。不可翻译，因为它不应该出现在产品版本中。即使面对 SystemUI 调谐器界面的用户看不到[,](https://android.googlesource.com/platform/frameworks/base/+/android-8.0.0_r1/packages/SystemUI/res/values/strings.xml#1869)[我们也很可能能够编辑它](https://android.googlesource.com/platform/frameworks/base/+/android-8.0.0_r1/packages/SystemUI/res/xml/tuner_prefs.xml)，这样我们就可以访问它。

我们在过去的[中已经用启用导航条调谐器](https://forum.xda-developers.com/nexus-6p/themes-apps/mod-enable-navbar-tuner-nougat-t3447478)这样的模块为其他功能做了这样的事情，所以我们有可能能够用这个始终打开环境显示功能再做一次。