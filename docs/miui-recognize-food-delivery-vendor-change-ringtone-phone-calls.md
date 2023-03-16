# MIUI 准备自动识别和更改送餐供应商的电话铃声

> 原文：<https://www.xda-developers.com/miui-recognize-food-delivery-vendor-change-ringtone-phone-calls/>

小米的 MIUI 继续得到该公司定期和积极的开发。与其他大型原始设备制造商不同，小米让发烧友用户有机会在这些功能进入稳定版本之前，通过测试版试用其中的一些功能。例如，以前的 MIUI 测试版展示了一些功能，如附加的[屏幕投射功能，黑暗模式调度，新的 MiLanPro 字体](https://www.xda-developers.com/miui-9819-screen-cast-features-dark-mode-scheduling-font/)，一个[键盘下的快捷栏，双 Wi-Fi 加速，](https://www.xda-developers.com/miui-985-dual-clock-under-keyboard-shortcut-bar-dual-wlan-acceleration/)和[更多的](https://www.xda-developers.com/tag/miui/)。这些测试版还提供了一些正在开发的功能，所以我们可以根据经验猜测小米未来会怎么样。针对中国地区的最新 MIUI 10 Beta 9.8.20 表明，小米正在致力于自动识别来自服务供应商的来电，然后用单独的铃声拨打电话，以便于识别。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些功能目前在 live build 中没有实现，可能会在未来的 build 中随时被小米拉出来。

在 MIUI 10 Beta 9.8.20 的设置应用中发现了以下字符串:

```
 <string name="intelligent_recognition_item_summary">Identify incoming calls made by service vendors (e.g. food delivery) and use separate ringtones for them</string>

<string name="intelligent_recognition_item_title">Identify services</string> 
```

虽然这些字符串是在中国 MIUI 测试版中发现的，但我们相信该功能最终会进入印度。过去，小米与印度的各种第三方服务供应商合作，对 MIUI 进行本地化，使其对印度观众更有用，而像这样的功能将非常适合印度。像 Zomato、Swiggy 和 Uber Eats 这样的食品配送服务在印度非常庞大，尤其是在城市地区，这要归功于它们的深度折扣模式和服务发现方法。许多顾客，从工作人员到参加派对的青少年，都依赖这些服务在瞬间将食物送到他们手中。MIUI 与这些服务的更深层次的集成将为最终用户带来好处。

MIUI 如何知道这些服务供应商何时会打电话来，尤其是每次送货主管都在变化的时候？我们对此的最佳猜测是，小米*可能*设想了这样一种场景，这些服务供应商将向小米共享其送货主管的手机号码。MIUI 已经包含了本地化的应用程序使用跟踪功能，因此这个*可以*用于确定客户何时期待特定服务的交付。然后，可以识别来自具有该连接服务的递送主管的呼叫，并且可以应用不同的铃声来提醒用户关于呼叫者和呼叫目的的信息。无可否认，这是一种推测，所以当特性完全开发出来时，功能可能会完全不同。

* * *

*感谢 PNF 软件为我们提供了使用许可 [JEB Decompiler](https://www.pnfsoftware.com/?aid=xdadev) ，这是一款针对 Android 应用的专业级逆向工程工具。*