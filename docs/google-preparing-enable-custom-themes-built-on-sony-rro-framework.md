# 谷歌可能最终启用基于索尼 RRO 框架的定制主题

> 原文：<https://www.xda-developers.com/google-preparing-enable-custom-themes-built-on-sony-rro-framework/>

如果你还不知道，谷歌在昨天的 I/O 活动中发布了第二个 Android O 开发者预览版(Android O DP2)。我们已经[深入研究了到目前为止我们发现的所有新东西](https://www.xda-developers.com/heres-everything-new-in-android-o-developer-preview-2/)，但是有一件关于 DP2 的事情困扰着我。每个[收到测试版更新或者手动刷新](https://www.xda-developers.com/android-o-beta-program-is-live/)新图片的人都很快在快速设置中遇到了[完全不同的用户界面](https://www.xda-developers.com/heres-everything-new-in-android-o-developer-preview-2/#QuickSettings)。谷歌究竟为什么决定改变主题？经过更多的测试和挖掘，我得出了一个结论。不管出于什么原因，谷歌已经决定将其[“倒置”主题](https://www.xda-developers.com/android-o-adds-inverted-light-theme-to-display-options/)设为默认主题；也许当该公司正在测试一个基于索尼运行时资源覆盖的定制主题方案时，他们无法在 Android O Beta 发布前及时获得默认的像素主题。

*Android O 开发者预览版 2 中的默认系统主题*

鉴于谷歌在 Android 6.0 棉花糖中实现了对 RRO 的支持，Android O 的主题化框架基于索尼的 RRO，这对一些人来说似乎是显而易见的，尽管这需要你有一个根设备。然而，由于 Android O 的源代码还没有发布，暗示 Android O 中的这个系统主题实际上是 RRO 纯属猜测。这就是为什么我们[最初对这个神秘设定的报道](https://www.xda-developers.com/android-o-adds-inverted-light-theme-to-display-options/)，以及[其他网站做的报道](http://www.androidpolice.com/2017/03/21/android-o-feature-spotlight-looks-like-android-may-getting-native-support-themes/)，都没有把这个联系起来。但是有几个证据将这一功能与主题化框架联系起来，我们认为这应该最终表明 **Android O 的设备主题是基于 RRO** 的。有了 RRO 的支持，这可能**最终会为我们一直在等待的**非 RRO 用户提供主题化解决方案。

* * *

## 什么是运行时资源覆盖(RRO)？

RRO 是索尼开发者创建的主题框架，为索尼的 Xperia 主题提供动力。RRO 的美妙之处在于，它允许您替换应用程序资源，而不必修改应用程序的源代码。这是通过使用覆盖层实现的，覆盖层包含自己的资源字符串，用于在应用程序加载时替换覆盖的应用程序的资源。

对于那些看到“RRO”并想到“层”的人来说，你已经很接近了。Layers 是索尼 RRO 的一个略微修改的版本，但在基础级别上，它的工作方式非常相似。RRO/Layers 将主题 apk“安装”到/system/vendor/overlay。在启动时，包管理器读取这些 apk，验证它们，然后使用 *[idmap](https://github.com/android/platform_frameworks_base/blob/master/cmds/idmap/idmap.cpp)* 将其链接到系统资源表中。你可以阅读由 [SykoPompos](https://plus.google.com/+SykoPompos/posts/VeQgiWgiktt) (现已废弃)[图层管理器](https://play.google.com/store/apps/details?id=com.lovejoy777.rroandlayersmanager&hl=en)应用程序的开发者撰写的更全面的常见问题。

*弃用的图层管理器应用截图*

* * *

**推荐阅读:** [主题化简史:从 OEM 主题到 RRO 层](https://www.xda-developers.com/a-brief-history-of-theming-from-oem-themes-to-rro-layers/)

* * *

当然，Android 定制 ROM 社区中很少有人还在使用基于 RRO 的主题引擎。大多数已经转移到另一个主题引擎，如 [Substratum](https://www.xda-developers.com/layers-manager-is-being-deprecated-in-favor-of-substratum/) ，这是一个基于叠加管理器服务(OMS)的层的进化。(CyanogenMod 主题引擎(CMTE)是另一个流行的主题框架，尽管[它的未来仍然悬而未决](https://www.xda-developers.com/exclusive-dead-cyanogenmod-theme-engine-cmte-not-coming-back-lineageos-replacement/)。)然而，即使你没有使用 OMS 提交的定制 ROM，[底层主题引擎应用](https://play.google.com/store/apps/details?id=projekt.substratum&hl=en)仍然支持使用“底层遗产”主题的能力，这些主题只是 RRO/Layers 主题。也正因为如此，用户开始搞清楚 Android O 的设备主题和 RRO 是一回事。

* * *

## Google 最终通过 RRO 引入了主题化

在一篇 *AndroidPolice* 文章的[评论部分，](https://disqus.com/home/discussion/androidpolice/android_o_feature_spotlight_quick_settings_are_now_grayscale_get_some_small_cosmetic_tweaks/#comment-3311099015) XDA 知名开发者 [Maxr1998](https://forum.xda-developers.com/member.php?u=5222551) 发布了一张截图，声称 Substratum Legacy 主题出现在谷歌的设备主题选择器中。

左边可以看到 Android O 开发者预览版 1 上 Maxr1998 安装的叠加 apk 列表。在右边，你可以看到 Android O 开发者预览版 2 中的两个主题选择。[之前在 Android O DP1](https://www.xda-developers.com/android-o-adds-inverted-light-theme-to-display-options/) 中，两个选项是“像素”和“反转”,其中“像素”设置为默认，而“反转”类似于 O DP2 中默认的灰度外观。

但是仔细看看 O DP2 中默认主题的名字。叫做“android.auto_generated_rro。”一个非常奇怪的名字，但名字中包含“RRO”让我第一次相信这确实是索尼的 RRO。

然后我想，如果这真的是 RRO，我还能在哪里找到证据呢？这些想法引导我检查/system/vendor/overlay，正如所料，其中确实有两个 APK 文件:framework-RES _ _ auto _ generated _ rro . apk 和 PixelThemeOverlay.apk

这两者都与显示设置中的主题名称相匹配。奇怪的是，当你在显示设置中选择像素主题时，它不起作用。我不是开发 RRO 主题的专家，所以我不能说为什么 Pixel 主题不起作用，尽管通过对这两个应用程序进行 APK 分解，可以清楚地看到这些确实是覆盖应用程序。

**PixelThemeOverlay.apk APK 拆卸**

[标签][标签标题="AndroidManifest.xml"]

```
 <?xml version="1.0" encoding="utf-8" standalone="no"?>
<manifest xmlns:andro package="com.google.android.theme.pixel" platformBuildVersionCode="25" platformBuildVersionName="O">
<overlay android:priority="1" android:targetPackage="android"/>
<application android:hasCode="false" android:label="@string/pixel_overlay_pixel"/>
</manifest> 
```

[/tab][tab title ="strings.xml"]

```
 <?xml version="1.0" encoding="utf-8"?>
<resources>
<string name="pixel_overlay_pixel">Pixel</string>
</resources> 
```

[/tab][tab title ="colors.xml"]

```
 <?xml version="1.0" encoding="utf-8"?>
<resources>
<color name="user_icon_1">#ff5e97f6</color>
<color name="user_icon_2">#ff5c6bc0</color>
<color name="user_icon_3">#ff26a69a</color>
<color name="user_icon_4">#ffec407a</color>
<color name="user_icon_5">#ff33ac71</color>
<color name="user_icon_6">#ff8bc34a</color>
<color name="user_icon_7">#ffff9800</color>
<color name="user_icon_8">#ffff7043</color>
<color name="system_error">#ffea4335</color>
<color name="primary_device_default_dark">#ff2d2d2d</color>
<color name="primary_device_default_settings">#ff2d2d2d</color>
<color name="primary_dark_device_default_dark">#ff242424</color>
<color name="primary_dark_device_default_settings">#ff242424</color>
<color name="secondary_device_default_settings">#ff3a3a3a</color>
<color name="tertiary_device_default_settings">#ff616161</color>
<color name="quaternary_device_default_settings">#ff9e9e9e</color>
<color name="accent_device_default_700">#ff3367d6</color>
<color name="accent_device_default_light">#ff4285f4</color>
<color name="accent_device_default_dark">#ff5e97f6</color>
<color name="accent_device_default_50">#ffe8f0fe</color>
</resources> 
```

[/tab]

[/tabs]

如果你浏览索尼提供的 RRO 文档，很明显这应该是一个 RRO 主题。在 androidManifest 文件中，覆盖行指示该覆盖以 framework-res.apk 文件(“Android”)为目标，它的优先级为“1”，这是它可以被赋予的最高优先级。

另一方面，在 framework-RES _ _ auto _ generated _ rro . apk 文件中有一个看起来与 AndroidManifest.xml 文件相似的文件，但是还有许多其他与主题无关的字符串。但这很容易解释，因为这个 RRO 主题基本上是 Google Pixel 的 framework-res.apk 的精简版本，我认为这是真的，因为\res\values\bools.xml 有一行`<bool name="config_useRoundIcon">true</bool>`，我从我们论坛上的一个帖子中知道，用户[需要设置](https://forum.xda-developers.com/android/apps-games/guide-enable-pixel-launcher-round-icon-t3536267)，以便[在系统范围内启用圆形图标支持](https://www.xda-developers.com/psa-android-7-1-circular-icon-support-is-determined-by-the-oem/)。

* * *

## 结论

我的测试人员还不能在 O DP2 中实现 root 访问，以尝试运行底层遗留/RRO 主题，但根据我自己和 Maxr1998 的发现，可以有把握地说 **Google 可能最终准备将 RRO 主题化带给大众**。

当然，不能保证这个特性不会在以后的 Android O 版本中被删除。有可能谷歌认为 RRO 没有按照他们想要的方式工作，并放弃了这个功能。然而，鉴于 RRO 在索尼和我们自己的开发社区中的广泛历史，我们中的许多人已经熟悉索尼运行时资源覆盖的伟大之处。由于已经有大量兼容 RRO 的主题可用，如果谷歌决定允许我们安装自定义主题，他们将打开闸门，让用户享受已经广泛存在的主题市场。

* * *

*专题图片演职员表:[SonyDevWorld](https://www.youtube.com/watch?v=it0WEuVUp7o)*