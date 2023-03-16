# 谷歌 Pixel 4 可能有一个类似苹果 True Tone 的显示功能

> 原文：<https://www.xda-developers.com/google-pixel-4-automatic-white-balance-true-tone/>

2016 年，苹果推出了采用苹果 True Tone 显示技术的 iPad Pro，可以根据环境亮度动态调整白平衡。这是一个简单但非常有效的功能，可以增强所有亮度级别的阅读体验。在安卓设备制造商中，只有[一加](https://www.xda-developers.com/oneplus-6-display-analysis-compared-oneplus-5t/)和最近的 [LG](https://www.xda-developers.com/lg-g8-thinq-display-review-lgs-focus-lies-elsewhere/) 试图模仿 True Tone，尽管只有后者成功做到了。现在，我们发现了谷歌正在研究这种显示功能的证据，它可能会出现在即将推出的谷歌 Pixel 4 系列上。

XDA 显示器分析师迪伦·拉加(Dylan Raga)表示，苹果设备中 TrueTone 的基础来自“人类视觉系统中的色度适应概念，即使在不同颜色的灯光下观看，物体也能呈现相同的颜色。这适用于反射表面，如任何现实世界的物体，但智能手机屏幕是发射的。在较暖的光线下观看时，屏幕经常显得过于蓝。这是因为显示器的感知白平衡会随着周围环境照明的颜色而变化。为了实现相同的视觉适应特性，显示器应该将其色温向环境照明的颜色改变，使得看起来屏幕表面被环境照明的颜色照亮。这使得无论环境照明的颜色如何，屏幕看起来都是一致的。”如果在谷歌 Pixel 4 和 Pixel 4 XL 上实现，这是它最有可能的工作方式。

包含这个特性的证据可以追溯到我们在一月份获得的[泄露版本](https://www.xda-developers.com/android-q-dark-theme-desktop-mode-permission-revamp/)。在那个版本中，我们发现 Android Q 有一个占位符设置来切换“显示白平衡”。当时甚至今天，它仍然什么都不做。经过一番挖掘，我们找到了原因:它需要一个全新的传感器，现有的谷歌 Pixel 智能手机上没有。[这听起来与我们今天早些时候刚刚发布的另一个可能的 Pixel 4 功能类似](https://www.xda-developers.com/google-pixel-4-aware-music-control-gestures-android-q/)。

在 Android Q 的设置应用中，有一个名为`DisplayWhiteBalancePreferenceController`的新类。在允许上述切换显示在显示设置中之前，它检查布尔框架值`config_displayWhiteBalanceAvailable`是否设置为真。它还要求像素上的当前颜色模式不设置为“2”，这对应于像素 2 上的“饱和”和像素 3 上的“自适应”。根据 Dylan Raga 的说法，该功能“不适用于饱和色配置文件，因为该配置文件没有进行正确的颜色管理和校准”，这意味着它“很可能没有校准数据来正确执行必要的颜色空间转换。”除了 preference controller 类，Settings 或 SystemUI 中没有其他关于这个新特性的内容。

然而，在框架内有多个整数、整数数组、字符串数组，最后还有一个字符串，它确认这个特性是用于基于亮度动态调整白平衡的，并且它需要一个新的传感器。以下整数、整数数组和字符串数组确认“`displayWhiteBalance`”要素基于环境颜色温度和亮度级别设置了不同的白平衡值。

### 在框架中显示白平衡资源-res

```
 <array name="config_displayWhiteBalanceAmbientColorTemperatures" />
<array name="config_displayWhiteBalanceBaseThresholds">
<item>0.0</item>
</array>
<array name="config_displayWhiteBalanceDecreaseThresholds">
<item>0.1</item>
</array>
<array name="config_displayWhiteBalanceDisplayColorTemperatures" />
<string-array name="config_displayWhiteBalanceDisplayNominalWhite">
<item>0.950456</item>
<item>1.000000</item>
<item>1.089058</item>
</string-array>
<string-array name="config_displayWhiteBalanceDisplayPrimaries">
<item>0.412315</item>
<item>0.212600</item>
<item>0.019327</item>
<item>0.357600</item>
<item>0.715200</item>
<item>0.119200</item>
<item>0.180500</item>
<item>0.072200</item>
<item>0.950633</item>
<item>0.950456</item>
<item>1.000000</item>
<item>1.089058</item>
</string-array>
<array name="config_displayWhiteBalanceIncreaseThresholds">
<item>0.1</item>
</array>

<integer name="config_displayWhiteBalanceBrightnessFilterHorizon">10000</integer>
<integer name="config_displayWhiteBalanceBrightnessSensorRate">250</integer>
<integer name="config_displayWhiteBalanceColorTemperatureDefault">6500</integer>
<integer name="config_displayWhiteBalanceColorTemperatureFilterHorizon">10000</integer>
<integer name="config_displayWhiteBalanceColorTemperatureMax">8000</integer>
<integer name="config_displayWhiteBalanceColorTemperatureMin">4000</integer>
<integer name="config_displayWhiteBalanceColorTemperatureSensorRate">250</integer>
<integer name="config_displayWhiteBalanceDecreaseDebounce">5000</integer>
<integer name="config_displayWhiteBalanceIncreaseDebounce">5000</integer> 
```

然而，更能说明问题的是以下字符串，它证实了该功能需要一个新的谷歌传感器:

```
 <string name="config_displayWhiteBalanceColorTemperatureSensorName">com.google.sensor.color</string> 
```

现有的谷歌 Pixel 智能手机上都没有这种传感器，因此它可能是谷歌 Pixel 4 系列的新品。此外，我们还看到了其他具有“com.google.sensor”命名方案的谷歌传感器，如 Active Edge ( `com.google.sensor.elmyra`)和 Pixel Stand ( `com.google.sensor.dreamliner`)。因此，很有可能这个“`com.google.sensor.color`指的是能够测量颜色数据的环境光传感器。

谷歌 Pixel 3 中的 [TMD2725](https://ams.com/tmd2725) 似乎没有能力，但也许 Pixel 4 中使用的任何传感器都将是。LG G8 ThinQ 上的 ToF 传感器与一个能够检测颜色的环境光传感器配对，Dylan 说这是环境光传感器供应商正在开始做的事情。也许谷歌 Pixel 4 会包含这样一个包——毕竟，我们期待 Pixel 4 支持[安全面部识别](https://www.xda-developers.com/android-q-face-id-rumor/)。