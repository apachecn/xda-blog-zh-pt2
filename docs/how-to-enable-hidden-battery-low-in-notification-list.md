# 如何在通知列表中启用隐藏的“电池电量低”。

> 原文：<https://www.xda-developers.com/how-to-enable-hidden-battery-low-in-notification-list/>

XDA 成员 [FRANQ_23_PL](http://forum.xda-developers.com/member.php?u=2427711) 写了一个指南来启用低电量通知，还提供了一种在 Windows Mobile 设备上更改通知声音的方法。

由于您必须导入开发人员提供的注册表设置，Resco 注册表编辑器或类似的程序需要这样做。还提供了一个注册表黑客来解锁所有通知方法。

请确保在继续之前备份您的注册表。

本指南是为 HTC Leo 设计的，但也适用于其他设备。

> *原帖由****FRANQ _ 23 _ PL***
> 
>  *[MOD]在通知列表中启用隐藏的“电池电量低”+自定义声音[更新于 25 月 6 日]
> 
> 你好！
> 
> *我昨天生气的时候发现，我听不到声音通知，*
> 
> 我的电池电量很低，当我需要它工作的时候，我的手机会在外面关机。
> 
> *我的第一个“发现”(也许每个人都知道，对我来说这是新的)是在\Windows\*
> 
> 是声音文件 lowbatt.wav，这个文件是低电量通知的声音，所以我们可以用任何我们想要的声音来替换。
> 
> *我在寻找这个文件的注册表关联，然后我发现了如何启用“低电量”状态*
> 
> 在设置>声音和通知>选项卡“通知”>第一个下拉列表中。
> 
> 要启用此选项，请从附件导入注册文件。这可能是因为在这个下拉列表中出现“电池电量低”选项。
> 
> 如果你想在你的语言中有这个位置，有源代码，你可以从 las 行修改“电池电量低”,
> 
> 复制这整个代码，粘贴到 PC 记事本，并保存为“*”。* "和文件名*。注册，并在下一步发送到手机
> 
> 并导入到带有 Resco 注册表的注册表中:*

 *你可以在[注册表黑客的线程](http://forum.xda-developers.com/showthread.php?p=7246322#post7246322)中找到更多信息。*