# Android 10 启动器端口为 Android 9 带来了新的手势动画

> 原文：<https://www.xda-developers.com/android-10-launcher-port-gesture-animations-android-9/>

Android 10 为手势导航带来了[重大变化](https://www.xda-developers.com/google-releases-stable-android-10-for-pixel-smartphones/)，其中许多是受欢迎的改进，但有些不是那么大。例如，虽然回家或在应用程序之间切换的新过渡动画比 Android 9 Pie 上的更流畅，但新的背部手势[可以说是一种回归](https://www.xda-developers.com/google-android-q-gesture-mess/)，因为它干扰了许多应用程序的侧边栏。如果你被困在 Android 9 Pie 上，想要尝试一些新的手势，你可以[闪存一个定制的 ROM](https://www.xda-developers.com/android-10-custom-rom-xiaomi-poco-f1-mi-6-8-redmi-note-5/) (如果有的话)或者你可以尝试这个发布在我们论坛上的修改过的 Android 10 启动器。

XDA 资深成员 [paphonb](https://forum.xda-developers.com/member.php?u=6018897) 最出名的是将 Pixel Launcher 移植到非谷歌设备上，并致力于 [Lawnchair](https://www.xda-developers.com/lawnchair-2-0-2130-desktop-lock-app-categorization-adaptive-brightness-theming/) 。今天早些时候，他在我们的论坛上为他的最新创作创建了一个主题:一个修改过的 Android 10 启动器，可以在任何基于 Magisk 的 Android 9 Pie 设备上运行。这个启动器端口带来了新的向上滑动回家和最近的应用程序切换过渡动画，但它没有带来新的手势栏或向后滑动手势。这是因为手势栏和后退手势被编码到 SystemUI 中，而不是启动器中，所以制作一个包含这两个特性的端口要复杂得多，因为它需要进行特定于设备的修改。这里有一个视频显示了在启用此模式的 Android 9 Pie 上滑动手势的样子:

安装这个模块的一个缺点是它取代了你的默认启动器，无论是新星启动器，动作启动器，Lawnchair 等等。修改后的启动器基于 AOSP Android 10 Launcher3，因此在功能方面相当简单。

为了安装这个 mod，你需要 root 权限，因为你必须使用 [QuickSwitch Magisk 模块](https://forum.xda-developers.com/apps/magisk/module-quickswitch-universal-quickstep-t3884797)使 paphonb 的启动器端口成为最近应用程序屏幕的处理程序。只需安装调制启动器 APK，安装 QuickSwitch，使调制启动器成为 QuickSwitch 中的默认启动器，打开调制启动器的设置页面，启用标志(“ENABLE_GESTURES”和“FULL_GESTURE_MODE”))我确认这在我的[华硕 ZenFone 6](https://forum.xda-developers.com/zenfone-6-2019) 上运行，运行基于 Android 9 Pie 的 [OmniROM](https://forum.xda-developers.com/zenfone-6-2019/development/rom-omnirom-forzenfone6-2019-t3959209) 。

[**Android 9+设备的 Android 10 启动器端口【Root】**](https://forum.xda-developers.com/android/apps-games/root-android-10-launcher-gestures-t3966591)

作为一个额外的好处，这个端口还带来了向下滑动手势，以下拉通知抽屉。Google [在稳定的 Android 10 中移除了这个手势](https://www.xda-developers.com/pixel-launcher-android-q-swipe-pull-down-notifications/),所以那些安装这个 mod 的 Android Pie 用户将比收到最新 Android 操作系统更新的用户多一个好处！