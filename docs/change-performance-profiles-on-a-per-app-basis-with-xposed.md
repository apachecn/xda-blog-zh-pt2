# 使用 Xposed 基于每个应用程序更改性能配置文件

> 原文：<https://www.xda-developers.com/change-performance-profiles-on-a-per-app-basis-with-xposed/>

# 使用 Xposed 基于每个应用程序更改性能配置文件

使用这个 Xposed 框架模块在每个应用程序的基础上更改您的性能配置文件。

你可能还记得不久前， [CyanogenMod 在其最近的版本中实现了每个应用的性能概要文件](http://www.xda-developers.com/android/upcoming-cyanogenmod-11-builds-to-include-benchmark-performance-optimizations/ "Upcoming CyanogenMod 11 Builds to Include Benchmark Performance “Optimizations”")。虽然许多人很快批评了这一举动，因为[的某些基准](http://review.cyanogenmod.org/#/c/64308/1/overlay/common/frameworks/base/core/res/res/values/config.xml)被自动包含在高性能白名单中，但当明智地使用并给予足够的用户控制和透明度时，性能配置文件是合理有用的。毕竟，在阅读电子书时，你可能会限制自己的最大 CPU 速度或活动核心数。

显然，并不是所有人都运行 CyanogenMod ROM。但是幸运的是，有一些工具可以将性能分析带给所有 rom 的用户。XDA 公认的开发人员 h0rn 3t T1 的 Performance Profiles 就是这样一个工具，它使用了 T2 的 Xposed Framework T3 的魔力。

顾名思义，性能配置文件允许用户设置每个应用程序的性能参数。这包括能够修改最小和最大 CPU 频率(包括多核控制)、调控器、I/O 调度器、GPU 频率、NICE 优先级等等。当你的屏幕关闭时，当你在锁屏时，或者当你在某些应用程序中时，你可以设置这些参数的描述文件。应用程序是通过活动来检测的，所以当一个应用程序在屏幕上至少有一个可见的活动时，这是有效的。

如果你一直在寻找一种方法来在你的设备上实现每个应用程序的性能配置文件，那就去试试[模块线程](http://forum.xda-developers.com/xposed/modules/xposed-performance-profile-t2723739)吧。