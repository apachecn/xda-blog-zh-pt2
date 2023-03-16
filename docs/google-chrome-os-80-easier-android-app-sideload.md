# Chrome OS 80 将为开发者带来更简单的安卓应用侧装

> 原文：<https://www.xda-developers.com/google-chrome-os-80-easier-android-app-sideload/>

上周在 Android Dev 峰会上，谷歌宣布了 Chrome OS 爱好者多年来一直想要的一项功能:无需启用开发者模式即可下载 Android 应用。在过去的中，我们已经看到代码提交[会启用这个特性，但是这些实现都没有进入稳定通道。现在谷歌已经正式确认这一功能将在 Chrome OS 80 中实现，该系统将于 2020 年 2 月的第二周稳定发布，我们不再需要虔诚地监控 Chromium Gerrit 的这一功能添加。](https://www.xda-developers.com/sideload-android-apps-chromebook-chrome-os/)

正如你在上面的特色图片中看到的，通过 [*检索关于 Chromebooks*](https://www.aboutchromebooks.com/news/chrome-os-80-to-bring-arc-sideloading-of-android-apps-to-chromebooks/) ，[谷歌增加了这个功能](https://android-developers.googleblog.com/2019/10/high-engagement-larger-screens-how.html)，让 Android 应用程序开发者直接从 Android Studio 部署他们的应用程序。Chromebook 销量同比增长 22%(从 2018 年 9 月到 2019 年 8 月)，Chrome OS 上 Android 应用程序的总使用时间增长了 4 倍，Android 应用程序开发人员受到激励，将他们的工作带到 Chrome book 上。为 Chromebooks 开发需要考虑应用如何对显示模式(笔记本电脑和平板电脑)、窗口管理(多窗口和自由形式窗口)以及键盘/鼠标输入的变化做出反应，因此建议在原生硬件上测试应用。为此，谷歌推动 Chrome OS 变得对开发者更加友好，去年[增加了一个 Linux 容器](https://www.xda-developers.com/chrome-os-linux-app-support-google-pixelbook/)，使其能够运行 Linux 版本的 [Android Studio](https://www.xda-developers.com/android-studio-3-5-changelog/) 。

虽然你可以在 Chromebook 上开发和构建 Android 应用程序，但部署应用程序有点令人头疼。目前，在 Chrome OS 上侧装 Android 应用程序的推荐方式是启用开发者模式。启用开发者模式后，下载 Android 应用程序就像点击你编译的 APK 文件一样简单。但是，开发人员模式本质上是不安全的，因为它放松了经过验证的引导保护，并授予对根 shell 的访问权限。这也是一个痛苦的处理过程，因为它需要对你的设备进行电源清洗(工厂重置),并处理一个烦人的警告屏幕，每次启动时你都必须手动绕过它。幸运的是，当 Chrome OS 80 在 2020 年 2 月在稳定渠道推出时，所有开发人员都将能够直接从 Android Studio 将他们的 Android 应用程序部署到他们的 Chromebook 上，而不必启用开发人员模式。如果你在 Chrome 操作系统开发频道，你最早可以在下个月晚些时候进行测试。

不幸的是，看起来 Google 并不打算让最终用户使用这个特性。根据可能实现该功能的[提交](https://chromium-review.googlesource.com/c/chromium/src/+/1834896)，该功能需要启用 Crostini (Linux 应用支持)，限制哪些 Chromebooks 将可以访问该功能。此外，禁用该功能需要进行强力清洗。不过，如果你习惯命令行，侧装 Android 应用应该和使用“adb install”一样简单。或者，你可以直接“adb 推送”APK，输入“adb shell”，然后使用“pm install”。