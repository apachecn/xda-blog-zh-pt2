# Gboard 测试浅色主题的自动白色导航条/深色主题的自动黑色导航条

> 原文：<https://www.xda-developers.com/gboard-white-nav-bar-light-theme-black-nav-bar-dark-theme/>

# Gboard 测试浅色主题的自动白色导航条/深色主题的自动黑色导航条

谷歌的键盘应用“Gboard”现在正在测试浅色主题的白色导航条颜色和深色主题的黑色导航条颜色。

随着谷歌 Pixel 2 和谷歌 Pixel 2 XL 的发布，对该设备最早的抱怨之一是[显示器烧屏](https://www.xda-developers.com/google-pixel-2-xl-display-burn-issues/)(事实证明这是暂时的图像残留。)为了解决这些抱怨，谷歌发布了一个更新，让系统在几秒钟后将导航栏变暗。在 API level 27 (Android 8.1 Oreo)中，谷歌引入了一个 [windowLightNavigationBar](https://developer.android.com/reference/android/R.attr#windowLightNavigationBar) 常量，因此应用程序可以请求系统显示导航按钮颜色，与通过 [navigationBarColor](https://developer.android.com/reference/android/R.attr.html#navigationBarColor) 常量设置的浅色导航栏背景一致。有了这些新功能，由于[减轻了静态导航栏引起的有机发光二极管显示屏](https://www.xda-developers.com/google-pixel-2-xl-warranty-color-mode/)的差异老化，暂时的图像残留问题在很大程度上得到了解决。自 Android 8.1 Oreo 发布以来的几个月里，很少有应用程序更新为支持“白色导航条”，但似乎 Gboard 可能会在不久的将来成为其中之一。

该应用程序的最新版本 7.4 目前正在谷歌 Play 商店上推出。由 XDA 知名开发者[quinny 899](https://forum.xda-developers.com/member.php?u=3563640)([Mighty Quinn Apps](http://quinny898.co.uk/)的 Kieron Quinn)发现，这个版本的应用程序正在测试一个功能，当用户选择一个浅色的 Gboard 主题时，它会使用上述 API 显示一个白色的导航栏。另一方面，当用户选择深色的 Gboard 主题时，会显示标准的黑色导航栏。相比之下，Gboard 目前总是显示一个黑色的导航栏，无论你在应用程序的设置中选择什么主题。

左侧:(新行为)白色导航条，带有浅色 Gboard 主题。中间:(新行为)黑色导航条，深色 Gboard 主题。右:(标准)黑色导航条与轻 Gboard 主题。

这项功能对大多数用户来说还不可用。一旦它推出，它会很好地与新的自动黑暗主题，是启用时，电池节省(这也是在测试中。)

WhatsApp、Facebook Messenger 等应用的[智能回复也尚未上线，但我们会让你了解谷歌键盘应用中任何正在开发的功能的最新进展。您可以从下面的 Play Store 下载最新版本的键盘应用程序。](https://www.xda-developers.com/gboard-smart-replies-whatsapp-facebook-allo-snapchat/)