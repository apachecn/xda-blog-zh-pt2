# 谷歌地图可能很快就会进入黑暗模式，并能够显示公交线路

> 原文：<https://www.xda-developers.com/google-maps-10270-starring-transit-lines-dark-mode/>

谷歌地图是谷歌最好的软件产品之一，由于其易用性和相对准确性，它在全球范围内被广泛采用。这款应用多年来一直在稳步改进，以使我们的通勤和生活变得更容易，以至于许多人一走出家门就启动地图已经成为一种习惯。在努力开发新功能，如[“裸眼”步行导航模式](https://www.xda-developers.com/google-maps-10-26-eyes-free-walking-navigation-mode/)、[隐姓埋名模式](https://www.xda-developers.com/google-maps-google-search-incognito-mode/) ( [推出](https://www.xda-developers.com/privacy-features-coming-google-maps-youtube-chrome/))和[更容易的异常报告](https://www.xda-developers.com/google-maps-report-speed-camera-disabled-vehicle-lane-closure-object-on-road/)之后，谷歌地图现在似乎正在努力开发黑暗模式和启动运输线的能力。

## 深色模式

黑暗模式最近风靡一时，谷歌地图可能很快就会赶上这一趋势。目前，主地图 UI 主要使用白色背景，并采用[深色主题仅用于导航](https://www.xda-developers.com/google-maps-manual-dark-mode-navigation/)，这可能不适合每个人的口味。正如 *[AndroidPolice](https://www.androidpolice.com/2019/10/09/dark-mode-signs-show-up-in-google-maps/#1)* 所发现的，谷歌正在通过其官方 Instagram 页面上的一个帖子取笑地图的黑暗模式:

* * *

## 运输线特征

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些特性目前还没有在实时构建中实现，并且可能会被开发人员在未来的构建中随时引入。

Google Maps v10.27.0 包含以下字符串:

### 谷歌地图中的新字符串

```
 <string name="TRANSIT_SPACE_CANNOT_STAR_LINE_IN_INCOGNITO_TOAST">You can't star lines while Incognito mode is on.</string>
<string name="TRANSIT_SPACE_CANNOT_STAR_STATION_IN_INCOGNITO_TOAST">You can't star stations while Incognito mode is on.</string>
<string name="TRANSIT_SPACE_CLEAR_FILTER_BUTTON">Clear filters</string>
<string name="TRANSIT_SPACE_DEPART_FROM_HERE_TEXT">Depart from here</string>
<string name="TRANSIT_SPACE_LINES_TAB_HEADER">Lines</string>
<string name="TRANSIT_SPACE_LINE_COLLAPSE_CARD_BUTTON_TEXT">Show fewer %s %s details</string>
<string name="TRANSIT_SPACE_LINE_COLLAPSE_CARD_BUTTON_TEXT_WITHOUT_LINE_NAME">Show less</string>
<string name="TRANSIT_SPACE_LINE_COLLAPSE_CARD_BUTTON_TEXT_WITH_LINE_NAME_UNKNOWN_VEHICLE_TYPE">Show fewer %s details</string>
<string name="TRANSIT_SPACE_LINE_EXPAND_CARD_BUTTON_TEXT">Show more %s %s details</string>
<string name="TRANSIT_SPACE_LINE_EXPAND_CARD_BUTTON_TEXT_WITHOUT_LINE_NAME">Show more line details</string>
<string name="TRANSIT_SPACE_LINE_EXPAND_CARD_BUTTON_TEXT_WITH_LINE_NAME_UNKNOWN_VEHICLE_TYPE">Show more %s details</string>
<string name="TRANSIT_SPACE_LINE_NAME_VEHICLE_TYPE_TEXT">%1$s %2$s</string>
<string name="TRANSIT_SPACE_LINE_SEARCH_BUTTON_TEXT">See lines here</string>
<string name="TRANSIT_SPACE_LINE_STARRED_TOAST">Line starred &amp; pinned to top</string>
<string name="TRANSIT_SPACE_LINE_STARRED_TOAST_ACTION_TEXT">View</string>
<string name="TRANSIT_SPACE_LINE_STAR_BUTTON_TEXT">Star the %s %s</string>
<string name="TRANSIT_SPACE_LINE_STAR_BUTTON_TEXT_WITHOUT_LINE_NAME">Star the line</string>
<string name="TRANSIT_SPACE_LINE_STAR_BUTTON_TEXT_WITH_LINE_NAME_UNKNOWN_VEHICLE_TYPE">Star the %s</string>
<string name="TRANSIT_SPACE_LINE_STAR_BUTTON_TOOLTIP_TEXT">Tap to save</string>
<string name="TRANSIT_SPACE_LINE_STATION_TAB_ACTIVATED_STATUS_TEXT">%s tab selected</string>
<string name="TRANSIT_SPACE_LINE_STATION_TAB_INACTIVATED_STATUS_TEXT">%s tab not selected</string>
<string name="TRANSIT_SPACE_LINE_UNSTAR_BUTTON_TEXT">Unstar the %s %s</string>
<string name="TRANSIT_SPACE_LINE_UNSTAR_BUTTON_TEXT_WITHOUT_LINE_NAME">Unstar the line</string>
<string name="TRANSIT_SPACE_LINE_UNSTAR_BUTTON_TEXT_WITH_LINE_NAME_UNKNOWN_VEHICLE_TYPE">Unstar the %s</string>
<string name="TRANSIT_SPACE_MODE_FILTER_BUS_OPTION">Bus</string>
<string name="TRANSIT_SPACE_MODE_FILTER_FERRY_OPTION">Ferry</string>
<string name="TRANSIT_SPACE_MODE_FILTER_RAIL_OPTION">Rail</string>
<string name="TRANSIT_SPACE_MODE_FILTER_SUBWAY_OPTION">Subway / Metro</string>
<string name="TRANSIT_SPACE_MODE_FILTER_TRAIN_OPTION">Train</string>
<string name="TRANSIT_SPACE_MODE_FILTER_TRAM_LIGHT_RAIL_OPTION">Tram / Light rail</string>
<string name="TRANSIT_SPACE_NEARBY_LINES_LIST_HEADER">Lines in this area</string>
<string name="TRANSIT_SPACE_NEARBY_STATIONS_LIST_HEADER">Stations in this area</string>
<string name="TRANSIT_SPACE_NO_CONNECTION_ERROR_MESSAGE">Can't connect to Maps</string>
<string name="TRANSIT_SPACE_NO_CONNECTION_ERROR_SUBTITLE_MESSAGE">Check your internet connection, or try again in a few minutes</string>
<string name="TRANSIT_SPACE_NO_CONNECTION_TRY_AGAIN_BUTTON">Try again</string>
<string name="TRANSIT_SPACE_NO_DEPARTURES_NEARBY_ERROR_MESSAGE">No upcoming departures in this area</string>
<string name="TRANSIT_SPACE_NO_NEARBY_LINES_ERROR_MESSAGE">No nearby lines found</string>
<string name="TRANSIT_SPACE_NO_NEARBY_STATIONS_ERROR_MESSAGE">No nearby stations found</string>
<string name="TRANSIT_SPACE_NO_STARRED_LINES_ERROR_MESSAGE">No starred lines</string>
<string name="TRANSIT_SPACE_NO_STARRED_LINES_ERROR_SUBTITLE">Star the lines you use most to see them here</string>
<string name="TRANSIT_SPACE_NO_STARRED_LINES_WHEN_INCOGNITO_ERROR_MESSAGE">Incognito mode is on</string>
<string name="TRANSIT_SPACE_NO_STARRED_LINES_WHEN_INCOGNITO_ERROR_SUBTITLE">Your starred lines aren't available when Incognito mode is on</string>
<string name="TRANSIT_SPACE_NO_STARRED_LINES_WHEN_SIGNED_OUT_ERROR_MESSAGE">To see your starred lines, sign in</string>
<string name="TRANSIT_SPACE_NO_STARRED_STATIONS_ERROR_MESSAGE">No starred stations</string>
<string name="TRANSIT_SPACE_NO_STARRED_STATIONS_ERROR_SUBTITLE">Star the stations you use most to see them here</string>
<string name="TRANSIT_SPACE_NO_STARRED_STATIONS_WHEN_INCOGNITO_ERROR_MESSAGE">Incognito mode is on</string>
<string name="TRANSIT_SPACE_NO_STARRED_STATIONS_WHEN_INCOGNITO_ERROR_SUBTITLE">Your starred stations aren't available when Incognito mode is on</string>
<string name="TRANSIT_SPACE_NO_STARRED_STATIONS_WHEN_SIGNED_OUT_ERROR_MESSAGE">To see your starred stations, sign in</string>
<string name="TRANSIT_SPACE_NO_UPCOMING_DEPARTURES_TEXT">No upcoming departures</string>
<string name="TRANSIT_SPACE_ONBOARDING_CARD_DISMISS_BUTTON_DESCRIPTION">Dismiss</string>
<string name="TRANSIT_SPACE_ONBOARDING_CARD_HEADING">Quickly check bus and train times</string>
<string name="TRANSIT_SPACE_ONBOARDING_CARD_SUBTITLE">Star lines to see them first</string>
<string name="TRANSIT_SPACE_SEE_MORE_DEPARTURES_TEXT">More departures</string>
<string name="TRANSIT_SPACE_SIDE_MENU_NAME">Your transit</string>
<string name="TRANSIT_SPACE_SIGN_IN_BUTTON_TEXT">Sign in</string>
<string name="TRANSIT_SPACE_SIGN_IN_TO_STAR_A_TRANSIT_LINE_PROMPT">To see your starred lines, sign in</string>
<string name="TRANSIT_SPACE_SINGLE_LETTER_LINE_NAME_VEHICLE_TYPE_TEXT">the %1$s %2$s</string>
<string name="TRANSIT_SPACE_STARRED_VIEW_TOGGLE">Starred</string>
<string name="TRANSIT_SPACE_STATIONS_SEARCH_BUTTON_TEXT">See stations here</string>
<string name="TRANSIT_SPACE_STATIONS_TAB_HEADER">Stations</string>
<string name="TRANSIT_SPACE_STATION_COLLAPSE_CARD_BUTTON">Show fewer %s details</string>
<string name="TRANSIT_SPACE_STATION_EXPAND_CARD_BUTTON">Show more %s details</string>
<string name="TRANSIT_SPACE_STATION_STARRED_TOAST">Station starred &amp; pinned to top</string>
<string name="TRANSIT_SPACE_STATION_STARRED_TOAST_ACTION_TEXT">View</string>
<string name="TRANSIT_SPACE_STATION_STAR_BUTTON_TEXT">Star %s</string>
<string name="TRANSIT_SPACE_STATION_UNSTAR_BUTTON_TEXT">Unstar %s</string>
<string name="TRANSIT_SPACE_TURN_OFF_INCOGNITO_BUTTON_TEXT">Turn off Incognito</string>
<string name="TRANSIT_SPACE_UNABLE_TO_LOAD_LINE_DETAILS_TEXT">Can't load details for this line, try again later</string>
<string name="TRANSIT_SPACE_WIDER_SEARCH_BUTTON_TEXT">Search a wider area</string>
<string name="TRANSIT_SPACE_WIDER_SEARCH_CARD_TEXT">Don't see your line?</string>
<string name="TRANSIT_SPACE_WIDER_SEARCH_STATION_CARD_TEXT">Don't see your station?</string> 
```

在这种情况下，标记一条线是指将经常使用的旅行媒介，尤其是经常使用的旅行路径标记为收藏。用户将能够查看附近的公共交通路线，包括公共汽车、渡轮、铁路/火车/地铁/地铁和电车/轻轨。例如，将一条路线标记为您的最爱可以让您快速查看公共汽车和火车的时间，以及您旅行时该路线上即将到达的车站/站点。我们认为这一功能对于喜欢经常使用特定公共交通路线的用户来说非常有用。

我们不知道该功能何时上线。

* * *

*感谢 PNF 软件为我们提供了使用许可 [JEB Decompiler](https://www.pnfsoftware.com/?aid=xdadev) ，这是一款针对 Android 应用的专业级逆向工程工具。*