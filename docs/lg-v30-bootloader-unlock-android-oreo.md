# LG V30/V30+的 Android Oreo 更新意外地允许不受支持的型号解锁引导加载程序

> 原文：<https://www.xda-developers.com/lg-v30-bootloader-unlock-android-oreo/>

# LG V30/V30+的 Android Oreo 更新意外地允许不受支持的型号解锁引导加载程序

LG V30/V30+的 Android Oreo 更新意外地允许不支持的型号解锁其引导加载器。

社区对 LG V30 有着复杂的感觉，因为许多人希望该公司坚持使用该系列已经闻名的副屏幕。其他人也对 LG 的设计风格感到不安，这种设计风格使该设备看起来与市场上的其他设备非常相似。尽管如此，LG V30 被社区中的一些人视为 2017 年最好的智能手机，其唯一的缺点是 LG 的 bootloader 解锁过程。然而，XDA 成员 [TxanMoe](https://forum.xda-developers.com/member.php?u=6158380) 偶然发现了一种方法，允许我们解锁不支持的 LG V30 型号的引导加载程序，如一些美国运营商版本。

这一发现过程仍处于早期，但我们可以看到它适用于市场上的大多数 LG V30 型号。有趣的是，这种方法**将不会与 T-Mobile LG V30** 型号一起工作，因为它具有与其他方法不同的 RSA 加密。

这个过程需要你下载 Android Oreo us 998 KDZ 或 Oreo H930 KDZ 固件(取决于你的手机),然后下载 Oreo 兼容版本的 T2 TWRP T3。完成后，从线程、 [Magisk](https://www.xda-developers.com/tag/magisk/) 或 [SuperSU](https://www.xda-developers.com/tag/supersu/) 、加密禁用器和根检查禁用器中获取 unlock.bin 文件。Android Oreo 上的 LG V30 US998 或 H930 变体已经可以跳到下一步，但其他型号需要使用 Frankenstein 方法来转换到 Oreo US998。这实际上需要你先闪现牛轧糖 US998，然后再到奥利奥。欧洲 H930G 或任何地区的 H930DS 设备将需要使用 LGUP 转换到开放市场 H930。

完成后，您需要启用 OEM 解锁和 USB 调试模式，并将 new_unlock.bin 文件复制到您的设备。将 LG V30 引导至快速引导模式(又名引导加载程序模式)，然后使用快速引导刷新 new_unlock.bin 文件。那些之前解锁过 LG bootloader 的人可能对这个过程很熟悉，但整个事情的独特之处在于**我们使用的 unlock.bin 文件实际上来自华为 Mate 8 设备**。

LG V30 最近的 Android Oreo 更新中似乎有某种错误，允许这种工作，因为它已经被证明不能在旧版本的固件上工作。完成所有这些之后，你就可以继续安装 TWRP，如果你愿意的话，还可以获得你的设备的 root 权限。发现这个疯狂方法的用户制作了一个视频展示了下面的过程，XDA 公认的贡献者 [ChazzMatt](https://forum.xda-developers.com/member.php?u=3250376) 根据这个过程制作了一个冗长的文本指南。看看下面这两个。

* * *

[**解锁 LG v 30/v 30+**T3 的 bootloader](https://forum.xda-developers.com/lg-v30/help/wtf-lg-v30-t3790500)