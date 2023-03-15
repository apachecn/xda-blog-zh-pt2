# 一加应用程序锁功能可以很容易地被绕过

> 原文：<https://www.xda-developers.com/oneplus-app-locker-bypass/>

一加手机上的软件被称为 OxygenOS。它在现有安卓系统的基础上增加了几个漂亮的功能，而不会与你在谷歌设备上的预期相差太远。我最近开始将 OnePlus 5 作为日常驾驶，尽管存在争议，但我认为这对谷歌 Nexus 系列的粉丝来说是一个伟大的升级。话虽如此，我还是会仔细检查我收到的每一个新设备，看看我喜欢或不喜欢的每个[小方面。在深入研究 OxygenOS 设置时，我发现了一加应用程序锁功能，它可以锁定你在 pin/密码/指纹后面选择的应用程序。](https://www.xda-developers.com/oneplus-5-media-volume-steps/)

左图:隐藏在 App Locker 下的 XDA 实验室。右图:被应用锁定功能隐藏的 XDA Feed。

我通常是第三方解决方案的粉丝，因为他们不会强迫你，而且通常比第一方解决方案提供更多的功能。不过，在应用锁的情况下，我更喜欢像一加应用锁这样的集成解决方案，因为它们应该更难杀死(因此更安全)也更快(因为它们不依赖于可访问性服务或从使用统计 API 读取)。然而，我震惊地发现，OxygenOS 应用程序锁定功能可能会被**轻易绕过**。

*上述演示是在运行[oxygen OS 4 . 5 . 8](https://www.xda-developers.com/oneplus-oxygen-4-5-8-open-beta-21-12/)的 OnePlus 5 上进行的*

不可否认，我不认为这是什么重大的安全漏洞，因为这个功能主要是在你想和别人分享你的手机时使用的(希望是你已经信任的*)。如果你依赖于这个功能，那么这意味着你将把你的手机交给一个已经解锁的人，所以这是**而不是绕过你的手机的主要安全措施**如密码/pin/指纹或其他加密措施或工厂重置保护。尽管如此，缺陷就是缺陷，如果像我这样不是安全研究员的人可以发现这一点，那么任何人都可以。*

 ** * *

## 一加应用程序锁绕过解释

如上面的视频所示，我将 [XDA Feed](https://www.xda-developers.com/get-xda-feed-for-any-phone/) 应用程序隐藏在应用程序锁定功能之后。不出所料，我不输入密码就打不开这个应用。如果我尝试进入设置- >安全&指纹- >应用程序锁，系统会提示我输入密码。但当我回到主屏幕，点击我制作的一个名为“一加应用锁定器旁路”的神秘应用图标时，它会打开应用锁定器设置页面，我可以自由禁用任何现有的应用锁定。

*访问 OxygenOS 应用程序锁功能通常需要输入密码/PIN 码*

任何人都应该能够在他们运行 OxygenOS 的一加设备上复制这个过程，如果他们安装了诸如 Nova Launcher 之类的启动器(这将是一大堆人)或任何其他可以启动活动的应用程序。由于应用程序锁定功能最有可能被那些只想隐藏某些敏感应用程序(例如包含完全家庭友好图片的超级秘密画廊应用程序)同时炫耀他们的[闪亮新手机](https://www.xda-developers.com/soft-gold-oneplus-5-launch-review/)的人使用，所以大多数人不太可能会想到隐藏他们的启动器应用程序。此外，由于没有办法将软件包安装程序隐藏在应用程序锁后面，人们也可以安装一个像我自己的旁路应用程序来绕过一加应用程序锁。

如果你正在使用 Nova Launcher，并且很好奇如何做到这一点，这很简单。只需在“仪表板”下的“应用程序锁”中添加一个活动快捷方式只需点击这个快捷方式将启动应用程序锁设置，而不会询问您的密码。

*OxygenOS App Locker 设置活动*

我不太清楚为什么从第三方应用程序启动活动时，应用程序储物柜设置不要求输入密码。解决这个问题的一个方法是简单地将活动设置为[未导出的活动](https://developer.android.com/guide/topics/manifest/activity-element.html)，这样就不能从任何其他应用程序访问它。

```
 <activity android:label="@string/app_lock_label" android:name=".applocker.AppLockerSettingsActivity" android:screenOrientation="nosensor">
<intent-filter>
<action android:name="com.oneplus.security.action.APP_LOCKER"/>
<category android:name="android.intent.category.DEFAULT"/>
</intent-filter>
</activity> 
```

`com.oneplus.security`的`AndroidManifest.xml`文件(部分内容已在上面复制)显示，一加 App Locker 功能的活动确实是一个导出的活动。在活动标签上加上`android:exported=false`应该能解决这个问题，我相信。

* * *

## 一加知道，将在 OxygenOS 更新中修复

我们将此问题通知了 OxygenOS 团队，他们在以下声明中承认了这一点:

> 我们知道这个问题，我们将在即将到来的 OTA 中修复它。

如果你现在正在使用应用锁定功能，并希望确保没有人能够绕过它，我建议你在现有的应用锁定基础上添加任何启动器和浏览器应用。在我看来，这个问题并没有减损 OnePlus 5 的软件体验，但让它成为一个提醒，任何安全措施都可能存在漏洞。谢天谢地，这一次的安全漏洞相当小。*