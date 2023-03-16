# 谷歌可能会让你在 Android 11 中调整画中画窗口的大小

> 原文：<https://www.xda-developers.com/android-11-resize-picture-in-picture-pip-windows/>

Android 8.0 奥利奥[将](https://www.xda-developers.com/google-announces-android-o-developer-preview-1-available-for-supported-devices/)画中画模式引入 Android 智能手机。该功能允许您在使用其他应用程序时在一个小的浮动窗口中观看视频。它对导航也很有用，因此您可以回复信息或在互联网上查找信息，而不会错过您路线上的下一站。随着智能手机变得越来越大，特别是随着可折叠设备的推出，画中画窗口一直保持相同的大小。不过，在 Android 11 中，谷歌可能会为用户引入一种调整画中画窗口大小的方式。

*Android 11 中的画中画(PIP)模式。我打开了一个 YouTube 视频，然后做了 home 手势(点击 home 键也可以)在 PIP 窗口中打开视频。*

OEM 可以设置默认边缘插入(PIP 窗口第一次出现时离屏幕边缘有多远)、默认屏幕宽度和高度百分比、默认纵横比、默认重力(PIP 窗口开始显示的角落)和吸附行为(用户放开后 PIP 窗口移动的位置)。然而，大多数 OEM 厂商并不触及 AOSP 中的[默认值，他们通常不会修改或扩展 PIP 窗口的功能。由于 AOSP 没有为用户提供调整 PIP 窗口大小的方法，OEM 也没有。随着 Android 11 开发者预览版 2 的 SystemUI 中引入一个名为 PipResizeGestureHandler 的新类，这种情况可能会发生变化。](https://android.googlesource.com/platform/frameworks/base/+/master/core/res/res/values/config.xml#3417)

这个新类负责检查画中画窗口左、右、上、下边缘周围的触摸区域内的手势事件。用户可以拖动画中画窗口来调整它的大小，尽管窗口的纵横比不会改变。目前，通过调整大小，画中画窗口的大小似乎没有限制。以这种方式调整画中画窗口的大小似乎类似于调整[自由形式多窗口](https://www.xda-developers.com/android-nougats-freeform-window-mode-what-it-is-and-how-developers-can-utilize-it/)的大小，除了自由形式窗口没有强制的纵横比。

PipResizeGestureHandler 类是 com.android.systemui 的一部分，而不是 com.google.android.systemui 的一部分，因此这种画中画模式功能的变化应该会在 AOSP Android 11 以及谷歌 Pixel 上的 Android 11 中得到反映。由于该类位于 com.android.systemui.pip.phone 下，而不是 com.android.systemui.pip.tv 下，因此该功能很可能是针对手机而不是 Android TV 的。然而，我无法在我的 Pixel 3a XL 上激活这项新功能，所以我不能确认它是否有效。不过，我将在这个版本和后续的预览版中更多地探索代码，看看我是否能让它工作起来。

**[安卓 11 XDA 新闻](https://www.xda-developers.com/tag/android-11/)**