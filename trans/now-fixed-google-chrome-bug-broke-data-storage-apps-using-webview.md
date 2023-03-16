# 谷歌 Chrome 接收更新以修复擦除应用程序数据的错误

> 原文：<https://www.xda-developers.com/now-fixed-google-chrome-bug-broke-data-storage-apps-using-webview/>

# 现已修复的谷歌 Chrome bug 破坏了许多使用 WebView 的应用程序的数据存储

谷歌现在已经开始推出谷歌 Chrome 的更新，修复了使用 WebView API 的 Android 应用程序中的数据擦除错误。

本月初，谷歌[开始在所有平台上推出 Chrome 79](https://www.xda-developers.com/google-chrome-79-password-phishing-protection/) 。此次更新带来了大量新功能，包括更好的密码保护、实时网络钓鱼保护、扩展的预测性网络钓鱼保护等。但随着新功能的出现，Chrome 79 也引入了一个错误，该错误导致使用 WebView API 的 Android 应用程序的数据丢失[。](https://bugs.chromium.org/p/chromium/issues/detail?id=1033655)

根据 ArsTechnica 最近的一份报告，数据丢失是由于谷歌改变了 Chrome 79 存储个人资料的位置，而没有迁移旧数据。这导致受影响的应用程序重置为新安装的状态。在关于该漏洞的一份声明中，谷歌的一位发言人写道:“在检测到 WebView 中的一个问题后，Android 设备上 Chrome 和 WebView 的 M79 更新被暂停，因为一些用户的应用数据在这些应用中不可见。此应用程序数据没有丢失，并将在我们本周发布更新时在应用程序中可见。我们为任何不便道歉。"

谷歌已经开始为 Android 推出 Chrome 79 (79.0.3945.93 ),它带来了以下功能，以及稳定性和性能的改进:

*   WebView 错误修复:解决了 WebView 中一些用户的应用程序数据在这些应用程序中不可见的问题。应用数据未丢失，并将在此更新后在应用中可见。参见[crbug.com/1033655](http://crbug.com/1033655)
*   密码安全:当你登录一个网站时，Chrome 现在可以警告你，如果你的密码以前在数据泄露中暴露过
*   支持虚拟现实:WebXR 设备 API 支持沉浸式在线虚拟现实体验
*   重新排序书签:将书签拖到位，或轻按书签的选项菜单并选择上移或下移

Chrome 79 中引入的变化的完整列表可以在 [Git 日志](https://chromium.googlesource.com/chromium/src/+log/79.0.3945.79..79.0.3945.93?pretty=fuller&n=10000)中看到。您可以通过下面的链接从 Play Store 下载 Chrome 79 修补程序更新。如果你是受上述错误影响的几个人之一，你应该在更新后取回所有的旧数据。但是，请注意，在上次更新后，您可能会丢失受影响的应用程序收集的任何新数据。

* * *

**来源:[谷歌博客](https://chromereleases.googleblog.com/2019/12/chrome-for-android-update_17.html)**

**Via:[Ars Technica](https://arstechnica.com/gadgets/2019/12/chromes-data-disaster-browser-update-wipes-out-android-app-data/)**