# 三月份的像素功能下降可能包括黑暗模式调度等

> 原文：<https://www.xda-developers.com/google-pixel-feature-drop-march-include-dark-mode-scheduling-quick-access-wallet/>

回到去年 12 月，谷歌[推出了一种新方法](https://www.xda-developers.com/google-pixel-feature-drop-post-snap-portrait-mode-auto-call-screen/)来为其 Pixel 系列带来功能更新。该公司没有在新功能准备好的时候推出新功能，而是采用了一种更系统的方法，并宣布将每三个月推出一个新的“功能下降”，与[安卓安全补丁](https://www.xda-developers.com/tag/android-security-updates/)一起推出。第一个功能下降是随着 12 月的安全补丁一起发布的，它引入了一些新功能，包括快照后人像模式、自动呼叫筛选等。根据发布时间表，谷歌预计将在下个月推出第二款 Pixel 功能。虽然该公司尚未发布任何关于下一款 drop 将包含哪些功能的信息，但 Pixel Tips 应用程序最新更新的拆解揭示了下一款 drop 将会推出的所有功能。

我们的朋友在*9 到 5 谷歌*进行了有问题的拆卸，以下是他们的发现:

## 黑暗模式调度

黑暗模式调度首次出现在 Android 10 的早期测试版中，与新的全系统黑暗模式一起出现。该功能允许用户计划在日落或自定义时间自动激活黑暗模式。然而，[功能在稳定版发布之前就被弃用了](https://www.xda-developers.com/android-q-ama-summary/),因为该公司认为它可能会在应用程序正在使用时突然重启，从而对用户体验产生负面影响。然后，回到去年 12 月，谷歌问题跟踪器上的一条评论显示，该公司仍在开发该功能，这表明该功能[可能会在 Android 11](https://www.xda-developers.com/dark-mode-scheduling-could-be-coming-in-android-11/) 中卷土重来。

```
 <string name=”tips_darktheme2_feature_description”>Dark theme turns on automatically at sunset</string>
<string name=”tips_darktheme2_feature_name”>Schedule Dark theme</string>
<string name=”tips_darktheme2_link”>Dark theme settings</string>
<string name=”tips_darktheme2_media_description”>Video about Dark theme. To add Dark theme to Quick Settings, swipe down twice from the top of your screen and tap Edit.</string>
<string name=”tips_darktheme2_summary”>”Dark theme uses a black background to keep your battery alive longer. It also changes the appearance of your Google apps, like Gmail and Photos.\nAdd Dark theme to your Quick Settings to turn it on or off anytime. Touch and hold to set up a schedule.”</string>
<string name=”tips_darktheme2_title”>Take it easy on your eyes and your battery with Dark theme</string> 
```

这个功能在最近发布的 Android 11 开发者预览版中再次被发现，这让我们相信这是 Android 11 独有的功能。然而，根据前述拆卸中发现的新代码字符串，该功能可能会在即将到来的运行 Android 10 的 Pixel 设备的 Pixel 功能下降中发布。该代码提到，该功能将在黑暗主题设置中可用，用户也可以通过长按黑暗主题快速设置磁贴来设置时间表。

## 卡片和通行证

Android 10 早期测试版中发现的另一个功能[也将随着下一个功能下降而出现在 Pixel 设备上。这项名为卡片&通行证的功能将允许用户快速访问他们保存在 Google Play 电源菜单中的卡片。与黑暗模式调度非常相似，这个功能也在第一个 Android 11 开发者预览版](https://www.xda-developers.com/android-q-google-pay-power-menu/)中被[发现，这让我们相信它将与 Android 的下一个迭代一起推出。](https://www.xda-developers.com/android-10-11-developer-preview-quick-access-wallet-google-pay/)

```
 <string name=”tips_powerkey_features_link”>Cards &amp; passes settings</string>
<string name=”tips_powerkey_features_feature_name”>Quick access to wallet</string>
<string name=”tips_powerkey_features_summary”>”Press &amp; hold the Power button to access payment methods, passes, and emergency info.
– Payment methods in Google Pay: If your phone is locked, youâ
– Boarding passes and tickets: Available from the lock screen before a flight or event.
– Emergency info: To help in an emergency, people with access to your phone can view your medical info and dial your emergency contacts without unlocking your phone.”</string> 
```

然而，9to5Google 发现的代码串表明，它可能会在 3 月份的功能下降中发布。该代码清楚地强调了该特性在发布时将如何工作，并为该特性提供了几个不同的用例。例如，卡&通行证功能将允许用户从锁定屏幕上的电源菜单快速访问他们保存的卡、机票或活动门票以及紧急信息。它还澄清说，即使用户将能够访问锁定屏幕上的信息，他们也必须解锁手机才能完成支付。

## 播放/暂停动作感应手势

第一个 Android 11 开发者预览版还强调了 Pixel 4 系列的[新运动感应手势，允许用户甚至不用触摸他们的设备就可以播放/暂停音乐。Pixel Tips teardown 也突出显示了与该功能相关的代码，这表明它可能会为 Android 10 上的 Pixel 4 设备发布。](https://www.xda-developers.com/android-11-new-motion-sense-gesture-pause-music-pixel-4/)

```
 <string name=”tips_oslo_music_feature_description”>Use Quick Gestures to pause or skip songs</string>
<string name=”tips_oslo_music_summary”>”Pause or resume music by tapping the air above the phone.
Skip songs by swiping left or right above the phone.”</string> 
```

根据代码，该功能将允许用户简单地点击手机上方的空气，以暂停或恢复音乐播放。它还突出了 Pixel 4 设备上已经可用的跳过音轨手势。

## 汽车碰撞检测

最后，拆卸还表明，Android 11 的个人安全应用程序也可能在下一次 Pixel drop 中进入旧 Pixel 手机。不知道的是，该应用预装在 Android 11 开发者预览版 1 上，并包括一个汽车碰撞检测功能，此前只有 Pixel 4 系列才有。

```
 <string name=”tips_carcrash_title”>Get help calling emergency services after a car crash</string>
<string name=”tips_carcrash_feature_description”>With car crash detection, your phone can call emergency services</string> 
```

虽然我们[设法在旧的 Pixel 设备上下载应用](https://www.xda-developers.com/personal-safety-app-android-11-google-pixel-4-sideload-enable-car-crash-detection/)并启用汽车碰撞检测功能，但很高兴看到谷歌正式将其引入更多的 Pixel 设备。根据代码，该应用程序将在检测到汽车碰撞时自动呼叫紧急服务，这在必要时真的可以派上用场。

Pixel 设备的新功能看起来确实很有趣，但值得注意的是，这些功能是在拆卸过程中发现的，谷歌可能会在下一次 Pixel drop 中跳过其中的一些功能。谷歌也很有可能在这些功能发布前对其进行一些重大修改。

* * *

**Via:[9 to 5 Google](https://9to5google.com/2020/02/27/pixel-tips-march-feature-drop-dark-mode-schedule/)**