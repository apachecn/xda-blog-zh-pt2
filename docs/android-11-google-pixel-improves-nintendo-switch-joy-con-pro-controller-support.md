# 任天堂 Switch 控制器在 Android 11 的谷歌 Pixel 上工作得更好

> 原文：<https://www.xda-developers.com/android-11-google-pixel-improves-nintendo-switch-joy-con-pro-controller-support/>

# 谷歌 Pixel 上的 Android 11 极大地改善了任天堂 Switch Joy-Con 和 Pro 控制器的支持

谷歌 Pixel 上的 Android 11 通过消除延迟，大大改善了对任天堂 Switch Joy-Con 和 Pro 控制器的支持。

由于微软即将推出的 xCloud 服务，云游戏成为了移动游戏讨论的焦点，我们一直在关注 Android 上的控制器支持状况。回到 Android 11 Beta 1，我们注意到谷歌增加了惊人的 [84 个新控制器映射](https://www.xda-developers.com/android-11-84-new-gaming-controller-mappings/)，这意味着新的 Android 版本可以识别来自 84 个新游戏控制器的输入。许多新支持的控制器来自第三方游戏配件制造商，因为 Android 已经支持三大游戏机的原始游戏控制器。虽然 Android 自 2017 年以来一直支持连接到任天堂 Switch Joy-Cons [和自 2019 年](https://www.xda-developers.com/nintendo-switchs-joy-con-controllers-natively-pair-with-android-but-lag/)以来支持连接到 Pro 控制器[，但这两个控制器的延迟是无法忍受的。不过，谢天谢地，谷歌终于修复了 Pixel 手机 Android 11 版本的主要连接和延迟问题。](https://www.xda-developers.com/android-10-nintendo-switch-pro-controller-mapping-support/)

这里是我录制的两个视频，展示了任天堂 Switch 游戏机与运行 Android 10 的谷歌像素 4 和运行 Android 11 的谷歌像素 3a XL 的对比。请注意，在 Pixel 3a XL 的视频中，同步状态的 led 指示灯没有失控，我的输入几乎立即被识别出来，操纵杆似乎向各个方向发送输入。

我在这两个视频中玩的游戏是*超级马里奥阳光*，一款使用海豚模拟器模拟的任天堂 GameCube 游戏。Dolphin Emulator 在配有[骁龙 855](https://www.xda-developers.com/qualcomm-snapdragon-855-kryo-485-cpu-adreno-640-gpu-spectra-isp-cv/) 的 Pixel 4 上运行得更好，而在配有[骁龙 670](https://www.xda-developers.com/qualcomm-snapdragon-670-chipset/) 的 Pixel 3a XL 上运行得更好，但你仍然可以清楚地看到改进后的控制器支持的差异。

不过，谷歌 Pixel 上改进的任天堂 Switch Joy-Con 和 Pro 控制器支持并不一定是因为 Android 11 的更新。针对 Pixel 的 Android 11 更新恰好有[必要的内核驱动](https://android-review.googlesource.com/q/%2522hid-nintendo%2522)来提高兼容性。内核驱动程序增加了对 Joy-Cons 和 Pro 控制器的适当支持，只需要“很少或不需要用户校准”。然而，Joy-Con 仍然被视为独立的输入设备，因此您可能需要使用 [Joy-Con Enabler 应用程序](https://www.xda-developers.com/joy-con-enabler-lets-you-use-both-joy-cons-on-a-rooted-android-4-1-device/)来让某些应用程序将它们识别为单个控制器。

*感谢 XDA 会员[章程](https://forum.xda-developers.com/member.php?u=9648761)的提示！*