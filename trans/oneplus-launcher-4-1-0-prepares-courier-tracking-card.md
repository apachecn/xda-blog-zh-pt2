# 一加发射器 4.1.0 准备添加一个新的快递跟踪卡到货架上

> 原文：<https://www.xda-developers.com/oneplus-launcher-4-1-0-prepares-courier-tracking-card/>

OxygenOS 是一加的 Android 皮肤版本，是其设备受欢迎的主要原因之一。它为用户提供了一种类似 Android 的普通体验，同时还提供了大量的定制选项。就连设备上的股票应用程序也追随了这一趋势，包括一加启动器。这个启动器起初看起来很小，但它提供了一些关键功能来帮助你充分利用你的手机。一加在每一次更新中都加入了新的功能。该公司此前已经在发射器中添加了一个[停车位置服务](https://www.xda-developers.com/oneplus-launcher-oxygenos-save-parking-location/)和一个[密码保护的隐藏空间](https://www.xda-developers.com/oneplus-launcher-hidden-space-password/)。最近，launcher 的测试版更新引入了一个新的[主屏幕应用布局和一个计数器](https://www.xda-developers.com/oneplus-launcher-homescreen-app-layout-step-counter-shelf/)。现在，该公司正在准备推出一种新的快递跟踪卡。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些特性目前还没有在实时构建中实现，并且可能会被开发人员在未来的构建中随时引入。

一加发射器的最新更新(版本 4.1.0.191023153137.21b0828)的拆卸揭示了暗示即将到来的功能的代码字符串。新的快递跟踪卡将使用您的电话号码或快递号码来跟踪递送。值得注意的是，谷歌在 Pixel 设备主屏幕左侧的 Discover feed 中提供了类似的功能。但是，它利用从您的电子邮件中收集的信息，而不是使用您的电话号码或快递跟踪 ID。

```
 <string name="quick_page_express_title">Courier tracking</string>
<string name="quick_page_settings_express_subtitle">Tracking the courier information using the phone number or courier number</string>
<string name="quick_page_settings_preference_express">quick_page_express_card_enabled</string> 
```

到目前为止，我们还没有关于这个功能何时上线的信息。但是，由于一加已经开始研究它，我们预计它将在未来几周内推出测试版。如果你想在它进入稳定频道之前试用它，你可以通过下面的链接注册一加发射器测试程序。刚才那个 4。x 版本的 launcher APK 的 API 级别最低为 29，这意味着它们只能安装在 Android 10 设备上，目前包括 OnePlus 6/6T，一加 7/7 Pro 和一加 7T/7T Pro。

**[一加发射器测试版程序](https://play.google.com/apps/testing/net.oneplus.launcher/join?authuser=1)**

* * *

*感谢 PNF 软件为我们提供了使用许可 [JEB Decompiler](https://www.pnfsoftware.com/?aid=xdadev) ，这是一款针对 Android 应用的专业级逆向工程工具。*