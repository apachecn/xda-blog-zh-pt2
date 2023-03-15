# 杂货跟踪可能很快会出现在 Pixel At a Glance 小工具上

> 原文：<https://www.xda-developers.com/pixel-at-a-glance-grocery-teardown/>

谷歌为其 Pixel 智能手机保留了一些特殊的软件功能，其中之一是“一览”小工具。尽管所有 Android 设备上都有同名的小工具(由谷歌应用提供)，但 Pixel 手机上的版本有额外的集成和略有不同的外观。如果一个新的报告是准确的，它甚至可以显示杂货提货和送货的状态。

谷歌查看了最新的谷歌搜索应用更新的代码，发现了几个提到杂货店送货和取货的字符串。目前还没有太多细节，但看起来谷歌将检查你的 Gmail 收件箱，查看关于杂货提货和送货的邮件，就像它已经为即将到来的飞机旅行和其他活动数据所做的那样。然后，小部件将显示收件的预定时间，如果收件准备好了，则显示送货的预定时间，或者确认订单已经送达。

```
<string name=”ambient_settings_grocery_subtitle”>Grocery deliveries and pickups from Gmail</string>

 <string name="”assistant_grocery_pickup_pre_static”">%1$s 次装货计划在%2$s</string> 

<string name="”assistant_grocery_pickup_ready”">% 1＄s 分拣现已就绪</string>

<string name="”assistant_grocery_delivery_pre_static”">% 1＄s 交货计划在% 2＄s</string>

<string name="”assistant_grocery_delivery_completed”">% 1＄s 订单已交付</string>
```

如果 widget 的唯一数据源是 Gmail，这意味着该功能将依赖于从杂货店取件和送货提供商发送的电子邮件中收集数据。一些零售商已经停止包括所订购商品的具体细节，比如亚马逊，大概是为了防止谷歌轻易了解顾客的购买历史。然而，只要存在杂货店或提货订单的时间，小部件就可能按预期工作。

在过去的几个月里，谷歌已经推出了其他更新。早在今年 1 月，小工具[就开始为一些人显示 Nest 门铃提醒](https://www.xda-developers.com/at-a-glance-widget-nest-doorbell-alerts-rolling-out/)，同时 Nest 应用程序正常发送推送通知。谷歌也在 4 月份开始推出一款用于蓝牙设备电池和连接状态的 T2 指示器。

**来源:** [9to5Google](https://9to5google.com/2022/04/11/pixel-at-a-glance-grocery-pickup-delivery/)