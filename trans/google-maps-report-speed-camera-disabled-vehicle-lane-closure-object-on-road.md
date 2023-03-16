# Android 版谷歌地图可能增加 4 种新的事故报告类型

> 原文：<https://www.xda-developers.com/google-maps-report-speed-camera-disabled-vehicle-lane-closure-object-on-road/>

**更新(美国东部时间 10/17/19 @下午 1:20):**谷歌地图现在可以让你报告施工、残疾车辆、车道封闭和行驶中的物体。

数百万司机使用谷歌地图，因此它作为一个众包交通和事故报告工具非常有用。Maps 去年首次推出了事件报告功能，不过 Waze 早就有了。谷歌在去年 11 月推出了[碰撞和速度陷阱报告](https://www.xda-developers.com/google-maps-crash-speed-trap-reporting/)，几个月前增加了[交通减速报告](https://www.xda-developers.com/google-maps-traffic-slowdown-reporting/)。今天早些时候， [*AndroidPolice*](https://www.androidpolice.com/2019/09/05/google-maps-lets-you-report-road-constructions/) 注意到，道路建设报告正在向一些用户推出，我们也可以独立证实这一点。然而，我们也有证据表明，谷歌正在测试至少 3 种其他类型的事件报告:残疾车辆、车道封闭和道路上的物体。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些特性目前还没有在实时构建中实现，并且可能会被开发人员在未来的构建中随时引入。

如果你打开谷歌地图应用程序，进入导航模式，点击被气泡包围的+图标，你会看到一个底部的表格，其中有报告路上事故的选项。对于包括我自己在内的大多数用户来说，你只能选择报告道路上的撞车、超速或减速。

 <picture>![Google Maps reports](img/b18d84558de2b033699ead1b820d674f.png)</picture> 

Most users can currently only report crashes, speed traps, and slowdowns.

我们获得了一个未发布的谷歌地图版本 10.25.24，它包含了新的字符串，表明这个底部表单将填充选项，以报告残疾车辆，车道封闭或路上的物体。APK 也有报告速度相机的字符串，但这些字符串在过去几个月的地图应用程序的公开发布中已经存在。报告高速摄像机的功能还没有出现在地图应用程序中，所以我们认为这也值得一提。

在版本 10.25.24 中增加了:

```
 <string name="REPORT_INCIDENT_PROMPT_LANE_CLOSURE">Lane closure</string>
<string name="REPORT_INCIDENT_PROMPT_LANE_CLOSURE_REPORTED">Lane closure added to the map</string>
<string name="REPORT_INCIDENT_PROMPT_LANE_CLOSURE_REPORTING">Adding lane closure to the map</string>
<string name="REPORT_INCIDENT_PROMPT_OBJECT_ON_ROAD">Object on road</string>
<string name="REPORT_INCIDENT_PROMPT_OBJECT_ON_ROAD_REPORTED">Object on road added to the map</string>
<string name="REPORT_INCIDENT_PROMPT_OBJECT_ON_ROAD_REPORTING">Adding object on road to the map</string>
<string name="REPORT_INCIDENT_PROMPT_DISABLED_VEHICLE">Disabled vehicle</string>
<string name="REPORT_INCIDENT_PROMPT_DISABLED_VEHICLE_REPORTED">Disabled vehicle added to the map</string>
<string name="REPORT_INCIDENT_PROMPT_DISABLED_VEHICLE_REPORTING">Adding disabled vehicle to the map</string> 
```

已经在过去几个月的版本中出现:

```
 <string name="REPORT_INCIDENT_PROMPT_CAMERA">Speed camera</string>
<string name="REPORT_INCIDENT_PROMPT_CAMERA_REPORTED">Speed camera added to the map</string>
<string name="REPORT_INCIDENT_PROMPT_CAMERA_REPORTING">Adding speed camera to the map</string> 
```

我真的希望谷歌地图能尽快添加这些事件报告。在休斯顿或洛杉矶这样的城市，开车可能是一件苦差事，在那里，你路线的一个意外变化可能会增加一个多小时的通勤时间。路上的意外物体如果被碾过，可能会损坏你的轮胎，或者如果司机没有安全避开它们，可能会导致事故。残疾车辆报告将给那些想知道是什么在某一天造成如此大的交通流量的司机带来一些安心(至少对我来说是这样的)。)最后，知道测速摄像头在哪里会让你对当前速度更加谨慎，这样你就有希望更安全地驾驶。

这些事件报告都没有在谷歌地图的当前版本中发布，在我们获得的未发布版本中也没有。当他们开始向用户展示时，无论是在全球还是在 A/B 测试中，我们都会让你们知道。

*感谢 PNF 软件为我们提供了使用许可 [JEB Decompiler](https://www.pnfsoftware.com/?aid=xdadev) ，这是一款针对 Android 应用的专业级逆向工程工具。*

* * *

## 更新:推出

谷歌地图是上个月在 APK 的一次拆卸中发现的，现在它允许你报告施工、残疾车辆、车道封闭和行驶中的物体。以前，可以报告撞车、超速和交通减速。这使得可以报告的事件总数达到 7 起。要报告事故，只需点击+号，然后点击“添加报告”

**来源:[谷歌](https://blog.google/products/maps/new-ways-report-driving-incidents-google-maps/)**