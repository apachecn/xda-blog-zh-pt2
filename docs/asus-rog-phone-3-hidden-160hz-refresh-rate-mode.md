# 如何在华硕 ROG 手机 3 上启用隐藏的 160 赫兹刷新率

> 原文：<https://www.xda-developers.com/asus-rog-phone-3-hidden-160hz-refresh-rate-mode/>

上周三，华硕发布了 ROG 手机 3，这是这家台湾公司旗下 ROG 游戏子品牌的第三款智能手机。这款手机的规格表与手机本身一样庞大，可能会成为[最佳安卓手机](https://www.xda-developers.com/best-android-phones/)之一的竞争者，其功能包括高通骁龙 865+，高达 16GB 的内存，6,000mAh 电池，两个 USB-C 端口，144Hz 刷新率显示屏。在手机的显示设置中，您可以选择默认的“自动”刷新率模式，让系统决定显示器的刷新率应该是多少，或者您可以选择以 60Hz，90Hz，120Hz 或 144Hz 运行手机。有趣的是，似乎华硕一直在测试一个隐藏的第 6 刷新率模式:160Hz。

**[华硕 ROG 手机 3 论坛](https://forum.xda-developers.com/asus-rog-phone-3)**

**XDA 回顾:** [华硕 ROG Phone 3 回顾:游戏智能手机之王回来了](https://www.xda-developers.com/asus-rog-phone-3-review/)

当我在调查 ROG Phone 3 如何处理其刷新率切换时，我发现在设置应用程序中提到了隐藏的 160Hz 刷新率模式。深入挖掘，我发现了一个调试命令，可以用来在设置表面 160 赫兹模式！你所要做的就是在你的电脑上设置 Android 调试桥(ADB )(我们[在这里](https://www.xda-developers.com/install-adb-windows-macos-linux/)有关于如何做的指南),然后从命令提示符或终端窗口运行以下命令:

```
 adb shell setprop debug.vendor.asus.fps.eng 1 
```

一旦你输入这个命令，重启你的手机。手机重启后，您可以在“设置”>“显示”>“刷新率”或“刷新率快速设置”磁贴中切换 160Hz 显示模式。

如果你怀疑这是否真的有效，你可以用几种方法中的一种来测试刷新率。首先，你可以去[testufo.com](https://testufo.com/)看 UFO 在太空中循环的帧速率。第二，你可以试试[流体模拟 app](https://play.google.com/store/apps/details?id=games.paveldogreat.fluidsimfree) ，在 app 的设置里把刷新率设为 160。(这是我个人最喜欢的测试方式，因为随着流体运动变得更加平滑，您可以真正看到更高刷新率的影响。)最后，你可以尝试在 ROG 手机 3 上支持 144fps 播放的众多游戏之一的[——如果游戏在设备上支持 144fps 播放，那么它的帧速率很有可能实际上是“解锁的”，也可以以 160fps 运行。例如，Pac-Man 应用程序对我来说运行速度是 160fps，我相信许多其他人也会这样。](https://www.xda-developers.com/asus-rog-phone-3-144hz-high-refresh-rate-display-games-support/)

现在，我肯定你在想这样做是否安全。如果对面板不安全的话，我想华硕是不会测试这个更高的刷新率的。我已经用 160 赫兹的频率运行我的 ROG Phone 3 好几天了，没有遇到任何稳定性问题。然而，很明显，华硕没有完成这种显示模式，因为它似乎没有在这种模式下正确校准显示器。您可以在“设置”>“显示”>“精彩”中调整一些显示参数，直到您找到一个看起来对您有吸引力的配置，但这种刷新率模式被隐藏是有原因的——它不是最终用户级别的。由于手机和显示器能够处理 160Hz 的 2340x1080，我希望华硕重新考虑这种显示模式，并在适当校准后在未来的软件更新中启用它。ROG Phone 3 当然有足够的能量(高通骁龙 865+)和电池(6000 毫安时)来处理它，为什么不呢？

如果您想禁用此功能并将显示设置恢复正常，只需从您的 PC 输入以下 ADB 命令，然后重启手机:

```
 adb shell setprop debug.vendor.asus.fps.eng 0 
```

*感谢 PNF 软件为我们提供了使用* *[JEB 反编译](https://www.pnfsoftware.com/?aid=xdadev)* *的许可，这是一款针对 Android 应用的专业级逆向工程工具。*