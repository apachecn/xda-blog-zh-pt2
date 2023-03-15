# 谷歌 Android 版 Chrome 将很快支持自定义下载文件夹

> 原文：<https://www.xda-developers.com/google-chrome-android-custom-download-folder/>

# 谷歌 Android 版 Chrome 将很快支持自定义下载文件夹

Android 版谷歌浏览器中的一个新标志将允许你改变默认的下载文件夹。这个标志可以在谷歌 Chrome Canary 上访问。

谷歌 Chrome 浏览器基于开源 Chrome 浏览器项目，由于其开源特性，它可以随时跟踪浏览器的任何发展。我们最近报道，在 Chromium gerrit 中发现一个新的承诺后，Google Chrome for Android 将添加 [HDR 视频播放支持](https://www.xda-developers.com/hdr-video-playback-support-chrome-for-android/)。今天，我们发现谷歌 Chrome for Android 正准备增加一个新功能:更改默认下载文件夹。

目前，谷歌 Chrome 的所有下载都存储在/data/media/user 的/Downloads 文件夹中。该文件夹可能会变得非常混乱，因为该文件夹是大多数应用程序的共享默认下载文件夹。如果你的设备存储空间不足或者从来没有足够的存储空间，那么你可能想把 Chrome 的下载文件夹换成你设备的 SD 卡(如果你有 sd 卡的话)。

这样一个基本功能已经存在于谷歌 Chrome 的桌面版本中，但它最终将转向 Android 版本。我们发现 Chromium gerrit 中的一个[提交](https://chromium-review.googlesource.com/#/c/chromium/src/+/813060/)带来了这个特性。它最近被合并了，启用该特性的标志可以在最新的 [Chromium](https://www.xda-developers.com/xda-spotlight-living-on-the-bleeding-edge-with-chromium-auto-updater/) 的夜间版本中找到。你可以通过复制并粘贴这一行到 Chrome 的地址栏来直接访问这个标志:

```
 chrome: 
```

标志上写着“允许改变 Android 上的默认下载存储位置。”我在我的设备上启用了它，但在 Chrome 的设置中找不到可以更改默认下载文件夹的位置。回头看看提交，这个特性似乎还在开发中，因为提交只是添加了一个标志，但它实际上并没有实现更改下载目录的逻辑。在设置中添加相关首选项的提交尚未被合并，所以这一功能可能还需要几天才能在 Android 版本的 Chrome 上使用，而它将需要更长的时间才能进入 Chrome 的稳定或测试分支。