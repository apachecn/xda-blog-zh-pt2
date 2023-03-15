# 谷歌地图 10.49 版准备显示门票价格

> 原文：<https://www.xda-developers.com/google-maps-v10-49-prepares-show-admission-ticket-prices/>

谷歌地图是最有用的谷歌服务之一。虽然当前的新冠肺炎·疫情可能已经减少了我们对地图的依赖，因为我们的日常通勤已经减少了，但这款应用仍然[拥有许多](https://www.xda-developers.com/new-google-maps-features-revealed-better-uber-fare-estimates-connections-public-transit-route-options-more/) [功能](https://www.xda-developers.com/google-maps-starts-showing-traffic-lights-on-android/)，这些功能允许它在简单的“地图”范围之外保持相关性[(以及](https://www.xda-developers.com/google-maps-platform-open-game-developers-pokemon-go-like-experiences/)[功能，这些功能也使它成为一款伟大的地图应用](https://www.xda-developers.com/google-maps-more-colors-details-landscapes-streets/))。谷歌再次扩大地图的范围，因为该应用程序的最新版本准备显示门票价格。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些特性目前还没有在实时构建中实现，并且可能会被开发人员在未来的构建中随时引入。

[谷歌地图](https://play.google.com/store/apps/details?id=com.google.android.apps.maps) v10.49 包括以下字符串，表明该应用程序正在努力显示票价:

```
 <string name="ADMISSION_PRICES_ACTION_BUTTON_TITLE">Tickets</string>
<string name="ADMISSION_PRICES_EXPLANATION">Adult ticket options</string>
<string name="ADMISSION_PRICES_EXPLANATION_WITH_WEBSITE">Adult ticket options from &lt;a href=\"%1$s\">%2$s&lt;/a></string>
<string name="ADMISSION_PRICES_EXPLANATION_WITH_WEBSITE_NO_TICKET_REQUIRED">From &lt;a href=\"%1$s\">%2$s&lt;/a></string>
<string name="ADMISSION_PRICES_SEE_MORE_TICKETS">See more tickets</string>
<string name="ADMISSION_PRICES_TITLE">Official tickets</string>
<string name="ADMISSION_PRICES_TOOLTIP_CONTENT">Prices are based on typical adult admission and may vary based on the specific ticket types, dates, or eligibility for other discounts.</string>
<string name="ADMISSION_PRICES_TOOLTIP_CONTENT_DESCRIPTION">Disclaimer</string> 
```

这些字符串不限制将显示这些门票价格的活动类型，因此我们认为这些信息可以在各种文化活动和旅游景点中显示。疫情无疑减少了人们为休闲和娱乐而旅行的次数，但随着各区开始开放，这一新功能有助于公布门票价格。这将是有用的，因为这个价格可能会不同于新冠肺炎之前的价格，事先获得这些信息将对规划旅行有很大的帮助。

谷歌地图更新还在停车时段功能中包含以下字符串:

```
 <string name="PARKING_SESSION_ACTIVE_INDICATOR">ACTIVE</string>
<string name="PARKING_SESSION_END_TIME_PREFIX">until %s</string>
<string name="PARKING_SESSION_EXPIRING_NOTIFICATION_TEXT">%s left on your parking session</string>
<string name="PARKING_SESSION_EXPIRING_NOTIFICATION_TITLE">Your parking will expire at %s</string> 
```

[停车位置功能](https://www.xda-developers.com/google-maps-v9-49-beta-finally-remembers-your-avoid-tolls-preference-and-saves-your-parking-location/)已经有一段时间了。很久以前也发现了[的停车会话功能，当你的会话即将结束时，它也会弹出通知。我们不确定为什么要添加这些字符串。也许谷歌计划向前发展？](https://techcrunch.com/2017/03/20/google-maps-lets-you-record-your-parking-location-time-left-at-the-meter/)

地图更新还包括谷歌助手驾驶模式的新字符串:

```
 <string name="GOOGLE_ASSISTANT_DRIVING_MODE_SETTINGS_SUMMARY">Manage driving mode</string> 
```

谷歌计划[逐步淘汰 Android Auto](https://www.xda-developers.com/android-auto-app-no-longer-supported-google-assistant-new-driving-mode/) ，取而代之的是[早在 2019 年](https://www.xda-developers.com/google-assistant-driving-mode-waze/)宣布的谷歌助手驾驶模式。2020 年已经过半，但这种驾驶模式尚未正式推出。这个字符串可能表明谷歌即将推出该功能，但该功能已经开发了这么长时间，我们真的不能肯定。

* * *