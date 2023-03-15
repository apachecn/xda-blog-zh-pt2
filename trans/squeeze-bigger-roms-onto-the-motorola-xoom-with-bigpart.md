# 使用 BigPart 将更大的 rom 压缩到摩托罗拉 Xoom 上

> 原文：<https://www.xda-developers.com/squeeze-bigger-roms-onto-the-motorola-xoom-with-bigpart/>

摩托罗拉 Xoom 是一款非常重要的设备。这是第一款*真正的*安卓平板。当然，最初的[三星 Galaxy Tab](http://forum.xda-developers.com/galaxy-tab) 比 Xoom 早了一段时间，但与 Froyo 一起发货意味着它经常看起来像一部过度生长的智能手机，而不是一部根本不同的东西。

当 Xoom 第一次发布的时候，它已经被证明是有前途的，但是它已经开始显示出它的年龄了。1 GHz 的 Tegra 2 不再像以前那样精神，1280x800 的分辨率不再让观众流口水。然而，它的大部分鱼尾纹不是源于它仍然胜任的双核 CPU 或 1 GB 的 RAM，而是它的股票分区布局。事实上，摩托罗拉声称设备的系统分区没有足够的空间来存放最新版本的安卓系统。

虽然开发人员已经成功地通过远远超过摩托罗拉官方最新更新的 Android 更新来延长设备的寿命，但随着 Android 不断发展和变得越来越大，这项任务变得越来越困难。但是由于该设备的特点是内存总量很大，因此需要进行重新分区。现在，XDA 承认开发者 [bigrushdog](http://forum.xda-developers.com/member.php?u=470268) 和资深成员 [realjumy](http://forum.xda-developers.com/member.php?u=697814) (以及来自 [Schischu](http://forum.xda-developers.com/member.php?u=2371134) 和 [rchtk](http://forum.xda-developers.com/member.php?u=4533695) 的一些帮助)能够通过创建 BigPart 为这个设备注入新的生命。

将您的设备更新到新的分区布局是一个相当简单的过程。您必须首先加载新的自定义恢复。然后，该恢复基本上用于执行一系列擦除和格式化。毕竟，你的设备将被重新分区。重要的是要注意，一旦你改变你的分区布局，你必须只闪存与 BigPart 分区布局兼容的 rom。

请访问[原始线程](http://forum.xda-developers.com/showthread.php?t=2506997)以了解更多信息。请记住，因为你在搞乱分区布局，这比一般的闪存更危险。但是如果你小心谨慎，按照说明去做，这个过程本身并没有什么困难。