# 用于较小内核调整的基本内核厨房

> 原文：<https://www.xda-developers.com/basic-kernel-kitchen-for-minor-kernel-tweaking/>

我们通常鼓励那些想学习如何开发的人通过开发代码来这样做[，而不是使用厨房。但是，每个人的入门都不一样。这意味着一些有抱负的开发人员可能想在实际创建真正的开发工作之前尝试一些简单的东西，比如 ROM 厨房。对于那些希望开始学习更多内核知识的人来说也是如此。](http://www.xda-developers.com/android/sage-advice-from-cyanogen-still-valid-today/ "Sage Advice from Cyanogen Still Valid Today")

正是考虑到这一点，XDA 公认的贡献者 [championswimmer](http://forum.xda-developers.com/member.php?u=4308696) 发布了一个旨在修改内核的厨房。这个项目背后的动机来自 XDA 公认的开发者和退休的高级主持人 [dsixda](http://forum.xda-developers.com/member.php?u=673068) 的现在传奇的 [ROM 厨房](http://forum.xda-developers.com/showthread.php?t=633246)，championswimmer 希望为内核创建一个类似的厨房，以帮助新用户开始做一些小的修改。

厨房主要是让用户从一个 *boot.img* 文件中提取 Zimage 和 ramdisk，将 zImage 和 ramdisk 合并成一个 *boot.img* 文件，并修改启动闪屏。正如开发商所描述的:

> 完全菜单驱动界面(如 dsixda kitchen)
> 
> 从 boot.img 文件中提取 zImage 和 ramdisk
> 
> 从 zImage 和 ramdisk 创建 boot.img
> 
> 从任何包含 kernel.sin 的 ftf 文件中提取 zImage 和 ramdisk(Xperia 2010、2011、2012)
> 
> 从 zImage 和 ramdisk 创建可刷新的 ftf(仅限 Xperia 2010)
> 
> 从 ramdisk 文件夹创建压缩的 ramdisk 二进制文件
> 
> 从 ramdisk 二进制文件中提取 ramdisk 文件
> 
> 将 png 图像转换为 rle 格式(用于 android 启动启动图像)
> 
> 转换 rle 启动飞溅到 png 文件(以便您可以编辑它)

和 dsixda 的厨房一样，这个厨房是一个菜单驱动的脚本，打算在 Linux 上运行。有了这个厨房，初级内核开发人员可以对内核的各个部分进行一些小的调整。

然而，championswimmer 确保提醒新用户:

> 我想在这里补充一点...我们不应该把它当作一台庞大复杂的机器，扔进去一只靴子，又拿回来一只
> 
> 我真的非常希望想要成为内核开发者的人也能仔细检查一下内部结构...看脚本，读源文件，试着理解厨房里发生了什么，而不仅仅是把它当作一台“封闭的机器”

那些想要了解更多的人应该前往[原始线程](http://forum.xda-developers.com/showthread.php?t=1659584)。