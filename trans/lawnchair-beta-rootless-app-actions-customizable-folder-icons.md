# Lawnchair 的最新测试版增加了无根应用程序的动作等等

> 原文：<https://www.xda-developers.com/lawnchair-beta-rootless-app-actions-customizable-folder-icons/>

# Lawnchair 的最新测试版增加了无根应用程序操作、可定制的文件夹图标等等

Lawnchair 是最受欢迎的第三方启动器之一，它的最新测试版带来了 Android Pie 的应用程序操作功能。

Android 最大的优点之一就是它的可定制性。这种定制可以是简单的事情，比如简单地切换启动器，让你的主屏幕成为你自己的，甚至可以使用 Substratum 和最近推出的 Substratum Lite 这样的应用程序来改变 UI 和 UX 的整个方面。你想走多远实际上取决于你，但如果你想进行简单的主屏幕润色，有许多可供选择的发射器可以下载，包括用户最喜欢的【Nova 发射器和 [Hyperion 发射器](https://www.xda-developers.com/hyperion-supreme-hyperion-pro/)，由 Substratum 后面的同一批人制作。其中最可靠的一个是 Lawnchair，它今天有了一些新的改进，至少在测试版中是这样。

其中一个改进是无根应用程序动作。App Actions 只是 Android Pie 的许多新功能之一，但它需要谷歌的 Action Services 应用程序集成到系统中才能工作，这实际上结束了无根的变通方法，并限制了第三方启动器如何集成这一功能。Lawnchair 的实现有所不同:它不依赖 Android Pie 中的 AOSP 实现，而是试图模仿其功能。Lawnchair 只是从最近使用的 100 个快捷方式中取出最常用的应用程序快捷方式，然后在抽屉中显示为应用程序操作。

这种方法也允许开发人员将这一功能带到 Android 8.0/8.1 Oreo 和 Android 7.1 Nougat 设备上，因为它们完全支持应用程序快捷方式。这种方法虽然不完全是 Android Pie 实现的那种应用程序动作，但应该与 Google 的实现几乎完全一样。在其他改进中，我们还获得了自定义文件夹图标的能力，修复了旧版本的崩溃，提高了稳定性，等等。完整的变更日志包括:

*   片段#getActivity 可以为空(由 Till Kottmann 提供)
*   修复棒棒糖上剩余的崩溃
*   具体为 GSON 和 OWM 设置适当的优化规则(由 Till Kottmann 提供)
*   修复 OWM 集成，初步支持基于位置的天气与 OWM(由蒂尔科特曼)
*   不要把启动动作当成应用程序启动
*   仅使用多达 100 个事件来预测行动(由 Till Kottmann)
*   将图标形状覆盖迁移到常规首选项以允许备份它(由 Till Kottmann 完成)
*   摆脱不工作的电报聊天插件
*   减少惰性初始化的不必要使用(由 paphonb)
*   创建无根的行动建议实施(由 Till Kottmann)
*   修复开放主页设置(由蒂尔科特曼)
*   为没有 root 用户的用户添加后备应用建议算法(由 Till Kottmann 提供)
*   修复向下滚动后选择图标包时的崩溃
*   修复剩余的不正确图标存在检查(由 Till Kottmann)
*   懒惰地初始化更多的东西以减少内存占用(由 Till Kottmann 提供)
*   重构抽屉标签后端(由 paphonb 提供)
*   显著提高图标包解析速度(由 Till Kottmann 提供)
*   当 Lawnchair 未设置为默认时，减少日志溢出(由 Till Kottmann 提供)
*   正确回退到#newIcon 中的 DefaultPack(由 Till Kottmann 提供)
*   删除 2019 年愚人节的笑话(由 paphonb)
*   清理首选项控制器委托(由 paphonb 完成)
*   修正了在标签页编辑器中发送删除按钮时崩溃的问题
*   将硬件位图用于文件夹图标预览(由 paphonb 提供)
*   对选项卡名称编辑器的改进(由 paphonb 提供)
*   改进标签指示器(由 paphonb 提供)
*   初始支持自定义文件夹图标(由 Till Kottmann 提供)
*   更新最新 AS canary 的依赖项(由 Till Kottmann 提供)

你可以点击[这个链接](https://www.apkmirror.com/apk/deletescape/lawnchair/lawnchair-2-0-1905-ci-alpha-release/)从 APKMirror 下载最新的测试版。或者，如果你不想浪费测试版的时间，你可以现在就从 Play Store 购买稳定版。