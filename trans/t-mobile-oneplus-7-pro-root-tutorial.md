# 如何跳过 T-Mobile 一加 7 Pro Bootloader 解锁等待时间

> 原文：<https://www.xda-developers.com/t-mobile-oneplus-7-pro-root-tutorial/>

去年秋天，一加凭借 T-Mobile 品牌的一加 6T 首次正式进入美国市场。除了一些定义上的差异，它与国际版本基本相同。最显著的变化是 SIM 托盘只能容纳一张 nanoSIM 卡，并且缺少即时引导程序解锁选项。通过 T-Mobile 购买一加 6T 的客户必须首先完全付清设备费用，并在解锁引导程序之前解锁 SIM 卡。这是一个至少 40 天的过程。幸运的是，解决这个问题就像[转换成国际固件](https://www.xda-developers.com/t-mobile-oneplus-6t-international-without-unlocked-bootloader/)并像平常一样解锁引导程序一样简单。对我们来说不幸的是，一加用其最新的 T-Mobile 手机一加 7 Pro“修复”了这个变通办法。

虽然你仍然可以将你的 T-Mobile 一加 7 Pro 刷新到国际固件，但这样做并不允许你解锁引导程序。然而，有一个相当简单的方法来解锁你的 T-Mobile 变种的引导加载程序，即使你没有资格获得官方解锁。我们自己的丹尼尔·马尔凯纳偶然发现了这个方法，而且这个方法非常简单。

**[T-Mobile 一加 7 Pro 论坛](https://forum.xda-developers.com/oneplus-7-pro)**

**注意:这可能是一个限时的机会。这个过程依赖于刷新一加的 Android Q DP3，一加可能会修补这个方法。**

## 扎根 T-Mobile 一加 7 Pro 的步骤

警告:此过程将会删除您的数据(两次)！开始之前，请确保您已经备份了所有内容。

1.  你需要做的第一件事是将你的一加 7 Pro 刷新到国际固件。亚当为此写了一份快速指南。
2.  一旦你上了国际版固件，你会想要下载并刷新国际版的 Android Q 开发者预览版 3。你可以在这里下载固件[。](https://forums.oneplus.com/threads/android-q-developer-preview-3-for-oneplus-7-pro-and-7.1076548/)
    *   如果到目前为止一切正常，您应该会注意到没有任何服务。
3.  转到“设置”并启用开发者选项。
4.  转到开发者选项并启用 OEM 解锁开关。
5.  重启到快速启动，像平常一样解锁引导程序。如果你不确定如何做到这一点，亚当在这里有一个指南。

在这一点上，你的 T-Mobile 一加 7 专业版将引导加载解锁。如果你想恢复手机服务，要么刷新 Android Pie 回滚包(可以从 Android Q DP3 固件的同一页面获得)，要么安装 TWRP，刷新你选择的自定义 rom。丹尼尔测试了 ha 浩劫操作系统和 AOSiP 操作系统，它们都在他的设备上运行良好。请记住，可能会有一些不可预见的兼容性问题。

如果出于任何原因，你需要使用 [MSMDownloadTool 来恢复你的手机](https://forum.xda-developers.com/oneplus-7-pro/how-to/guide-mega-unbrick-guide-hard-bricked-t3934659)，你将会得到一个锁定的引导程序，你需要重新开始这个过程。

仅此而已。这比一加 6T 的方法稍微复杂一点，但也不复杂多少。请记住，这可能会在即将到来的开发者预览版中得到修补，所以如果你一直在考虑支持你的一加 7 Pro，现在是时候了。如果你真的尝试了，让我们知道它是否对你有效！