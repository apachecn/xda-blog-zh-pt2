# 谷歌 Chrome 64 增加了并行下载功能，以加快下载速度

> 原文：<https://www.xda-developers.com/google-chrome-parallel-download-accelerate-download-speeds/>

# 谷歌 Chrome 64 增加了并行下载功能，以加快下载速度

谷歌 Android 版 Chrome 正在增加并行下载功能，以加快 64+版本的下载速度。默认情况下，该功能现已启用。

Android 上的谷歌 Chrome 浏览器每天都在不断增加新功能，变得越来越好。谷歌 Chrome 63 最近推出了稳定频道，并增加了对 Android Oreo 的[智能文本选择功能](https://www.xda-developers.com/android-oreo-smart-text-selection-stable-google-chrome/)的支持。我们最近还发现有证据表明，该浏览器将很快支持 [HDR 视频播放](https://www.xda-developers.com/hdr-video-playback-support-chrome-for-android/)和[自定义下载文件夹](https://www.xda-developers.com/google-chrome-android-custom-download-folder/)，但我们也发现了另一个正在向 Chrome 64 及以上版本推出的功能:**并行下载**。该功能**通过创建并行作业来处理下载，从而加快了下载速度**。

这在理论上应该会提高谷歌 Android 版 Chrome 的下载速度，尽管我没有任何关于它会有多大帮助的数据。根据[提交](https://chromium-review.googlesource.com/#/c/chromium/src/+/812472/)，当下载活动超过 2 秒时，并行下载功能被激活。该功能创建 3 个并行作业来加快下载速度。该承诺提到，该功能将为 100%运行 Chrome 版本 64 及以上的用户启用。这意味着任何运行 Chrome Dev、Chrome Canary 或 Chromium build 的人都将默认启用这一功能，随后会有 Chrome Beta 和 Chrome Stable 推出。

如果你想现在就在 Chrome Beta 上测试这个功能，你可以通过复制粘贴这行代码到地址栏来启用这个标志。

```
 chrome: 
```

这个标志表示它将“启用并行下载以加快下载速度”，实际上是在 3 个月前添加的[，但在经历了大量内部测试后，该功能似乎处于谷歌认为已经准备好为所有用户启用的状态。对于大多数只是偶尔从网上下载小文件的用户来说，并行下载可能不会有太大的不同，但是当你下载较大的文件(如 ROM zips)时，你可能会注意到不同。](https://chromium-review.googlesource.com/#/c/chromium/src/+/656301/)

如果您发现启用此功能后有所不同，请告诉我们。我很好奇它是否能显著提高谷歌浏览器的下载速度。