# 三星 Galaxy S20 具有隐藏的 96Hz 显示模式

> 原文：<https://www.xda-developers.com/samsung-galaxy-s20-hidden-96hz-display-mode/>

三星最近发布了他们的 [Galaxy S20 系列智能手机](https://www.xda-developers.com/samsung-galaxy-s20-specs-features-pricing-availability/)。它们拥有三星旗舰产品的所有功能，包括性能良好的相机以及顶级的内部部件，但它们也有一个值得注意的关键特性，即高刷新率显示屏。三星 Galaxy S20 系列的显示屏支持 3200x1440 (WQHD+)的最大分辨率和 120Hz 的最大刷新率。尽管有一些限制，例如 120Hz 模式仅限于 FHD+分辨率(WQHD+仅限于 60Hz，所以你只能选择其中一个)，但这是三星的第一个也是一个重要的里程碑。

120 赫兹显然会让你的手机看起来非常流畅，但有一个缺点:电池寿命。在显示设置中，你可以选择让 Galaxy S20 以 2400x1080 (FHD+)和/或 60Hz 运行:与其他制造商的许多其他智能手机不同，没有中间 90Hz 选项，只剩下 60Hz 和 120Hz 作为两个选项。120Hz 刷新显示器的速度是 60Hz 的两倍，在此过程中会对电池寿命产生影响。然而，我们最近发现，这不是显示器支持的唯一模式:在 Galaxy S20s 中还可以设置其他隐藏的显示模式。

**XDA 论坛:[银河 S20](https://forum.xda-developers.com/galaxy-s20) || [银河 S20+](https://forum.xda-developers.com/galaxy-s20-plus) || [银河 S20 超](https://forum.xda-developers.com/galaxy-s20-ultra)**

如果你运行 shell 命令“dumpsys display”，你会发现 Galaxy S20 的显示屏实际上支持以下模式:

```
 [{id=1, width=1440, height=3200, fps=60.000004}, 
{id=2, width=1440, height=3200, fps=48.0}, 
{id=3, width=1080, height=2400, fps=120.00001}, 
{id=4, width=1080, height=2400, fps=96.00001}, 
{id=5, width=1080, height=2400, fps=60.000004}, 
{id=6, width=1080, height=2400, fps=48.0}, 
{id=7, width=720, height=1600, fps=120.00001}, 
{id=8, width=720, height=1600, fps=96.00001}, 
{id=9, width=720, height=1600, fps=60.000004}, 
{id=10, width=720, height=1600, fps=48.0}] 
```

在这里，我们可以看到有几个分辨率和刷新率是用户无法访问的:1600x720 (HD+)分辨率、96fps 和 48fps。尽管这些模式不能通过手机的设置来切换，但它们出现在这里意味着手机支持这些模式，因此，我们可以强制 Galaxy S20 在这些模式中的一种模式下运行。

通过将`Settings.System.peak_refresh_rate`和`Settings.System.min_refresh_rate`的值更改为 48.0 或 96.0，您可以将 Galaxy S20 的刷新率设置为这些隐藏值之一。将你的手机设置为 96Hz 将会使你的电池寿命略有增加，因为你的显示器不会经常刷新内容，同时仍然具有高刷新率的优势:它看起来仍然比 60Hz 平滑得多。但是，它仍然不能与 WQHD+一起使用，因为该组合没有被列为支持的显示模式之一。

**从 Amazon.in 购买—三星 Galaxy:[S20](https://www.amazon.in/Samsung-Galaxy-Storage-Additional-Exchange/dp/B08445DF23/?tag=xdaportalin-21)| |[S20+](https://www.amazon.in/Samsung-Galaxy-Storage-Additional-Exchange/dp/B084451YSS/?tag=xdaportalin-21)| |[S20 超](https://www.amazon.in/Samsung-Galaxy-Storage-Additional-Exchange/dp/B08444S68Q/?tag=xdaportalin-21)**

不过，为了让你省去运行 shell 命令的麻烦，XDA 的资深成员[sathistony](https://forum.xda-developers.com/member.php?u=5246190)开发了一个简单的应用程序，可以让你在 96Hz 和 120Hz 之间转换。该应用程序甚至添加了两个快速设置磁贴，以在刷新率模式之间切换。该应用程序是[开源的](https://github.com/SatySatsZB/S20RefreshRateControl)，非常简单，因为它所做的只是为你改变峰值刷新速率和最小值刷新速率的设置值。你可以去 testufo.com[的](https://testufo.com/)确认改变是否有效。

立即查看 XDA 实验室上的应用[！](https://labs.xda-developers.com/store/app/sszb.s20.refresh)

【appbox xda sszb.s20.refresh】