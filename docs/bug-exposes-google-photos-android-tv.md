# 【更新 2: Vu 的声明】Bug 潜在暴露了其他用户在 Android TV 设备上的谷歌私人照片

> 原文：<https://www.xda-developers.com/bug-exposes-google-photos-android-tv/>

**更新 3/4/19 上午 11:35:**在谷歌发出回应后，Vu 现已就 Android TV bug 分享了一份声明(如下)。

Android TV 是谷歌为电视和数字媒体播放器修改的 Android 操作系统。整个 Android TV 体验与 Android 的区别主要在于它的界面，它非常注重语音搜索和内容发现。虽然我们不经常听到 Android TV 和谷歌计划对该操作系统进行的更新，但互联网巨头确实在 Google IO 2018 上宣布了 Android TV 的 Android Pie。除此之外，除了消费内容，你真的不能用电视做太多事情。

然而，在内容发现的过程中，我们可能意外地发现了太多的“内容”。安卓电视和谷歌主页应用程序中新发现的一个漏洞使得用户可以列出几乎所有连接到安卓电视设备的账户。

正如 [@wothadei](https://twitter.com/wothadei/) 所发现的，当他试图通过 Google Home 应用程序访问他的 Vu Android 电视设备时，他可以查看许多用户的关联帐户。~~更糟糕的是，谷歌照片上链接到这些账户的个人照片本可以通过环境模式屏保设置轻松显示，如下图所示:~~

更新:对用户来说幸运的是，这个 bug 没有让谷歌照片显示私人照片成为可能。

用户后来重置了他们的 Android 电视，这阻止了他们访问 Google 相册上的任何图像，甚至是他们自己的图像。也有可能陌生人的照片实际上并没有显示，只是列出了账户；但这本身就是一个不容忽视的隐私问题。这款电视来自 Vu，运行 Android 7，自 2017 年以来没有收到任何安全补丁。运行 Android 8 Oreo 的 Mi Box 3 不存在相同的问题，但[另一名用户已经证实](https://twitter.com/aarjithn/status/1102254356479574018)该问题不仅限于制造商 Vu，但可能与 Android TV、谷歌账户或谷歌 Home 应用程序有关。

目前，还没有修复或解决方法。即使您在专用网络上，其他用户也可以在 Android TV 上访问您的帐户。

## 更新 1:谷歌的回应

我们非常重视用户的隐私。在我们调查这一漏洞时，我们已经禁用了通过谷歌助手远程投拍或在安卓电视设备上查看谷歌照片的功能。

## 更新 2: Vu 的回应

[blockquote author="VU 团队"]Vu Televisions 最近被告知 Android 电视中的 Google Home 应用程序出现故障。在核实这一事件后，Vu Televisions 通知了谷歌，后者确认这是谷歌 Home 应用程序的软件故障。

我们感谢我们的客户让我们注意到这一点，我们可以确认谷歌正在立即纠正他们的错误。

Vu Televisions 以其卓越和响应迅速的客户服务而闻名，是唯一一家在 ISO 9001 设有服务中心的电视品牌。[/blockquote]