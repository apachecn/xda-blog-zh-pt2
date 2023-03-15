# 索尼 Flashtool 更新至 v0.9.23.0，支持牛轧糖 FTF

> 原文：<https://www.xda-developers.com/flashtool-for-sony-updated-to-v0-9-23-0-with-support-for-nougat-ftf/>

# 索尼 Flashtool 更新至 v0.9.23.0，支持牛轧糖 FTF

索尼设备的 Flashtool 已经更新，支持基于牛轧糖的 FTF 文件，以及更多这样的功能！前往了解更多信息！

拥有索尼设备并对其进行过任何软件修补的用户肯定听说过 XDA 知名开发商 Androxyde 的 Flashtool。对于外行人来说，Flashtool 为索尼设备所有者提供了在升级和降级的库存包中自由移动的权利，并且曾经被用作刷新修改过的“定制”rom 的手段(在恢复得到普及之前)。

Flashtool 的流行源于它的使用案例以及它支持的设备数量。这款基于个人电脑的软件适用于所有索尼手机，从 2009 年发布的 Xperia X10 一直到 T2 的 Xperia Z Ultra 和更新的手机。现在，Flashtool 的用例以支持牛轧糖 FTF 闪烁的形式增加了另一个里程碑。

Flashtool v0.9.23.0 更新的变更日志如下:

*   修正牛轧糖 sin 文件解析。FT 现在应该可以闪现牛轧糖 FTF 了
*   TA 对所有暴露于 dirtycow 漏洞的设备进行原始备份。[使用雷曼的 dirtycow 进行数据备份](http://forum.xda-developers.com/crossdevice-dev/sony/universal-dirtycow-based-ta-backup-t3514236)
*   用于创建 fsc 脚本的更精确的 USB 日志解析器
*   在高级模式下，一些新的 TA 功能:查看器和自定义 TA 文件生成器或 flashing
*   添加了一个新的设备属性来告诉 fsc 是否是强制性的。该属性的检查在闪烁之前完成

除了其所有的闪存使用案例之外，Flashtool 还有助于 TA 备份。TA 备份通常是为了保护索尼设备上的 DRM 密钥，否则如果用户决定解锁引导加载程序，这些密钥将无法挽回地丢失。该更新使用最近的 [DirtyCow 漏洞](https://www.xda-developers.com/9-year-old-linux-kernel-bug-dubbed-dirty-cow-can-root-every-version-of-android/)来允许 TA 分区备份。

要下载最新的 Flashtool，请前往其网站主页。另外，你也可以访问[论坛的帖子](http://forum.xda-developers.com/showthread.php?t=920746)。由于该软件是开源的，你也可以在 [Github](https://github.com/Androxyde/Flashtool) 上查看它的源代码。

你以前用过 Flashtool 吗？你对这个软件有什么体验？请在下面的评论中告诉我们！