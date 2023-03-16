# 一加启动器准备添加隐藏桌面对象的“纯模式”

> 原文：<https://www.xda-developers.com/oneplus-launcher-apk-teradown-pure-mode-gesture-for-hiding-desktop-objects/>

在最近的几次更新中，一加对 OxygenOS 的股票发射器做了一些小的调整。随着一加发布 v4，该公司[修改了最近菜单](https://www.xda-developers.com/oneplus-launcher-4-4-app-switcher-quick-search/),在应用预览下方添加了应用图标，以方便切换；在 4.5.2 版本中，changelog 向[暗示了一个名为 SearchPlus](https://www.xda-developers.com/oneplus-launcher-4-5-2-prepares-searchplus-scout-indian-oxygenos-builds/) 或一加 Scout 的全系统搜索功能，可以直接从应用抽屉的搜索栏中搜索应用、联系人和消息。在最新版本即 v4.5.4 中，一加启动器采用了新的[向下滑动手势来打开货架](https://www.xda-developers.com/oneplus-launcher-4-5-4-adds-swipe-down-gesture-oneplus-shelf/)。在同一个版本中，我们还发现了一个叫做“纯模式”的*看似*的新功能，它可以用来“隐藏桌面对象”。

根据我们在拆卸一加发射器 4.5.4 测试版时发现的字符串，纯模式可以通过将四个手指放在屏幕上并向外张开来激活。你们中使用 iPad OS 或 macOS 的人可能会将此与[“显示桌面”手势](https://support.apple.com/en-in/HT204895)相比较。根据下面的字符串描述，纯模式可以通过向内拉动手指来反转。

以下是我们在一加发射版 4.5.4 APK 拆卸版中发现的与纯模式相关的字符串:

```
 <string name="launcher_pure_mode">Pure mode</string>
<string name="launcher_pure_mode_description">Put four fingers on the display and spread them apart to hide desktop objects; Reverse this gesture to resume from Pure mode.</string>
<string name="launcher_pure_mode_dialog_btn_close">Understand</string>
<string name="launcher_pure_mode_dialog_description">Put four fingers on the display and close them up to resume from Pure mode.</string>
<string name="launcher_pure_mode_subtitle">Gesture for hiding desktop objects</string> 
```

由于该功能已经在开发中，我们无法确定这里的“桌面”是指主屏幕还是与连接外部显示器时激活的桌面模式有关。这个手势目前没有被激活，在一加启动器的设置菜单中也没有任何选项可以暗示与纯模式相关的东西，这让我们很好奇。

一加发射器的纯模式可以是:

*   简单模式，只有基本图标，如电话、信息和一些信使——顾名思义。这可能是一加数字健康事业的一部分，比如去年推出的[禅模式](https://www.xda-developers.com/oneplus-zen-mode-oxygenos-challenges-140/)，或者
*   该手势可能与桌面模式(目前必须从开发者选项中强制执行)有一些关系，并可用于隐藏所有打开的浮动窗口以显示桌面——就像在 macOS 上一样。

然而，这两种情况都是推测性的，可能是也可能不是纯模式的结果，所以要有所保留。我们希望在不久的将来通过更新了解更多关于这个特性的信息，如果我们发现一些重要的东西，我们会更新这篇文章。

*感谢 XDA 资深会员 [Some_Random_Username](https://forum.xda-developers.com/member.php?u=8234677) 的提示！*