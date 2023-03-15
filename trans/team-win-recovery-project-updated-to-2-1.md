# 团队胜利恢复项目更新至 2.1

> 原文：<https://www.xda-developers.com/team-win-recovery-project-updated-to-2-1/>

我们以前说过，现在我们再说一遍:基于触摸的恢复[是未来的](http://www.xda-developers.com/android/ext4-touch-recovery-for-the-gsm-evo-3d/)。除了让最终用户更容易地访问设备固件修改，他们还为 Android 黑客体验添加了一个非常需要的元素。虽然有些人可能会说这些升级恢复带走了激动和兴奋的感觉，但我认为它们提供了一个更有效的界面，并实现了一些真正独特的新功能，这些功能在过去的恢复中是不可用的。

在可以说是最受欢迎的基于触摸的恢复的一次相当大的更新中，XDA 认可的开发者 [Dees_Troy](http://forum.xda-developers.com/member.php?u=912474) 向我们展示了 Team Win Recovery Project(简称 TWRP)版本 2.1。除了简单地带来一个友好的用户界面，TWRP 2.1 还通过提供 zip 队列、基本的文件管理器和备份的双存储支持，打包了一个健康的功能。

TWRP 通过一个名为 *OpenRecoveryScript* 的新脚本引擎支持脚本，与 [GooManager](https://play.google.com/store/apps/details?id=com.s0up.goomanager) 一起使用。通过 ORS，用户可以在安卓系统中安装多个 *update.zip* 文件，清除缓存& dalvik，并运行备份。此外，以开放的名义，Team Win [已经将 ORS 提交给 ClockworkMod。](http://review.cyanogenmod.com/#change,14650)

用开发商的话说:

> Team Win Recovery Project 2.0(简称 twrp2)是一个定制的恢复工具，旨在方便使用和定制。我们从零开始，采用 AOSP 恢复并加载标准恢复选项，然后添加了许多我们自己的功能。这是一个完全触摸驱动的用户界面——不再需要音量摇杆或电源按钮。GUI 也完全是 XML 驱动的，完全是主题化的。你可以改变外观和感觉的每一个方面。

恢复软件版本 2 的新功能:

> TWRP 1.1.x 中出现的 Zip 排队又回来了
> 
> 支持双存储(从内部或外部存储备份、恢复和安装 zips 由您选择)
> 
> 滑块控制(滑动以确认大多数操作，也称为滑动以擦除)
> 
> 锁屏(用滑块解锁)
> 
> 基本文件管理器(复制，移动，删除和 chmod 任何文件)
> 
> 增加了对/data/media 设备的支持(大多数蜂窝平板电脑、Galaxy Nexus 等新型 ICS 设备)
> 
> 在备份菜单中显示每个分区的大小
> 
> 添加了列表框 GUI 元素(目前用于列出时区)
> 
> 更新的股票 XML 布局更加一致，更容易移植到不同的分辨率
> 
> XML 布局文件要小得多
> 
> 对于某些设备，分区可用备份更准确
> 
> 删除了不需要的错误消息(/misc 错误，无法统计 sd-ext 等。)
> 
> 修正了 blkid 检测代码的错误
> 
> 修正了在 zip 安装过程中每行文本之间插入一个空行的错误
> 
> 修正了一个错误，在安装压缩文件时，一个无效的压缩文件会导致 TWRP 在安装压缩文件时卡住
> 
> 增加了主题切换模拟模式的设置，使主题更容易
> 
> 新增设备- Galaxy Nexus GSM & CDMA(仅预览，手动安装)，宏碁 Iconia Tab A500，HTC Vivid，摩托罗拉 Defy
> 
> 添加了对的支持。主题引擎中的 jpg 图像
> 
> 更改了库存平板电脑主题的图像-使平板电脑尺寸缩小了约 500KB
> 
> 从图形用户界面中移除不需要的非图形用户界面图像——使所有构建小了大约 100KB

如果你渴望开始，请访问下面列出的开发线程。相反，如果你正在寻找复苏主题，请访问他们的[主题指南](http://www.teamw.in/project/twrp2themers)。