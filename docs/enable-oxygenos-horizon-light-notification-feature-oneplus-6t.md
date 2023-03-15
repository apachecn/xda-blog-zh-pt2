# 在一加 6T 上启用 OxygenOS 的地平线灯光通知[Root]

> 原文：<https://www.xda-developers.com/enable-oxygenos-horizon-light-notification-feature-oneplus-6t/>

# 在一加 6T [Root]上启用 OxygenOS 的地平线灯光通知功能

XDA 资深会员 mcdachpappe 创建了一个 Magisk 模块，可用于启用一加 6T 上的地平线灯光通知功能。请继续阅读！

为了便于维护和互操作性，一加为其所有设备上基于 Android 的 OxygenOS 软件维护了一个共同的代码库。以备受期待的 Always on Display 模式为例:它终于在一加 8 系列的最新 OxygenOS 11 开发者预览版中出现，[原始设备制造商已经承诺](https://www.xda-developers.com/oneplus-phones-always-on-display-oxygenos-11/)在即将到来的更新中为一加的其他智能手机带来这一功能。然而，该公司没有[跳过将“地平线之光”通知功能反向移植到一加 6T](https://www.xda-developers.com/oneplus-7-pros-horizon-light-feature-wont-be-coming-to-the-oneplus-6t-or-oneplus-7/) 。

**[一加 6T XDA 论坛](https://forum.xda-developers.com/oneplus-6t)**

对于那些不熟悉*地平线光*的人来说，一加设计了这个功能，当通知到达时，它会在显示屏的两侧显示脉冲。从[一加 7 Pro](https://forum.xda-developers.com/oneplus-7-pro) 开始，这种边缘照明功能在所有带曲面屏幕的一加手机上都可以使用，这意味着它在[一加 7T Pro](https://forum.xda-developers.com/7t-pro) 和[一加 8 Pro](https://forum.xda-developers.com/oneplus-8-pro) 上都可以使用，但在[一加诺德](https://forum.xda-developers.com/oneplus-nord)上不能使用。

XDA 资深成员 [mcdachpappe](https://forum.xda-developers.com/member.php?u=7030109) 现在提出了一个 Magisk 模块，可以在一加 6T 上启用*地平线光*。[模块](https://github.com/mcdachpappe/edgelighting)的工作原理很简单:用修改过的替换 OxygenOS 的股票系统 UI APK。通过 Magisk Manager 刷新模块后，您的一加 6T 的边缘应在每次通知时亮起五次。脉冲的颜色对应于生成通知的应用程序图标的颜色，例如 WhatsApp 为绿色。不过，这个模型没有用户界面，所以你不能修改硬编码的参数(灯光频率，颜色等。).

**[Magisk 模块启用一加 6T - XDA 线程上的地平线](https://forum.xda-developers.com/oneplus-6t/themes/magisk-edgelighting-horizonlights-t4142035)**

该模块的初始版本根据 [OxygenOS 10.3.5](https://www.xda-developers.com/download-oneplus-6-6t-receive-oxygenos-1035-ram-optimizations-buds-support-more/) 进行测试。国防部还不支持动态资源修补，这就是为什么当一加为一加 6T 推出下一个 OxygenOS 更新时，你可能需要一个新版本。