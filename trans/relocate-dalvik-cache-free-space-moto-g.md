# 重新定位 Dalvik 缓存，用 Mod 在您的 Moto G 上获得更多空间

> 原文：<https://www.xda-developers.com/relocate-dalvik-cache-free-space-moto-g/>

# 重新定位 Dalvik 缓存，用 Mod 在您的 Moto G 上获得更多空间

通过重新定位 Moto G 上的 dalvik 缓存，访问 600MB 未使用的存储空间。

moto g

Android 设备上几乎没有剩余内存是一件令人失望的事情，尤其是当你已经尝试将文件、音乐、视频、照片和应用程序削减至最基本的内容时(毋庸置疑，范围很广)。对于没有 SD 卡插槽的设备的所有者来说，这可能非常令人沮丧，非 LTE 版本的 [Moto G](http://forum.xda-developers.com/moto-g) 也不例外。这是因为设备的内部 eMMC 存储有一个大约 600MB 的分区，称为/cache，不幸的是，令人沮丧的是，它没有被使用，因为应用程序的缓存存储在/data 中。因此，这就在你的手机上留下了 600MB 未使用的空间。

为了访问这个尚未开发的内存空间，XDA 高级成员 [Bert98](http://forum.xda-developers.com/member.php?u=4758250) 编写了一个教程，将 dalvik 缓存中的文件链接到/cache，为您提供额外的 600MB 内存，否则您将无法获得。然而，如果您安装了许多应用程序，超过 90 个应用程序，并且您正在运行 ART，则此解决方案可能不起作用。后一种限制的原因是 ART 比 dalvik 使用更多的内存，并且/cache 分区中的空间不足以容纳这种大小。

如果你不想自己经历这个过程，你也可以选择让国防部为你自动完成，这是 XDA 资深会员 [skyguy126](http://forum.xda-developers.com/member.php?u=6036514) 的好意。mod 的安装取决于你在 Moto G 上运行的是普通 ROM 还是定制 ROM，无论是哪种情况，都会提供说明。Skyguy126 还提供了安装过程中出现问题时的故障排除说明。

因此，如果额外的 600MB 内存空间听起来像是你感兴趣的东西，请前往 [Moto G dalvik 重定位教程线程](http://forum.xda-developers.com/moto-g/general/mod-save-data-space-cache-partition-t2942765)和 [mod 线程](http://forum.xda-developers.com/moto-g/general/mod-storage-reloacting-dalvik-cache-t2953616)了解更多信息。