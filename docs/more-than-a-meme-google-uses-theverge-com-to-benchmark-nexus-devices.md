# 不仅仅是一个迷因:谷歌用 TheVerge.com 来测试 Nexus 设备

> 原文：<https://www.xda-developers.com/more-than-a-meme-google-uses-theverge-com-to-benchmark-nexus-devices/>

在 AOSP 四处挖掘是对 Android 有新发现的一个好方法，这次我们遇到了一些相当有趣的事情。一段时间以来，[用户报告称，](https://blog.lmorchard.com/2015/07/22/the-verge-web-sucks/)TheVerge.com[科技网站](http://www.theverge.com/)在移动设备上运行缓慢。

根据我的经验，他们的网站性能随着时间的推移已经有所提高，这是值得肯定的。另外，并不是说其他网站(包括我们自己的网站)没有我们可以努力解决的问题，但尽管如此，我发现在其官方的工作负载基准测试中，谷歌决定在他们的测试中使用 Verge 非常有趣。

* * *

**Android 工作负载自动化**

[工作负载自动化](https://github.com/ARM-software/workload-automation) (WA)是由 [ARM](https://www.arm.com/) 开发的一个框架，用于通过执行一套许多可重复的工作负载来收集 Android 设备上的性能数据。谷歌通过进行许多这样的工作负载测试和收集电力使用情况的总结来对他们的设备进行性能基准测试，然后他们将这些数据导入到电子表格中，以查看他们的优化如何随着时间的推移提高了性能。该公司挑选测试套件中包含哪些应用，但一般来说，他们仅限于大多数流行的谷歌应用。这是它如何工作的要点，但我们将展示来自源代码的证据，并更详细地描述测试套件，以便您可以更好地了解 Google 为测量性能所做的自动化测试。

在 AOSP，有一个专用于工作负载自动化测试的目录。用于测试的应用程序在 [defs.sh](https://android.googlesource.com/platform/system/extras/+/master/tests/workloads/defs.sh) 中定义，通常分为两类:默认、预装的谷歌应用程序或第三方网络浏览器。一个基准测试应用程序脱颖而出，我假设它是指基于虚幻引擎 4 的基准测试。

```

gmailActivity='com.google.android.gm/com.google.android.gm.ConversationListActivityGmail'
clockActivity='com.google.android.deskclock/com.android.deskclock.DeskClock'
hangoutsActivity='com.google.android.talk/com.google.android.talk.SigningInActivity'
chromeActivity='com.android.chrome/_not_used'
contactsActivity='com.google.android.contacts/com.android.contacts.activities.PeopleActivity'
youtubeActivity='com.google.android.youtube/com.google.android.apps.youtube.app.WatchWhileActivity'
cameraActivity='com.google.android.GoogleCamera/com.android.camera.CameraActivity'
playActivity='com.android.vending/com.google.android.finsky.activities.MainActivity'
feedlyActivity='com.devhd.feedly/com.devhd.feedly.Main'
photosActivity='com.google.android.apps.photos/com.google.android.apps.photos.home.HomeActivity'
mapsActivity='com.google.android.apps.maps/com.google.android.maps.MapsActivity'
calendarActivity='com.google.android.calendar/com.android.calendar.AllInOneActivity'
earthActivity='com.google.earth/com.google.earth.EarthActivity'
calculatorActivity='com.google.android.calculator/com.android.calculator2.Calculator'
calculatorLActivity='com.android.calculator2/com.android.calculator2.Calculator'
sheetsActivity='com.google.android.apps.docs.editors.sheets/com.google.android.apps.docs.app.NewMainProxyActivity'
docsActivity='com.google.android.apps.docs.editors.docs/com.google.android.apps.docs.app.NewMainProxyActivity'
operaActivity='com.opera.mini.native/com.opera.mini.android.Browser'
firefoxActivity='org.mozilla.firefox/org.mozilla.firefox.App'
suntempleActivity='com.BrueComputing.SunTemple/com.epicgames.ue4.GameActivity'
homeActivity='com.google.android.googlequicksearchbox/com.google.android.launcher.GEL' 
```

这些活动通过 ADB 命令行启动，使用以下 [Systrace](https://developer.android.com/studio/profile/systrace-commandline.html) 选项来衡量应用性能:

```
 dflttracecategories="gfx input view am rs power sched freq idle load memreclaim" 
```

特别是 Chrome 应用程序启动时带有一个加载边缘的标志:

至于为什么测试似乎对 *volantis* (Nexus 9)有所不同，我不是很确定。无论如何，至于这个 Chrome-activity-with-The-Verge 实际上通过了哪些测试，我们可以通过查看工作负载自动化测试的源代码来确定。

* * *

**测试套件**

首先，有一个 **[systemapps.sh](https://android.googlesource.com/platform/system/extras/+/master/tests/workloads/recentfling.sh)** 测试，谷歌声明它是这样工作的:

接下来是 [**recentfling.sh**](https://android.googlesource.com/platform/system/extras/+/master/tests/workloads/recentfling.sh) 测试，工作原理是这样的:

然后还有 **[chromefling.sh](https://android.googlesource.com/platform/system/extras/+/master/tests/workloads/chromefling.sh) ，**测试 Chrome 的性能相当简单:

工作负载自动化套件中另一个有趣的测试是 [**youtube.sh**](https://android.googlesource.com/platform/system/extras/+/master/tests/workloads/youtube.sh) 性能测试，它测量 UI jank

```

iterations=10
app=youtube
searchText="last week tonight with john oliver: online harassment"
vidMinutes=15 
```

最后，这些测试中的每一个都用于通过在一定时间内循环来测量真实世界的用电量，如 [**pwrtest.sh**](https://android.googlesource.com/platform/system/extras/+/master/tests/workloads/pwrtest.sh) 中所定义:

然后，谷歌可以使用 [**pwrsummary.sh**](https://android.googlesource.com/platform/system/extras/+/master/tests/workloads/pwrsummary.sh) 收集这些数据，并将它们导入电子表格:

这些都是相当常见的真实世界的 UI 性能测试，与你在我们自己的测试中看到的类型没有什么不同。打开 Chrome 时加载 Verge 主页的变化似乎是最近才发生的，因为去年谷歌在这些测试中只会在 Chrome 中打开一个新标签。然而，[2015 年 5 月 28 日](https://android.googlesource.com/platform/system/extras/+/4d31f7f%5E!/)的一项改变是在测试 Chrome 时引入了 Verge 的使用。有趣的是，谷歌在执行工作负载自动化测试时使用了所有地方的边缘，请记住，这并不意味着边缘是 web 性能的最大障碍。

事实上，远非如此，由于越来越多的广告扩散以弥补广告拦截器的增加，许多其他网页表现平平。事实上，考虑到普通谷歌员工对技术的精通程度，以及许多爱好者对 Verge 网页性能的内部玩笑，使用 Verge 的决定很可能只是出于方便。