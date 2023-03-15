# 成功登陆 AOSP 的顶级 Root-only 功能

> 原文：<https://www.xda-developers.com/from-the-community-to-aosp-root-only-features-that-made-the-cut/>

Android 是迄今为止最受欢迎的移动操作系统之一，其颠覆性的增长不仅归功于开放的手机联盟，还归功于该系统所包含的大量有用功能，这些功能实际上是富有成效的，而不仅仅是华而不实的。

然而，情况并非总是如此，在早期，固件构建缺少我们今天看到的功能丰富的许多组件。这些功能中的大部分要么来自山景城本身，要么来自许多设备原始设备制造商的核心，他们根据自己的喜好调整 Android...但是一些功能来自于，是的，你猜对了，Android 爱好者社区本身。通常从根应用程序开始，一些小的 mod 或定制 ROM 特性最终获得了足够的牵引力，为自己在 AOSP 库中赢得了一席之地，要么作为直接进口，要么作为不错的“端口”。以下是一些最著名的例子:

* * *

## 抬头通知

早在 2014 年初，[偏执的 Android](http://forum.xda-developers.com/paranoid-android) 团队宣布了 Hover，这是一个通知和多任务功能，领先于当时任何其他可用的功能。发布后不久，该团队推出了固件版本 4.3 的第一个测试版，由此带来的用户体验是无缝的，并提高了生产力。Hover 是 PA 的 Halo 系统的一种演变，它在屏幕顶部弹出浮动通知，允许用户快速浏览收到的通知，并将其扫开，或与它们互动。这取代了 Android 内置的烦人的 ticker 通知系统，不久之后，Android Lollipop 宣布内置浮动通知，尽管没有 [Hover](http://www.xda-developers.com/xhover-xposed-module/) 在处理通知时使用的浮动窗口系统。有趣的是，后来被称为“抬头通知”的代码被发现潜伏在 KitKat 4.3 和 4.4 库中，社区很快[制作了 mods](http://forum.xda-developers.com/xposed/modules/mod-heads-notifications-t2791217) 来启用它们。自从集成到 Android Lollipop 以来，几乎没有什么变化，5.1 更新继续添加之前缺失的“向上滑动隐藏”功能。

## 通知切换(快速设置)

CyanogenMod 作为一个小型的售后固件选项已经走过了很长的路，并作为 Android 系统的一部分开创了许多功能。CyanogenMod 7 是固件的姜饼版本，也是负责将 CM 名称放在许多爱好者嘴边的版本，它以快速切换的形式为通知阴影带来了一个有用且节省时间的功能，借鉴了三星在 TouchWiz 中的类似实现。这些小按钮位于通知面板的顶部，允许用户快速切换重要和常用的系统功能，如 WiFi、蓝牙、GPS 等。

与浮动通知不同，通知切换花了很长时间才出现在 AOSP，最终以“快速设置”的名义出现在 Android Jellybean 中，并在通知阴影中以隐藏面板的形式出现，由一个按钮切换。然而，鉴于面板的低发现率，这种实现导致了相对较差的用户体验，Android Lollipop 将它们移动到通知阴影的前面和中间，停留在标题下方但在通知上方，并可以选择通过向上滑动通知来快速隐藏它们。

## 截屏

任何操作系统的一个最明显的特性就是能够捕捉当前屏幕的内容作为图像，也就是截图。不幸的是，Android 在早期缺乏这样的能力，高级用户求助于 root 解决方案，如当时流行的 [Shoot Me](http://forum.xda-developers.com/showthread.php?t=1256109) 来满足他们的屏幕捕捉需求。唯一的例外是 TouchWiz，它可以在 AOSP 之前完成音量降低+电源按钮截图组合。这在 Android 2.2 Froyo 版本中发生了变化，当时谷歌开始向 AOSP 添加代码以实现截图，尽管它还不是官方 API，只有少数三星 Galaxy S 用户报告有能力成功实现这一点。Android 2.3 Gingerbread 使 API 正式化，应用程序可以在没有 root 访问权限的情况下拍摄设备截图，但直到 Android 4.0 冰淇淋三明治发布后，电源+音量降低截图组合才被添加到系统中，并在大多数设备上实现标准化。

## 屏幕录制

对于许多人来说，屏幕录制是一个有用的功能，无论你是想捕捉应用程序的演示，还是准备启动你的手机游戏频道，但直到 Android 4.4 Kitkat，该框架都没有原生 API 来完成录制。在此之前，先锋应用如 [SCR](http://forum.xda-developers.com/showthread.php?t=2422061) 使用了 FrameBuffer 或 SurfaceFlinger APIs，但即使如此，正常启动的应用也不允许访问它们。一种 adb-launch 技术出现了一段时间，但它被证明是重复和繁琐的，并且最常用的解决方案是使用超级用户权限来接入这些 API 的根应用程序。KitKat 的到来改变了一切，Google 终于认识到了屏幕录制的重要性，并在框架中添加了一个可公开访问的 API。从那以后，应用程序可以很容易地进入系统，获得高质量的录制，改变 Android 上屏幕录制的整个格局。

## 应用程序至标清

Android 上的存储管理曾经是一场噩梦，许多用户花了几个小时连接笔记本电脑和 Android 设备，对他们的 SD 卡进行分区，编写挂载脚本等，试图挤出用户可用的每一兆字节。小的内部分区和系统无法在 SD 卡上存储应用导致最终用户的应用安装率严重下降，除了 SD 卡分区，许多根应用如 [Link2SD](https://play.google.com/store/apps/details?id=com.buak.Link2SD&hl=en) 和 [Super App2SD](https://play.google.com/store/apps/details?id=com.droidsail.dsapp2sd&hl=en) 也出现了。Android 2.2 Froyo 将这一功能原生带到了操作系统中，突然间，用户可以将某些应用程序部分移动到 SD 卡中。这是一个很小但意义重大的改进，从那以后，内部分区的大小大大增加了，这个特性的重要性降低了，但当时它引起了人们的不满。

## 禁用系统应用

预装应用程序，或者许多爱好者喜欢称之为“膨胀软件”，是作为 Android 系统的一部分预装的应用程序，要么来自 OEM，要么来自运营商。通常情况下，这些应用程序占用大量空间，提供不必要的功能，导致用户体验不佳。在 Honeycomb 发布之前，摆脱臃肿软件的唯一方法是使用根卸载程序。然而，Android 4.0 冰淇淋三明治的推出为应用程序设置页面带来了一个功能，允许您禁用系统应用程序，虽然这不是 root enabled 功能的精确复制，但它提供了类似的可逆功能，并以用户友好的方式无缝地开箱即用。

## 瞌睡

几年前，臭名昭著的 [Greenify](http://forum.xda-developers.com/apps/greenify) 开始作为一种提高性能和节省电池的解决方案流传开来，它有效地将后台应用程序置于强制睡眠状态。它迅速扩大规模，各地的高级用户和爱好者都获得了性能和电池改进的修复，直到今天仍然是一个受欢迎的应用程序。Android 6.0 棉花糖[推出了 Doze](http://www.xda-developers.com/android-m-adds-doze-deep-sleeping/) ，这是一个与 Greenify 的路径无关的功能，它将后者近乎神奇的电池节省功能作为一项被动的永远在线服务，默认情况下可供每个用户使用。Doze 利用 Android 的传感器阵列来检测设备何时不在运动，并随后关闭设备上的几乎所有东西，只为通话、短信和其他高优先级通知保存状态。谷歌也有一个聪明的应急计划，通过谷歌云消息服务器强制路由和后续检查，防止开发人员错误地中断 Doze。

## 荣誉奖

尽管上述特性是从社区特性跳到 AOSP 代码库的最显著的特性之一，但是许多其他相对次要的特性也是如此。很少是以与它们的根对应物相同的方式实现的，但是大多数都经历了 Google 认为合适的改变。多窗口是前者之一，Android Marshmallow 具有一个隐藏的开关，以一种几乎与售后固件相同的方式实现分屏生产力增强，如 [OmniROM](http://forum.xda-developers.com/omni) 。

其他经历了相对实质性修改的包括:

1.  像 [XPrivacy](http://forum.xda-developers.com/xposed/modules/xprivacy-ultimate-android-privacy-app-t2320783) 这样的隐私控制，允许用户阻止应用程序访问某些权限。这一功能的一个版本在 Android 4.3 中以“App Ops”的名称首次出现，但在 Android 4.4 KitKat 中很快被移除。用户找到了[的变通办法](http://www.xda-developers.com/xposed-module-brings-back-app-ops-to-android-4-4-2-and-gives-your-control-of-your-application-permissions/)来启用隐藏设置，但直到 Android 6.0 棉花糖，权限设置才全面进入
2.  Android 一直是用户的最爱，因为它提供了无尽的定制选项，主题化是定制最重要的底层组件之一。完整的设备主题化通过 T-Mobile 的主题引擎的发布而流行起来，并一度占据了垄断地位，直到一个开发团队将 RRO 层带到了各种各样的定制 rom 中。Layers 最初是由索尼为 Xperia 主题开发人员创建的，在社区中获得了巨大的吸引力，用户最近报告称，Layers 主题也可以在 Android 6.0 Marshmallow 中本机工作(使用 root)，这使得爱好者认为，作为 AOSP 的一部分，对它们的全面支持可能就在眼前。
3.  多年来，Android 上的锁屏经历了各种各样的变化，从简单的 Froyo 滑块，到兜售 Jellybean one 的小工具，最后是最小而优雅的棒棒糖锁屏。虽然像 [WidgetLocker](https://play.google.com/store/apps/details?id=com.teslacoilsw.widgetlocker&hl=en) 这样的应用程序带来了没有 root 的锁屏小工具功能，但将相机快速启动和音乐控制等功能引入锁屏是由 modding 社区决定的。直到安卓冰淇淋三明治发布之前，它们才被合并到 AOSP，并一直延续至今，尽管有一些细微的改进和润色。

你知道以前有什么 Android 功能是根用户专有的吗？请在下面的评论区告诉我们