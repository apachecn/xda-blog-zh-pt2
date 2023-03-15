# 小米米 A1 利用安卓牛轧糖的 A/B 分区提供无缝更新

> 原文：<https://www.xda-developers.com/xiaomi-mi-a1-android-ab-partition/>

新的[小米 Android One 设备](https://www.xda-developers.com/xiaomi-joins-the-android-one-program-in-india-with-the-new-xiaomi-mi-a1/)，Mi A1，被证明是一个非常有趣的设备。这是小米第一款开箱不运行 MIUI 的设备。相反，这款设备运行的是搭载谷歌应用程序(Google Apps)和一些小米插件的普通安卓系统，以通常不应期待的价格区间和硬件套装提供了类似像素的体验。

运行 Android 而不是 MIUI 的好处之一是，Mi A1 的行为更可预测，受益于几个尚未进入 MIUI 的功能添加。其中之一是 Android 7.1 牛轧糖的[无缝更新功能](https://www.xda-developers.com/current-android-devices-are-unlikely-to-receive-android-ns-seamless-update-feature/)，这在谷歌 Pixel 和谷歌 Pixel XL 上有所体现，在后来的设备如 Moto Z2 Force 上有[。我们还没有看到这一功能的广泛采用，但随着](https://www.xda-developers.com/moto-z2-force-ab-seamless-updates/)[更多的 Android One 设备即将推出](https://www.xda-developers.com/moto-x4-android-one-render-leaked/)，这种情况可能很快会变得更好。

正如 [4pda.ru 论坛](http://4pda.ru/forum/index.php?showtopic=842604)上的用户所发现的，也正如我们自己的评测单位所证实的，小米 Mi A1 确实带有 [A/B 分区](https://source.android.com/devices/tech/ota/ab_updates)支持。

这意味着小米 Mi A1 带有两组分区，其中一组在设备活动时使用，而另一组则在应用新更新时使用。新的更新被下载并安装到非活动插槽上，而活动插槽继续进行它们的工作以保持电话开启和工作。更新安装完成后，设备会重新启动以将活动插槽与非活动但已更新的插槽进行切换，从而为用户提供无缝升级体验，除了简单的重新启动之外，几乎没有设备停机时间。由于用户数据分区是跨插槽共享的，所有下载的应用程序和其他个人用户数据都可供任一插槽使用。

A/B 分区各有利弊。拥有一组额外的分区可以作为备份，以防在更新过程中出现问题。如果设备在几次尝试后仍无法引导到更新的插槽中，它将重新引导到旧的插槽中，用户可以在重试更新时继续使用他的设备。无缝更新体验也有利于最终用户，他们不再需要盯着“Android 正在升级”屏幕几分钟，等待更新应用。

另一方面，A/B 分区本质上是两组分区，大多数时候只需要一组。结果，终端用户得到较低的存储量，因为电话存储的额外部分被保留给这些额外的分区。这在具有大量内部内存的设备上可能不是问题，因为 [A/B 分区更改只需要*一些*额外空间](https://source.android.com/devices/tech/ota/ab_updates#how-did-ab-affect-the-2016-pixel-partition-sizes)(因为对更多空间的需求会根据现在已过时的缓存和恢复分区的删除进行调整)。

此外，当涉及到 Pixel 和 Pixel XL 上的定制 ROM 和内核开发时，A/B 分区与基于文件的加密的切换相结合确实造成了一些技术障碍。Magisk 仍然没有为谷歌 Pixel 和谷歌 Pixel XL 提供官方支持，尽管[工作正在进行中](https://forum.xda-developers.com/showpost.php?p=73485958&postcount=28)和[用户可以安装非官方版本](https://forum.xda-developers.com/apps/magisk/unofficial-google-pixel-family-support-t3639262)。就支持 Moto Z2 势力而言，A/B 分区甚至[继续与社区](https://forum.xda-developers.com/z2-force/how-to/progress-root-twrp-roms-t3660300)作对。

* * *

此外，如果你好奇小米 Mi A1 带来的变化，小米已经在其网站上发布了该设备的[完整系统映像。可用的系统映像适用于版本 N2G47H.7.8.23 (Android N ),大小为 1.28GB。](http://en.miui.com/download-333.html)

小米 Mi A1 将于 9 月 12 日在印度进行首次销售。

* * *

**对小米米 A1 及其采用牛轧糖的 A/B 分区布局实现无缝更新有什么想法？请在下面的评论中告诉我们你的想法！**