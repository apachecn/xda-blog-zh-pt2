# 独家:这是华为 Mate 9 上搭载 EMUI 6 的安卓奥利奥

> 原文：<https://www.xda-developers.com/android-oreo-emui-6-huawei-mate-9/>

昨天的谷歌活动最终为我们带来了[谷歌 Pixel 2 和 Pixel 2 XL](https://www.xda-developers.com/google-pixel-2-xl-announced-price/) 、 [Pixelbook](https://www.xda-developers.com/high-end-google-pixelbook-launch/) 和 [Home Mini](https://www.xda-developers.com/google-home-mini-amazon-echo/) / [Max](https://www.xda-developers.com/google-home-max-bigger-assistant/) 但是即使谷歌的热情现在正在消退，未来几周仍然有很多东西值得 Android 爱好者期待。强大的华为 Mate 10 将于 10 月 16 日在德国慕尼黑举行的新闻发布会上首次亮相，这将是华为即将推出的基于 Android 8.0 Oreo 的 EMUI 6 的首次公开亮相。在此次活动之前，我们已经获得了用于华为 Mate 9 的 Android Oreo/EMUI 6 的**预发布固件版本，这次即将到来的更新有很多有趣的变化值得注意。**

华为 Mate 9 去年 11 月才在[以](https://www.xda-developers.com/huawei-mate-9-officially-unveiled/)[顶级硬件规格](https://www.xda-developers.com/huawei-mate-9kirin-960-early-testing-comparison-with-pixel-xlsnapdragon-821/)在发布，所以看到这款设备获得 Android Oreo 更新并不奇怪。早在今年 4 月就有迹象表明 Android 8.0 更新[的早期工作正在进行，尽管当时泄露的版本相当简单。现在，我们已经获得的构建功能齐全，实际上可以安装在 MHA-L29C432(国际华为 Mate 9 变体)的顶部，所以我们只是开始挖掘 EMUI 6 更新中的新功能。](https://www.xda-developers.com/huawei-has-already-started-internal-testing-of-android-o-on-the-mate-9/)

* * *

## 华为 Mate 9 基于 Android Oreo 的 EMUI 6

### 你所期待的事情

首先，让我们抛开那些无趣的细节。正如您所料，Android Oreo 所需的大部分特性在这个版本中都有。这意味着画中画模式支持、[严格的后台应用程序限制](https://www.xda-developers.com/android-oreo-oem-background-app-limitations/)、通知通道，甚至是恼人的“应用程序正在后台运行”通知，你可以[谢天谢地仍然使用应用程序隐藏](https://www.xda-developers.com/hide-app-running-background-notification-android-oreo/)。

我们应该注意，虽然华为实现了通知通道，但他们的通知重要性控制实际上是 EMUI 5 的延续，而不是基于您可能熟悉的 AOSP 版本。我认为这是一个福音，因为这意味着你不需要第三方应用程序来为不针对 Android Oreo 的应用程序带来通知重要性控制。

### EMUI 6 更新

这是事情变得更有趣的地方。总的来说，我会说 EMUI 5 和 EMUI 6 表面上没有太多变化，但有一些新的软件增加应该会让一些人高兴。

首先，在显示设置中有一个新的**屏幕分辨率**选项。这是基于 EMUI 5 的动态屏幕分辨率功能，称为“智能分辨率”(也存在于 EMUI 6 中)。虽然智能分辨率会自动在 720p 和 1080p 之间切换以节省电量，但这一新选项允许您手动在两种分辨率之间切换。这种方法可能比使用 ADB“WM size”命令要好，因为 ADB 命令只调整虚拟分辨率，而不是实际上让显示器以较低的分辨率进行渲染。

接下来，有一个新的按钮可以放在导航栏上。启用该按钮时，它会在导航栏的左侧添加一个小箭头。按下此按钮将暂时隐藏导航栏，直到您从底部向上滑动。对于那些喜欢拥有股票导航栏，但希望偶尔按需使用全屏显示的人来说，这个新按钮击败了 ADB 命令[永久隐藏导航栏](https://www.xda-developers.com/how-to-hide-the-navigation-bar-in-emui-5-0/)或[启用沉浸式模式](https://www.xda-developers.com/how-to-enable-system-wide-immersive-mode-without-root/)。这个按钮在技术上并不新，因为它出现在中国华为 Mate 9 固件上，但它对国际版本来说是新的。

如果你不是软件导航栏的粉丝，那么有另一个新的导航选项可供你尝试。它被称为**导航坞**，它的作用是放置一个可移动的浮动按钮，可以取代导航栏，用于所有后退、主页或最近的按钮按压。这与 EMUI 5 的“浮动码头”不同，因为该功能就像一个伪饼图控件，按下按钮将扩展可用导航选项的列表。EMUI 6 的导航 dock 使用手势控制，如向上滑动以返回主页，向右滑动以查看最近的内容，以及触摸以返回。

最后，在开发者选项中，我们发现了一些奇怪的东西。常见的[蓝牙音频编解码器定制](https://www.xda-developers.com/android-o-introduces-bluetooth-audio-codec-options/)功能出现了，因为它能够在各种蓝牙音频编解码器之间切换——包括 [aptX 和 aptX HD](https://www.xda-developers.com/google-says-it-wont-add-support-for-aptx-on-the-nexus-5x-and-nexus-6p/) 。aptX 和 aptX HD 是高通拥有的专有蓝牙音频编解码器，因此希望使用它们的公司必须向高通支付许可费。

我们不知道为什么华为甚至把它作为一个可选选项，因为它在这里甚至不工作(选择这些选项中的任何一个都会把选择恢复到 SBC)，但话说回来，这个*是*预发布版本，所以这些选项可能会在最终版本中消失。或许有了 root 访问权限和 Magisk 模块，我们可以像[谷歌 Nexus 6P](https://forum.xda-developers.com/showpost.php?p=72693862&postcount=42) 用户一样支持它。

### 发动机罩下的变化

你可能会奇怪，为什么我们还没有显示“关于手机”部分的截图。这是因为，就像华为内部发布的每一个测试版/测试版本一样，软件版本都被更改以减少泄露。幸运的是，通过查看 build.prop 文件可以很容易地验证真正的软件版本。在其中，我们可以看到以下内容:

```
 [ro.build.version.security_patch]: [2017-09-05]
[ro.build.version.release]: [8.0.0]
[ro.build.version.sdk]: [26] 
```

从一个单独的命令中，我们可以找到 Linux 内核版本

```
 Linux version 4.4.23+ (android@localhost) (gcc version 4.9.x 20150123 (prerelease) (GCC) ) #1 SMP PREEMPT Thu Sep 14 04:10:43 CST 2017 
```

所以，从这些信息来看，我们获得的华为 Mate 9 build 确实是基于 Android 8.0 Oreo(SDK 26 级)的。 [Linux 内核版本是 4.4](https://www.xda-developers.com/google-mandating-linux-kernel-versions-android-oreo/) ，从 Mate 9 上基于牛轧糖的 EMUI 5 的 4.1 更新而来。此外，安全补丁级别是 2017 年 9 月，这意味着 Mate 9 是 **[安全的，不会受到 Blueborne 漏洞](https://www.xda-developers.com/bluetooth-vulnerability-blueborne-impacts-android-ios-windows-and-linux-devices/)** 的影响。

最后，我们发现了一些 Android 爱好者特别感兴趣的事情。第一，**项目高音**支撑在那里。尽管 Mate 9 的[内核源代码已经发布好几个月了，但还没有任何定制的基于 AOSP 的 rom 可供该设备使用。](https://www.xda-developers.com/kernel-sources-released-for-the-huawei-mate-9-and-huawei-p10/)[也许项目三冠王支持会改变那个](https://www.xda-developers.com/project-treble-custom-rom-development/)，也许不会。这仍然很有趣，因为这是第一款确认支持 Project Treble 的设备，尽管它没有与 Android Oreo 一起推出。

最后但同样重要的是，这里有一件没人预料到会发生的事情:EMUI 中的底层支持。是的，**底层主题在 EMUI 6** 上起作用。这都要归功于索尼向 AOSP 做出的覆盖管理器服务(OMS)承诺，这些承诺最终在 Android Oreo 中实现了完全工作状态。正是由于这一点，谷歌 Nexus 和 Pixel 用户能够[使用](https://www.xda-developers.com/custom-themes-android-oreo-substratum/)[Andromeda add-on for substrate](https://www.xda-developers.com/andromeda-substratum-custom-themes-oreo/)享受全面的定制主题支持。我们在某些应用程序中测试了[命令行界面](https://www.xda-developers.com/android-oreo-command-line-themes/)以及[黑暗主题](https://www.xda-developers.com/install-dark-theme-android-oreo-without-root/)，可以确认它确实可以工作。

Substratum 支持乍一看可能不那么有趣，因为华为已经有了自己的主题引擎，但应该注意的是，Substratum 将允许您对不仅仅是系统应用程序进行主题化，正如在上面的 Google Messenger 应用程序截图中可以看到的那样。

* * *

这就是我们在华为 Mate 9 的 Android 8.0 Oreo 内部测试版中发现的所有内容。敬请关注 XDA 门户网站，我们将分享更多关于即将推出的华为和 Honor 设备的信息。跟踪门户网站的最佳方式是安装 XDA 实验室应用程序！

*固件是由 [FunkyHuawei.club](https://funkyhuawei.club/) 提供给我安装在我的华为 Mate 9 上的，这项服务可以让你安装预发布的华为固件，恢复被屏蔽的设备，并将中国地区的手机更名/转换为国际版本。该服务将在发布时支持 Mate 10。*