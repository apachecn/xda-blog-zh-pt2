# Razer Phone 使用索尼的 Overlay Manager 服务主题引擎

> 原文：<https://www.xda-developers.com/razer-phone-theme-engine-oms/>

本周早些时候，Razer Inc .——一家以面向游戏玩家的计算机硬件产品而闻名的公司——凭借 [Razer Phone](https://www.xda-developers.com/razer-phone-120hz-snapdragon-835/) 进入了移动智能手机的世界。它充满了对 Android 智能手机爱好者很有吸引力的硬件，如 8gb 内存和 4,000mAh 电池的高通骁龙 835 SoC，但它的 5.7 英寸 1440p IGZO 液晶屏和高达 120Hz 的可变帧率是其定义的硬件功能。最重要的是，这款手机运行了 Android 7.1 牛轧糖的近库存版本，并添加了一些 Razer 特有的功能，如 Game Booster 和主题商店。

Razer 手机上的主题商店可以定制系统元素，如通知设置和快速设置，但也可以定制应用程序，如拨号器、计算器、时钟和其他预装应用程序，如 Nova Launcher。例如，Razer 主题商店中的一个主题将上述应用程序和系统 UI 元素变成了棕色，以纪念 Razer 去年的愚人节玩笑—[Project breakwinner](https://www2.razerzone.com/breadwinner?utm_source=Razer_Social_Media&utm_medium=smlink_US_launch&utm_campaign=RazerBreadwinner)。

它是怎么做到的？我们现在已经了解到，驱动 Razer 手机的主题引擎是基于索尼开源覆盖管理器服务(OMS)的主题引擎(T1)，与 T2 流行底层主题引擎(T3)和安卓 8.0 奥利奥主题引擎(T5)背后的主题引擎相同。Razer 手机背后的软件团队精心挑选了让 OMS 在 Android Nougat 上运行所必需的提交，因此理论上任何为 OMS rom 构建的底层主题都应该适用于 Razer 手机。

不幸的是，只有一个问题。目前**只有系统签名的主题才可以被应用**，所以希望使用现有底层主题来设计新 Razer 手机的用户将会很不走运。希望为手机制作主题的主题商店将不得不等待，因为目前主题商店还没有向第三方主题开放。也许包含的股票主题对你们大多数人来说已经足够了，但是经常光顾我们论坛的发烧友很少对默认提供的内容感到满意。

*推荐阅读:[为什么 App 更新有时会打破底层主题](https://www.xda-developers.com/why-app-updates-sometimes-break-substratum-themes/)*

为了保护 Razer，**第三方主题可能会有问题**,尤其是当应用程序更新时——导致主题覆盖和应用程序的新资源之间不匹配。这款手机甚至还没有到达消费者手中，所以我们可以看到 Razer 在未来向第三方主题开放他们的主题商店。

* * *

***你对雷蛇手机有什么看法？请在下面的评论中告诉我们！***