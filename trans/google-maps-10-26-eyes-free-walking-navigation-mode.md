# [更新:推出]谷歌地图 10.26 暗示了一种新的“裸眼”步行导航模式

> 原文：<https://www.xda-developers.com/google-maps-10-26-eyes-free-walking-navigation-mode/>

**更新(美国东部时间 10/10/19 @下午 2:05):**谷歌在谷歌地图中为有视觉障碍的人推出“详细的语音指导”。

过去几周，Android 版谷歌地图增加了一些有用的新功能。8 月初，该公司增加了一个新的“[实时视图](https://www.xda-developers.com/google-maps-ar-navigation-timeline-sharing-features/)”导航模式，在增强现实中叠加行走方向。当月晚些时候，谷歌宣布，你很快就可以在导航时将多种交通方式结合在一起[。这个月，我们发现谷歌悄悄增加了一个](https://www.xda-developers.com/google-maps-mixed-route-directions-ridesharing-biking/)[街景图层](https://www.xda-developers.com/google-maps-android-street-view-layer/)，今天早些时候，谷歌告诉其当地导游[隐姓埋名模式](https://www.xda-developers.com/google-maps-google-search-incognito-mode/)现在可以在安卓应用中测试。

我们检查了今天在封闭测试中推出的最新版本的 APK 地图——版本 10 . 26 . 67——我们发现了另一个目前正在开发中的有用导航功能的证据。它在内部被称为“裸眼模式”，当你用它来步行导航时，它将减少你看手机的频率。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些特性目前还没有在实时构建中实现，并且可能会被开发人员在未来的构建中随时引入。

10.26.67 版本中包含了详细描述这种模式的新字符串。字符串显示，新模式将“在步行导航期间[添加]更详细的语音指导。”启用这个功能可能会让谷歌地图应用程序给你详细的步行导航指示，这样你就不必看着你的手机来查看你下一步需要走到哪里。如果你不小心离开了计划好的路线，应用程序会告诉你，你会被重新安排路线。

```
 <string name="EYES_FREE_EXTRA_DETAIL_SETTING">Hear more frequent and detailed audio announcements during walking navigation</string>
<string name="EYES_FREE_MODE_ONE_DIRECTION_BANNER_TEXT">Tap to enable detailed voice navigation</string>
<string name="EYES_FREE_MODE_ONE_DIRECTION_CONFIRMATION_TEXT">This option adds more detailed voice guidance during walking navigation. You can turn it off later in Google Maps settings, under Navigation. Would you like to enable it?</string>
<string name="EYES_FREE_MODE_ONE_DIRECTION_CONFIRMATION_TITLE">Want more detailed voice navigation?</string>
<string name="EYES_FREE_MODE_REROUTE_NOTIFICATION">It looks like you've left the route, so I'll re-route you.</string>
<string name="EYES_FREE_OPTIONS_TITLE">Detailed voice guidance</string> 
```

一旦该功能推出，你应该会看到一个横幅宣传它一旦你开始步行导航。该功能可以通过进入设置>导航并切换底部“步行选项”下的模式来禁用。该设置似乎还不适用于本地指南，但我们会跟踪这一新功能的进展，并在它上线时通知您。我们最近[还发现了证据](https://www.xda-developers.com/google-maps-report-speed-camera-disabled-vehicle-lane-closure-object-on-road/)表明谷歌地图将为残疾车辆、车道封闭和道路上的物体添加事件报告，但我们还没有看到证据表明这种做法已经推广到任何人。鉴于谷歌地图应用在导航方面的主导地位，我们预计他们将在向全球数百万用户推出这些功能之前大力测试这些功能。

*感谢 PNF 软件为我们提供了使用许可 [JEB Decompiler](https://www.pnfsoftware.com/?aid=xdadev) ，这是一款针对 Android 应用的专业级逆向工程工具。*

* * *

## 更新:推出

谷歌现在正在谷歌地图中推出详细的语音导航。该功能是为有视觉障碍的人设计的。这项功能今天将在 Android 和 iOS 上推出。你可以进入“设置”>“导航”>“详细语音指导”(位于“步行选项”下)来启用它)这在美国只适用于英语，在日本只适用于日语。

**来源:[谷歌](https://www.blog.google/products/maps/better-maps-for-people-with-vision-impairments/)**