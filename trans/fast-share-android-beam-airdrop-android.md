# 快速共享是一个即将推出的类似隔空投送的 Android 文件共享工具

> 原文：<https://www.xda-developers.com/fast-share-android-beam-airdrop-android/>

当我发现谷歌在 Android Q 中[贬低 Android Beam](https://www.xda-developers.com/google-deprecate-android-beam-api-nfc-share-files/) 时，我惊讶地看到有多少人对这个消息感到不安。文件传输服务使用 NFC 在设备之间传输文件，尽管它很慢且很少使用，但它仍然有其粉丝，因为它的可用性非常广泛。*事实上，每个* Android 设备都支持 Android Beam。现在，为了共享文件，你必须使用其他方法，这些方法不能保证在每台设备上都有效。谷歌通过谷歌应用将用户推向了[文件，但现在看来该公司正在开发一种新的文件共享工具。这款名为 Fast Share 的工具是 Google Play 服务中附近服务的一部分，它看起来不仅是 Android Beam 的替代品，也是苹果隔空投送的竞争对手。](https://www.xda-developers.com/google-files-go-now-files-new-material-theme-design/)

今天早些时候， *9to5Google* 首次发现了快速分享，但是我们[很快就找到了](https://twitter.com/MishaalRahman/status/1145086609911681025)如何访问它来分享下面的截图。我们也感谢 XDA 公认的开发者 [Quinny899](https://forum.xda-developers.com/member.php?u=3563640) 在获得这些截图方面的帮助。截图显示，新的文件共享工具将让你“在没有互联网的情况下分享到附近的设备”，就像 Android Beam 曾经做过的那样。该服务使用蓝牙而不是 NFC 来发起握手，然后通过直接的 Wi-Fi 连接来传输文件。这将允许更大的文件比 Android Beam 更快地传输。快速共享甚至允许您将您的设备“首选可见性”提供给附近的设备，这使这些设备“当您在附近时，即使您没有使用快速共享，也总能看到您的设备。”

分享流程似乎类似于苹果的隔空投送文件共享服务，这是安卓用户多年来一直想要的。您可以将一个或多个文件发送到另一台设备，方法是选择您想要的文件，然后在“共享表单”菜单中选择“快速共享”选项。然后，一旦设备出现在扫描菜单中，您就可以选择要发送到哪个设备。该活动目前显示了通用共享目标，包括 Chromebook、谷歌 Pixel 3、iPhone 和智能手表。希望这项服务一旦上线，将真正支持向 Chrome OS 设备、苹果 iOS 设备和 Wear OS 智能手表发送文件，但我们不能仅仅根据这些通用共享目标的存在来确定。

我们可以确定的是，该服务将支持向其他安装了 Google Play 服务的 Android 设备发送和接收文件。不过，Fast Share 是否需要特定的 Android 操作系统版本，我们还不确定。鉴于它只需要蓝牙和 Wi-Fi 直接支持，我想它会支持大多数现代 Android 版本。

我们将密切关注这项文件共享服务，并会让您知道它是否或何时上线。看起来它将是苹果隔空投送的一个不错的竞争对手，但鉴于它对 Google Play 服务的依赖，有些人会失望，因为它不会像 Android Beam 那样无处不在。众所周知，谷歌将服务从 AOSP 剥离出来，放入 Google Play 服务中，因此这一举动并不令人惊讶。尽管如此，鉴于市场上有这么多认证的 Android 设备，一旦这种新的文件共享工具上市，你可能很难找到不支持它的设备。

* * *

**Via:***9 to 5 Google*