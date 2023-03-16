# 如何修复运行安卓 8.1 奥利奥的谷歌 Pixel 2/2 XL 上的多点触控 Bug

> 原文：<https://www.xda-developers.com/fix-multi-touch-bug-google-pixel-2-xl-android-oreo/>

你拥有谷歌 Pixel 2 还是谷歌 Pixel 2 XL？你想在 PUBG Mobile 赢得一些鸡肉晚餐吗？如果是这样，你可能处于劣势。不，我不是在谈论游戏中键盘和鼠标用户的猖獗使用，而是一个可能导致一些令人沮丧的触摸屏问题的错误。自 Android 8.1 Oreo 发布以来的几个月里，许多用户报告了不稳定的多点触摸行为。从谷歌问题跟踪页面上的报告数量来看，这个问题非常普遍，但是仍然没有官方的解决方案。如果你正在寻找一种方法来修复它，有一个非官方的方法，涉及到闪存 Magisk 模块，我们今天想与你分享。

在我们开始之前，让我们绝对清楚我们首先在谈论什么问题。简而言之，当两个手指放在屏幕上时，手机可能会在两个手指之间产生不稳定的触摸事件。根据我们的消息来源，这在 FPS 游戏中非常明显，但也可以在其他地方复制，例如在谷歌照片中。这里有两个视频可以帮助你想象我们正在谈论的内容:

谷歌正在进行修复，但目前还不可用。根据最近[对安卓开源项目(AOSP) gerrit 的](https://android-review.googlesource.com/#/c/platform/frameworks/native/+/640606/)[两次](https://android-review.googlesource.com/#/c/platform/frameworks/native/+/640605/)承诺，修复包括对多个指针进行重采样。XDA 资深会员 [Freak07](https://forum.xda-developers.com/member.php?u=3428502) 没有等到下一次更新时才推出补丁，而是根据 Pixel 2 和 Pixel 2 XL 的最新[4 月安全补丁版本](https://www.xda-developers.com/nexus-pixel-security-april-2018-ota-factory-images/)编译了更新后的库(具体来说就是 libinput 和 libinputflinger ),这样你就可以立即安装补丁了。因为您将替换系统文件，所以您需要一个根设备。

* * *

## 修复运行 Android 8.1 Oreo 的谷歌 Pixel 2 和 Pixel 2 XL 上的多点触摸错误

1.  [解锁设备的引导程序，安装 Magisk](https://www.xda-developers.com/how-to-unlock-bootloader-and-root-the-google-pixel-2-and-pixel-2-xl/) 。
2.  从[这里](https://www.androidfilehost.com/?fid=890129502657595755)下载 Magisk 模块。
3.  使用 Magisk 管理器安装 Magisk 模块。
4.  重启你的手机。

*从左到右:安装该模块的步骤*

您不稳定的多点触摸屏问题现在应该得到解决！让我们在评论中知道这个修复是否对你有用。这个修复程序据说也适用于其他 Android 8.1 Oreo 设备，如谷歌 Pixel、谷歌 Pixel XL 和一加设备，如 OnePlus 5 和 OnePlus 5T，但尚未在这些设备上进行测试。该修复目前导致运行 [Android P Developer Preview](https://www.xda-developers.com/everything-new-android-p-developer-preview/) 的 Pixel 设备出现引导循环，因此如果您正在运行该版本，我们警告您不要立即刷新它。

*感谢 XDA 资深会员 Freak07 的提示！*