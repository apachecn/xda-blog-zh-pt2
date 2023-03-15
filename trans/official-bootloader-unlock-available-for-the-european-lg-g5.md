# 欧洲 LG G5 官方启动解锁！

> 原文：<https://www.xda-developers.com/official-bootloader-unlock-available-for-the-european-lg-g5/>

欧洲 [LG G5](http://forum.xda-developers.com/lg-g5) 用户的好消息！基于欧洲的 H850 型号的官方引导加载器解锁现在可以从 LG 的开发者网站获得。

XDA 公认的贡献者和开发者 [autoprime](http://forum.xda-developers.com/member.php?u=2684188) 发布了一个逐步解锁 LG G5 引导加载程序的指南。一定要注意，这是**专门为欧洲 H850** 准备的。这些说明不适用于中东等其他地区的 G5，并且与美国运营商的设备型号不兼容。

由于这是官方解锁引导程序的方法，这个过程并不复杂，但也不像 Nexus 那样简单。这些步骤包括获取手机的设备 ID，并复制 bootloader 头下的两个字符串。

一旦你有了组合设备 ID，就去 LG 的开发者网站注册一个账户。注册是免费的，所以这应该只需要几分钟。导航到[解锁页面](http://developer.lge.com/resource/mobile/IssueDeviceInfo.dev)，从上面输入你手机的 IMEI 和设备 ID 字符串，点击确认按钮。你会收到一个 unlock.bin 文件。

接下来，您必须使用 fastboot 命令将这个 unlock.bin 文件刷新到您的手机上:

> 快速启动闪存解锁 unlock.bin

你完了！这个步骤会清除你手机上的数据并解锁你的手机，所以一定要准备好足够的备份。在此之后，您可以大胆地进入 root、定制 rom 和内核的世界，而不涉及任何其他复杂的过程！

凭借这一点，欧洲 H850 加入了 T-Mobile 的兄弟 H830，承担了一个可解锁的引导加载程序。其他运营商版本和地区版本就没有这么幸运了，因此，仍然需要等待更多关于引导程序解锁程序的信息。

如果你有一台欧洲 LG G5 H850，前往[论坛主题](http://forum.xda-developers.com/lg-g5/development/official-european-lg-g5-h850-bootloader-t3363040)了解引导程序解锁、root 和 TWRP 安装的详细步骤。

**你对欧洲 LG G5 正式获得 bootloader 解锁有什么想法？请在下面的评论中告诉我们你的想法！**

请继续阅读相关内容:

[**查看 XDA LG G5 论坛> >**](http://forum.xda-developers.com/lg-g5)