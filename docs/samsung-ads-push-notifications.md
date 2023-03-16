# 三星仍在通过推送通知向用户发送广告

> 原文：<https://www.xda-developers.com/samsung-ads-push-notifications/>

三星手机以预装大量臃肿软件而闻名。曾经，每一个预装的谷歌应用都有一个三星的同类应用。如今，随着最新的 Galaxy 旗舰设备上预装的软件越来越少，软件情况有所改善。三星没有改进的一个地方是他们喜欢通过推送通知发送广告。

今天，我收到了三星推送服务的一则广告，提供我三星 Galaxy Tab S3 100 美元的折扣。这种折扣是每个人都可以享受的，并在三星网站上列出。该公司正在向使用三星 Galaxy S9 或 Galaxy S9+的用户发送这些通知。这则广告试图在新款 Galaxy Tab S4 发布之前销售 Galaxy Tab S3。

三年前 [*AndroidPolice*](https://www.androidpolice.com/2015/08/21/samsung-appears-to-be-pushing-notification-ads-to-some-users/) 写了一篇关于该公司通过三星推送服务向他们的设备发送广告的文章。当时该公司正在德国为 Galaxy S6 Edge+做广告。去年， *[TheNextWeb](https://thenextweb.com/insider/2017/06/12/samsung-galaxy-s8-notifications-ads/)* 写道，三星游戏启动器应用程序向 Galaxy S8 用户发送新的免费游戏广告。

我今天收到的这个新广告可以说比之前的推送通知更糟糕，因为它不是通过他们自己的游戏启动器广告一个免费的应用程序，而是广告一个售价 450 美元的产品。也许你们中的一些人会有不同的感觉，但是在我看来，广告一些免费的应用程序和广告昂贵的产品是有区别的。

如果您收到了来自三星推送服务的这些推送通知或任何其他广告，并希望停止接收它们，您可以使用 ADB[禁用应用程序](https://www.xda-developers.com/uninstall-carrier-oem-bloatware-without-root-access/)。只需运行以下命令:

```
 adb shell pm uninstall -k --user 0 com.sec.spp.push 
```

这将禁用该应用程序，并将其视为不再安装在设备上。这将适用于过去 3 年的任何 Galaxy 设备。

我认为一家公司向已经为他们的产品付了钱的人发送广告是不对的。购买设备时，我并不期望在上面看到广告。我希望我的体验没有广告，没有膨胀。幸运的是，禁用三星推送服务可以在一定程度上缓解这种情况。