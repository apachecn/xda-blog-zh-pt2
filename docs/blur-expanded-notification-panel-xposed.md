# 用 x 曝光模糊您的扩展通知面板

> 原文：<https://www.xda-developers.com/blur-expanded-notification-panel-xposed/>

# 用 x 曝光模糊您的扩展通知面板

用这个简单的 Xposed 模块给你的扩展通知面板添加模糊背景透明度。

与 Windows Phone 或 iOS 不同，Android 在各种设备上的外观截然不同。HTC Sense、三星 TouchWiz 或鲜为人知的 Emotion UI 等 OEM 皮肤看起来与准系统 AOSP 完全不同。干净的 Android 可能因为它的简单而拥有很多粉丝，但是并不是每个人都喜欢默认的 UI。

几乎每一个操作系统的缺陷都可以通过源代码修改或者使用由 XDA 资深公认开发者 [rovo89](http://forum.xda-developers.com/member.php?u=4419114) 和他的《犯罪公认贡献者》合伙人[钨文迪](http://forum.xda-developers.com/member.php?u=4322181)开发的 Xposed 框架来修复。如果你想要一个好看的扩展通知背景，XDA 认可开发商 [serajr](http://forum.xda-developers.com/member.php?u=3989065) 准备了一些可能会感兴趣的东西。

模糊系统 UI 是一个暴露的模块，它模糊了展开的通知面板的背景。在你当前的 ROM 上应用它后，你会看到一个部分透明的背景，这看起来比许多 ROM 中使用的标准纯色背景好得多。这个模块可以让你配置一些东西，如位图比例和模糊半径，这样你就可以相对容易地得到预期的结果。

该模块目前仅适用于智能手机，但在不久的将来可能会增加平板电脑兼容性。据报道，它可以在多种 rom 上运行——包括皮肤的和 AOSP 衍生的。你可以通过访问[模糊系统 UI 模块线程](http://forum.xda-developers.com/xposed/modules/xposed-blurred-ui-v1-0-16-07-2014-t2818273)找到模块并高斯模糊你的通知面板。