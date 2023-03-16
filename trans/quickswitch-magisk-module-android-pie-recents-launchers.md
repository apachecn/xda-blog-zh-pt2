# QuickSwitch 是一个 Magisk 模块，可以在受支持的第三方启动器上启用 Android Pie 最近的应用程序

> 原文：<https://www.xda-developers.com/quickswitch-magisk-module-android-pie-recents-launchers/>

# QuickSwitch 是一个 Magisk 模块，可以在受支持的第三方启动器上启用 Android Pie 最近的应用程序

QuickSwitch 是一个 Magisk 模块，它将 Android Pie 最近的应用程序功能带到了更多的启动器中。它目前与 Lawnchair 合作，不久将与 Hyperion 合作。

Android Pie 给最近的应用切换器带来了巨大的变化。谷歌完全重新设想了用户应该如何与最近的应用程序和主屏幕进行交互。垂直滚动的通讯录被应用程序窗口的水平列表所取代。谷歌自己的 Pixel Launcher 更进一步，在最近的应用程序屏幕上添加了搜索栏和应用程序快捷方式。不幸的是，这些功能并不适用于所有的发射器，但一个新的 Magisk 模块改变了这一点。

Android Pie 的一个令人沮丧的事情是，最近的新应用程序功能并不适用于所有的发布者。许多人错误地认为这些功能是 Pixel Launcher 独有的，但其他 OEM 也将这些功能集成到了他们预装的 Launcher 中。第三方启动器也可以自定义最近的应用程序屏幕，但是需要做一些工作。QuickSwitch 是一个 Magisk 模块，它将这些特性带到了更多的启动器中。它目前与 Lawnchair 合作，并将很快支持 Hyperion Launcher。

Lawnchair [最近发布了一个 Magisk 模块](https://www.xda-developers.com/lawnchair-android-pie-recent-apps-integration-root/)，使得集成 Android Pie 最近的应用成为可能。QuickSwitch 是一个类似的想法，但它希望与更多的发射器一起工作。该模块允许用户选择哪个启动器可以访问 quickstep(最近的应用程序)。QuickSwitch 检测哪些已安装的启动器能够成为最近的提供商。应该支持任何合并了 Android Pie 更改的基于 launcher3 的启动器。

**要求:**

*   安卓派。
*   Magisk 17+或 rootless，前提是您有 TWRP 和支持 init.d 的解锁引导加载程序。
*   一个可以作为最近提供商使用的启动器。

**安装:**

1.  通过 Magisk 或 TWRP 刷新快速开关模块。
2.  重启。
3.  打开快速切换应用程序。
4.  选择一个启动器作为您的最近通话提供商。
5.  重启。

[**在 Magisk 论坛**](https://forum.xda-developers.com/apps/magisk/module-quickswitch-universal-quickstep-t3884797/) 阅读更多关于 QuickSwitch 的信息