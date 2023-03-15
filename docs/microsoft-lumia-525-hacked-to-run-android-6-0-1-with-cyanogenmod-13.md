# 微软 Lumia 525 被黑运行 Android 6.0.1 搭配 CyanogenMod 13

> 原文：<https://www.xda-developers.com/microsoft-lumia-525-hacked-to-run-android-6-0-1-with-cyanogenmod-13/>

你可能听说过微软诺基亚 Lumia 525。不管怎样，我们都不会怪你。这是一款不起眼的小设备，配有 4 英寸 800x480 IPS 显示屏，由高通骁龙 S4 SoC 供电，1GB 内存和 8GB 存储空间。

该设备还配有 Windows Phone 8(更新至 Windows Phone 8.1)，面向预算细分市场。在软件方面，一个开发者已经找到了将手机从被抛弃的微软软件的束缚中解放出来的方法。微软没有更新设备 Windows 10，所以开发者做了退而求其次的解决方案:他们下载了最新的 Android！

XDA 资深成员 banmeifyouwant(T1)研究出如何让 T2 在 Lumia 525(T3)上运行安卓系统。不仅仅是任何一个安卓系统，它仍然是面向公众的“最新”官方安卓版本，安卓 6.0 棉花糖([除非谷歌决定明天发布安卓 7.0 牛轧糖](http://www.xda-developers.com/xda-external-link/canadian-carrier-telus-drops-hint-for-android-7-0-releasing-on-august-22nd/))。微软抛弃的手机现在运行一个几款安卓手机都没有的软件！

开发者从设备中完全移除了 Windows Phone 和 UEFI 元素，并刷新了[小内核引导加载程序](https://developer.qualcomm.com/download/db410c/little-kernel-boot-loader-overview.pdf)、TWRP 和 CyanogenMod 13 的一个端口。这使得开发人员能够启动 Android，并向我们展示视频作为概念证明。

接下来， [banmeifyouwant](http://forum.xda-developers.com/member.php?u=7062343) 还发布了一个视频，视频中他在运行 CyanogenMod 13 的同时在设备上运行 AnTuTu benchmark。

ROM 仍处于早期阶段，远没有达到一般用户所期望的稳定性。显示屏和触摸屏可以工作，但需要稍微校准，但除此之外，WiFi、调制解调器等几个关键领域都无法工作。但是，这是从本质上面向开发人员的阿尔法级软件所期望的。

ROM 和修改适用于 Lumia 525，但尚未发布。这套软件也可以修改，以适用于 Lumia 520，这是同一款手机，但内存较小。开发人员希望首先发布 Lumia 525 的安装程序和相关源代码，但他设备上的 eMMC 已经让步，因此，预计会有一些延迟。

Lumia 525 和 Lumia 520 以外的设备会得到吗？同一个开发者还没有提到他的计划，所以我们请求读者不要用相同的请求淹没[论坛线程](http://forum.xda-developers.com/windows-phone-8/general/android-6-0-1-cm13-lumia-525-t3442630)。如果您是一名开发人员，那么一旦源代码发布，您就可以为您的设备选择项目。

即使作为概念验证，对于两年前推出的廉价 Windows phone 设备来说，这也是一个不可思议的成就。我们希望这种发展继续下去，并在各种设备间传播。

你对这一发展有什么看法？请在下面的评论中告诉我们！