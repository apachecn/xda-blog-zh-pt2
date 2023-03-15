# 将无线 Xbox 360 控制器与 Nexus 7 配对

> 原文：<https://www.xda-developers.com/pair-a-wireless-xbox-360-controller-with-a-nexus-7/>

通常当我们想到将无线控制器与 Android 设备配对时，它是 Playstation 3 或 Wii 控制器。虽然这肯定没有什么错，但还是有人更喜欢 Xbox 360 手柄。虽然有线版本已经在 Android 上运行了一段时间，但现在有一种方法可以让无线 Xbox 360 控制器在 [Nexus 7](http://forum.xda-developers.com/forumdisplay.php?f=1673) 上运行。

XDA 资深成员 [sleeplessninja](http://forum.xda-developers.com/member.php?u=3800396) 已经想出如何让无线 Xbox 360 控制器在 Nexus 7 上工作。通常，对于 Xbox 360 控制器，您需要一个有线控制器和一根 USB OTG 电缆。已经有一种方法可以使用 Xbox 360 无线控制器加密狗让控制器在 Nexus 7 上工作，但仍有很多游戏无法正确注册控制器。

此问题已修复。正如无眠忍者所解释的:

> 所以当我在/system/usr/keylayout/中搜索时，我看到有一个 xbox 360 有线控制器的配置文件，所以我想为什么不复制这个配置文件并将其命名为无线 xbox 控制器。这个想法奏效了。你用供应商 ID 和产品 ID 来命名键盘布局，我也可以从 logcat 中获得。这样做的好处是，我认为我们可以用它来解决其他控制器的问题，但我不知道还有哪个控制器也有问题。

因此，一旦进行了简单的修改，您就可以充分发挥无线 Xbox 360 控制器的潜力。如上所述，这种方法可以用来解决其他控制器的问题。要了解更多信息，请前往[原始线程](http://forum.xda-developers.com/showthread.php?t=1792531)。