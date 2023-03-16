# 基于 Android Pie 的非官方 LineageOS 16 为 OnePlus 6 而生

> 原文：<https://www.xda-developers.com/unofficial-lineageos-16-android-pie-oneplus-6/>

LineageOS 16 将基于 Android Pie，尽管定制 ROM 尚未正式发布用于任何设备，但我们已经通过 XDA 认可的开发人员 [LuK1337](https://forum.xda-developers.com/member.php?u=5075128) 和 [luca020400](https://forum.xda-developers.com/member.php?u=5778309) 的非官方构建在 OnePlus 6 上尝到了它的味道。虽然这是一个早期版本，但它拥有 Android Pie 的所有主要功能，包括新设计的 recents 菜单、手势控制、自适应电池等！如果你有 OnePlus 6，你也可以通过一加[最近刚刚发布的](https://www.xda-developers.com/oneplus-6-oxygenos-open-beta-android-pie/)官方公开测试版来尝试 Android Pie。然而，如果你正在寻找一个稍微接近股票 Android 的东西，那么你来对地方了。

## 在 OnePlus 6 上安装非官方 LineageOS 16

这可能是你第一次遇到困难的地方。在安装 LineageOS 16 之前，你实际上必须在两个 [A/B 分区插槽](https://www.xda-developers.com/how-a-b-partitions-and-seamless-updates-affect-custom-development-on-xda/)上闪存一个 OnePlus 6 OxygenOS Open Beta(或 HydrogenOS Open Beta)。这个过程有点长，但并不难。**确保先做好备份。**

[button link = https://forum . xda-developers . com/OnePlus-6/development/rom-linea geos-16-0-t 3839750 " Icon = " Select a Icon " side = " left " target = " " color = " f 85050 " text color = " ffffff "]为 OnePlus 6 下载基于 Android Pie 的 LineageOS 16 非官方构建版[/button]

1.  下载 OnePlus 6 的最新公开测试版。这里可以找到那个[。](https://www.xda-developers.com/oneplus-6-oxygenos-open-beta-2-changelog/)
2.  为 OnePlus 6 下载最新的 Blu Spark TWRP。你可以在 XDA 资深会员 [eng.stk](https://forum.xda-developers.com/member.php?u=3873953) 的帖子[这里](https://forum.xda-developers.com/oneplus-6/development/kernel-t3800965)找到。**这是必要的，否则，你可能很难让 TWRP 随后工作。**
3.  启动恢复，闪存蓝光火花 TWRP(它会自动闪存到两个插槽)，并重新启动恢复。
4.  在 TWRP 的“擦除”部分擦除/系统和/数据。
5.  安装开放测试版 zip 文件，然后再次刷新 Blu Spark TWRP 安装程序**。**
***   重新启动以进行恢复，并重复步骤 4-5。这是为了确保 LineageOS 16 使用的固件文件安装在两个插槽上。*   擦除/系统和/数据和闪存线 geOS 16。*   再次重启以恢复。接下来，刷新 [GApps](https://www.xda-developers.com/open-gapps-arm-arm64-android-pie-roms/) 和 Magisk(如果你想的话),然后重启系统。**

 **就是这样！第一次启动时可能会有问题。我把它放了一会儿，直到我意识到它在靴子上冻住了。我用力重启我的手机(按住电源键十秒钟)，它很快就启动了。

## 实践:OnePlus 6 的第一个 LineageOS 16 构建

虽然这显然是一个非常早期的建设，我个人认为它值得日常驱动程序。除了几个功能和奇怪的 Snapchat 之外，几乎一切都正常。Snapchat 就是拒绝工作，不管什么原因。所有其他相机应用程序工作正常。我确实有一段时间 Snapchat 看起来工作得很完美，但后来它又回到了对着摄像头显示黑屏，并且无法显示我的朋友。

唯一不起作用的功能是 LineageOS 的实时显示和即时消息。我也不能让视频录制工作，但仅此而已。除此之外，这是一个令人惊讶的制作精良的构建，我在几个小时的使用中发现它非常类似于 OxygenOS 的流动性。这意味着你也可以获得全新的 Android Pie 用户界面，包括新的音量滑块和电源菜单。

附带的相机应用程序是缺乏的，但没有什么可以阻止你安装另一个相机应用程序。我个人在 OnePlus 6 上使用了谷歌相机 HDR+端口，它的性能绰绰有余。它完成了任务，现在着色问题已经解决，它完全有资格成为一名日常司机。

相对于 OxygenOS 的最新公开测试版，使用 LineageOS 值得吗？目前来看，还没有。虽然这是一个绝对伟大的非官方版本，但有一些问题是新发行的 ROM 的典型问题。例如，按下音量摇杆会在导航栏中调出自动旋转图标。窃听会锁住电话。这个图标在其他情况下也会出现，但我唯一一次能持续重现它的样子是按下音量摇杆。我敢肯定，再过几周，LineageOS 16 将成为 OnePlus 6 可用的最佳 Android 版本之一。不过现在，我建议等待并关注我们的论坛，让 Android 9 Pie 自定义 rom 变得更加稳定。

[**加入 XDA 一加 6 论坛**](https://forum.xda-developers.com/oneplus-6)**