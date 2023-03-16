# 通过 Google Files Go 共享的应用程序将由 Google Play 进行验证

> 原文：<https://www.xda-developers.com/google-play-offline-p2p-sharing-files/>

# 通过 Google Files Go、SHAREIt 和 Xender 共享的应用程序将由 Google Play 进行验证

申请的真实性(它来自谷歌 Play 商店吗？)将被内置在像 Files Go 这样的 P2P 共享应用中的元数据所验证。

谷歌已经研究出一种方法来保护那些喜欢侧加载应用程序的用户的安全。早在 6 月份，[他们开始自动将安全元数据](https://www.xda-developers.com/google-play-security-metadata/)添加到任何上传到谷歌 Play 商店的应用程序中，这样当它们在其他地方共享时，可以被验证为来自 Google Play。这有助于用户让他们的侧装应用程序从 Google Play 接收更新，就像他们从 Play 商店安装一样，也有助于开发人员更好地跟踪这些用户以获得支持。但是这种安全措施有一个很大的缺陷:只有当设备在线并与谷歌 Play 商店连接时才有效。由于谷歌实现这一功能是为了帮助数据计划和连接有限的国家的用户，这需要得到解决。

这就是为什么他们已经开始在某些点对点文件共享应用中实现元数据检查。这样，用户将能够验证应用程序的真实性，并确认它来自谷歌 Play 商店。在应用的成功对等交换之后，接收者将能够从播放商店获取更新。谷歌已经在 [SHAREIt](https://play.google.com/store/apps/details?id=com.lenovo.anyshare.gps) 中实现了离线 P2P 认证功能，但未来对[谷歌文件 Go](https://play.google.com/store/apps/details?id=com.google.android.apps.nbu.files) 和 [Xender](https://play.google.com/store/apps/details?id=cn.xender) 的更新也将添加这一新的检查。对开发者来说幸运的是，他们不需要做任何事情就能从这种变化中获益。你所有的应用在离线点对点分享时都会经过 Google Play 的验证。

上面提到的文件共享应用可以从下面的谷歌 Play 商店列表中下载。请密切关注未来几天和几周内 Files Go 和 Xender 的更新，看看它何时实现这一新功能。

* * *

[**来源:安卓开发者博客**](https://android-developers.googleblog.com/2018/10/offline-p2p-installs-beta.html)