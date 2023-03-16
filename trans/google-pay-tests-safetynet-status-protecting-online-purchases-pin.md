# Google Pay 测试显示安全网状态和网上购物的 pin 码

> 原文：<https://www.xda-developers.com/google-pay-tests-safetynet-status-protecting-online-purchases-pin/>

Google Pay 正在慢慢成为钱包的完全替代品，因为它增加了对更多支付形式、更多银行和更多卡类型的支持。为了让金融机构满意并保护用户的财务数据，Google Pay 应用程序使用 SafetyNet 认证 API 来验证该应用程序没有在装有被篡改软件的设备上运行。当然， [Magisk root](https://forum.xda-developers.com/apps/magisk) 被设计为绕过这些检查，但是 SafetyNet API 检查不是静态的，用户可能会意外安装 mod 或编辑文件，导致 API 报告证明失败。由于 Google Pay 检查 SNet 状态的方式，用户可能不知道他们的设备不再通过 SNet，直到他们实际进行支付。然而，这可能会在不久的将来发生变化，因为 Google Pay 应用程序可能会在主页上添加内置的 SafetyNet 状态检查器。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些特性目前还没有在实时构建中实现，并且可能会被开发人员在未来的构建中随时引入。

**安全网检查器**

早在 7 月，我们[在 Google Pay 应用中发现了一个新的认证检查通知字符串](https://www.xda-developers.com/google-pay-safetynet-checker-pixel-4-face-authentication/)。这个特性现在在最新版本中完全可用。一旦它上线，如果你的设备由于任何原因未能通过认证 API 检查，你会在主页标签中看到一条消息，告诉你你的手机“不能进行非接触式支付”如果你点击“检查软件”，你会收到一条更详细的信息，告诉你为什么不能使用 Google Pay。例如，我在我的根 Pixel 2 XL 上禁用了 MagiskHide，并收到了以下消息:

当这项功能上线时，你可以事先在 Google Pay 应用程序中检查你设备的 SNet 状态，这样当你无法进行非接触式支付时，你就不会在柜台感到惊讶。Google Play 上有很多第三方应用可以做到这一点，更不用说 Magisk Manager 自己内置的 SafetyNet checker 了，但这只是检查你的设备是否通过的又一种方式。

**PIN 保护网上购物**

这个下一个功能是由简·满春·王最先发现的，它将允许你使用你的谷歌账户 PIN 码为你的每一次网上购物切换 PIN 码保护。我可以显示这个设置，但即使在输入我的 Google 帐户 PIN 后，我也无法通过 Google Pay 应用程序保持这个设置。

像往常一样，在 Google Play 的最新版本中，这些功能还不能供公众使用。一旦这些功能上线，我们会通知您。

* * *

*感谢 PNF 软件为我们提供了使用许可 [JEB Decompiler](https://www.pnfsoftware.com/?aid=xdadev) ，这是一款针对 Android 应用的专业级逆向工程工具。*