# T-Mobile 一加 6T 现在可以在不解锁引导程序的情况下更名

> 原文：<https://www.xda-developers.com/t-mobile-oneplus-6t-international-without-unlocked-bootloader/>

# T-Mobile 一加 6T 现在可以在不解锁引导程序的情况下更名

XDA 初级成员 AnonymousTipster 分享了一种在没有解锁的引导加载程序/SIM 解锁的情况下将 T-Mobile 一加 6T 转换为国际版的方法。

围绕一加 6T 的一个大故事是 T-Mobile 合作伙伴关系。这在美国是一件大事，很多人从运营商那里购买他们的设备。因此，一加 6T 的销量比以前的设备好得多，但也不全是好事。T-Mobile 型号的[在更新上落后了](https://www.xda-developers.com/t-mobile-oneplus-6t-update-screen-unlock-camera/)，但是有办法转换成国际(即非 T-Mobile)版本。

以前将 T-Mobile 一加 6T 转换为国际 ROM 的方法的唯一问题是，你需要一个解锁的引导程序，这需要 SIM 卡解锁，这是 T-Mobile 已知的一个痛苦。如果你使用这种方法，这意味着没有来自网飞和 Hulu 等流媒体服务的受高清数字版权保护的视频。

令人欣慰的是，XDA 的初级成员 [AnonymousTipster](https://forum.xda-developers.com/member.php?u=9557721) ，以及[黑暗梦魇](https://forum.xda-developers.com/member.php?u=4204048)和[国际航空运输协会](https://forum.xda-developers.com/member.php?u=5467580)的努力，分享了一种在没有解锁引导加载程序/SIM 解锁的情况下将 T-Mobile 一加 6T 转换为国际的方法。你将运行与解锁的一加 6T 相同的软件，你甚至可以加入 [OxygenOS 开放测试程序](https://www.xda-developers.com/oxygenos-beta-2-10-oneplus-6t-6-caller-id-india-nav-bar-color-adaptation/)。下面列出了这些步骤，由 AnonymousTipster 提供。

## 如何重塑 T-Mobile 一加 6T 的品牌

**注意:这个过程会擦手机。请在继续之前备份手机中的所有重要文件。**

1.  下载 [iaTa](https://forum.xda-developers.com/member.php?u=5467580) 提供的[一加 6T MsmDownloadTool v 4 . 0 . 58(OOS v 9 . 0 . 11)](https://forum.xda-developers.com/oneplus-6t/how-to/tool-6t-msmdownloadtool-v4-0-oos-9-0-5-t3867448)
2.  点击这里下载打了补丁的 flasher 工具[。补丁只是删除了允许所有图像在一加 6T 上闪烁的检查。AnonymousTipster 表示，他们亲自测试了“MsmDownloadTool v 4.0 _ factory _ patched . exe”，但没有测试“MsmDownloadTool v 4.0 _ factory _ MCL _ op1 _ patched . exe”变体。他们说你可以对可执行文件和原始文件进行二进制比较，以防你对文件的信任有任何问题。](https://drive.google.com/open?id=1dYuVxnf_J97KPrRt6KEBOjau1BRvtnJQ)
3.  完全关闭你的 T-Mobile 一加 6T。
4.  同时按住音量增大键和音量减小键。
5.  按住这两个按钮，将 USB 线插入电脑。
6.  确保 Qcom 下载模式的 USB 驱动程序已安装并且正在运行(可在 MSMDownloadTool 线程中找到)。
7.  将修补后的工具可执行文件解压缩到与 MSMDownloadTool 相同的目录中。
8.  运行“MsmDownloadTool v 4.0 _ factory _ patched . exe”
9.  当您准备好开始修补设备时，请单击“开始”。
10.  大约 5 分钟后，它将完成工作并重新启动设备。
11.  你的手机将正常启动，但没有更多的 T-Mobile 标志。相反，您将看到 OxygenOS 通用徽标。

[**详见一加 6T 论坛**](https://forum.xda-developers.com/oneplus-6t/how-to/t-mobile-6t-to-international-t3888307)