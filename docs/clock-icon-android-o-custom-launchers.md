# Android O 引入了一个动画时钟图标，很快就可以在定制发布中使用

> 原文：<https://www.xda-developers.com/clock-icon-android-o-custom-launchers/>

谷歌可能即将在 Android O 中推出一项新功能——备受推崇的 Action Launcher 的作者克里斯·莱西(Chris Lacy)发现，时钟应用程序将在启动器中有一个动画图标。

据开发者称，Pixel Launcher 将很快支持谷歌时钟应用程序的动画时钟图标。几年前，谷歌日历也增加了类似的功能，但这次的更新明显有点不同。时钟图标要求的间隔要短得多，Google 找到了实现的方法。

克里斯·莱西(Chris Lacy)在谷歌时钟应用的`AndroidManifest.xml`文件中发现了以下几行。

### AndroidManifest.xml

```
 <meta-data 
  android:name="com.google.android.apps.nexuslauncher.LEVEL_PER_TICK_ICON_ROUND" 
  android:resource="@mipmap/launcher_clock"/>
<meta-data 
  android:name="com.google.android.apps.nexuslauncher.HOUR_LAYER_INDEX 
  android:value="1"/>
<meta-data 
  android:name="com.google.android.apps.nexuslauncher.MINUTE_LAYER_INDEX"
  android:value="2"/>
<meta-data 
  android:name="com.google.android.apps.nexuslauncher.SECOND_LAYER_INDEX"
  android:value="3"/>
<meta-data 
  android:name="com.google.android.apps.nexuslauncher.DEFAULT_HOUR" 
  android:value="10"/>
<meta-data 
  android:name="com.google.android.apps.nexuslauncher.DEFAULT_MINUTE" 
  android:value="10"/>
<meta-data 
  android:name="com.google.android.apps.nexuslauncher.DEFAULT_SECOND" 
  android:value="30"/> 
```

APK 包含以下图像:

当然，这些元素组合在一起就成了一个动画时钟图标！从已经发布的版本 25.0 开始，此功能将在 Action Launcher 中实现和提供。此外，动画时钟将作为一个独立的小工具。

动画时钟图标在移动世界中并不新鲜。这一功能在苹果 iOS 的早期版本中可用，谷歌需要几年时间才能将这一功能引入 Android。不是什么大事情，但是离让安卓更一致更美观又近了一步。此外，动画钟面应该很快就会找到第三方时钟应用程序。

希望目前大多数可用的发射器都有这个特性。如果你现在渴望在你的设备上拥有它，去 Google Play 并获得[动作启动器](https://play.google.com/store/apps/details?id=com.actionlauncher.playstore)。

* * *

[**来源:布莱格**](http://theblerg.net/post/2017/6/24/android-o-will-see-the-introduction-of-an-animated-clock-icon-in-launchers)