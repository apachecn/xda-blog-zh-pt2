# 谷歌地图 10.30 准备为电动汽车增加新功能

> 原文：<https://www.xda-developers.com/google-maps-10-30-electric-vehicle-charging-payments-compatible-plugs/>

去年年底，谷歌更新了地图，显示附近的电动汽车充电站。“地图”将向您显示有关电动汽车充电站所在企业的信息、可用端口的类型和数量、充电速度以及其他信息，包括评论、照片等。充电站信息来自 Tesla、Chargepoint、SemaConnect、EVgo、Blink、Chargemaster、Pod Point 和 Chargefox。虽然这些服务为谷歌地图提供了大量的电动汽车充电站，以显示在地图上，但司机仍然需要使用单独的应用程序来支付充电费用。然而，这可能会在不久的将来发生变化，因为谷歌地图 10.30 Android 版增加了一些字符串，表明它将支持直接从应用程序中支付。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些特性目前还没有在实时构建中实现，并且可能会被开发人员在未来的构建中随时引入。

**付费充电**

10.30 版本中新增了以下两个字符串，它们是与电动汽车相关的更大字符串集的一部分，描述了向用户的电动汽车配置文件添加支付方式。

```
 <string name="EV_PROFILE_VIEW_NETWORKS_HEADING">Your payment methods</string>
<string name="EV_PROFILE_ADD_NETWORKS">Add payment methods</string> 
```

**电动车简介，寻找兼容插头**

如前所述，谷歌地图正准备让你用你的电动车信息更新你的个人资料。你可以添加你的插头，这样当你在应用程序中搜索时，你只会看到兼容的充电站。

```
 <string name="EV_PROFILE_ADD_CONNECTORS_V2">Add plugs</string>
<string name="EV_PROFILE_EDIT">Edit</string>
<string name="EV_PROFILE_EDIT_CONNECTORS_TITLE_V2">Your plugs</string>
<string name="EV_PROFILE_LOADING_FAILED_MESSAGE">Please check your internet connection</string>
<string name="EV_PROFILE_LOADING_FAILED_RETRY_BUTTON_TEXT">Try again</string>
<string name="EV_PROFILE_LOADING_FAILED_TITLE">Maps is offline</string>
<string name="EV_PROFILE_OVERVIEW_TITLE">Electric vehicle settings</string>
<string name="EV_PROFILE_PIVOT_TOOLTIP_TEXT_V2">Showing compatible charging stations</string>
<string name="EV_PROFILE_PROMO_CARD_ACTION_TEXT_V2">Add plugs</string>
<string name="EV_PROFILE_PROMO_CARD_DESCRIPTION_V3">To only see charging stations that work with your EV, add your plugs</string>
<string name="EV_PROFILE_PROMO_CARD_DISMISS_TEXT_V2">No thanks</string>
<string name="EV_PROFILE_PROMO_CARD_TITLE_TEXT_V3">Get compatible charging stations</string>
<string name="EV_PROFILE_SEE_LESS">See less</string>
<string name="EV_PROFILE_SEE_MORE">See more</string>
<string name="EV_PROFILE_SETTINGS_TITLE_V2">Electric vehicle settings</string>
<string name="EV_PROFILE_VIEW_CONNECTORS_HEADING_V2">Your plugs</string>
<string name="RESTRICTION_EV_PROFILE_ANY_PLUGS">Any plugs</string>
<string name="RESTRICTION_EV_PROFILE_V2">EV plugs</string>
<string name="RESTRICTION_EV_PROFILE_YOUR_PLUGS">Your plugs</string>
<string name="CAR_EVCP_IN_SEARCH_APPLIED_TEXT">Showing compatible charging stations</string>
<string name="CAR_EVCP_IN_SEARCH_NOT_APPLIED_TEXT">Showing all results. Some charging stations may not match your plugs.</string> 
```

这些功能尚未在 Android 的谷歌地图应用中推出。不过，我们可能会在几天或几周内看到谷歌的声明。谷歌地图上一次更新与电动汽车相关的新功能是在 4 月的[，当时他们增加了充电端口的实时可用性。随着新电动汽车的出现，地图应用早就应该有新功能了。](https://www.blog.google/products/maps/finding-place-charge-your-ev-easy-google-maps/)

* * *

*感谢 PNF 软件为我们提供了使用许可 [JEB Decompiler](https://www.pnfsoftware.com/?aid=xdadev) ，这是一款针对 Android 应用的专业级逆向工程工具。*