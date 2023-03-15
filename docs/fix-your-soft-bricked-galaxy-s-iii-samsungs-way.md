# 用三星的方式修理你的软砖 Galaxy S III

> 原文：<https://www.xda-developers.com/fix-your-soft-bricked-galaxy-s-iii-samsungs-way/>

说到砌砖，不管是硬砖还是软砖，我们通常都有自己的做法。无论是[创建夹具迫使手机进入下载模式](http://www.xda-developers.com/android/what-is-the-samsung-anyway-jig/)还是 [unbrick mods 让死去的手机起死回生](http://www.xda-developers.com/android/htc-rezound-added-to-the-htc-unbricking-project/)，我们一直以这样一种方式运作，我们并不真正需要 OEM 支持。这并不是说我们不喜欢 OEM 支持，但他们很少分发他们的维修指南。

XDA 资深会员 [Net.silb](http://forum.xda-developers.com/member.php?u=4354560) 已经设法获得了[三星 Galaxy S III](http://forum.xda-developers.com/forumdisplay.php?f=1563) 的官方砖修指南。这绝对是一篇令人兴奋的阅读，它概述了三星如何处理三星 Galaxy S III 设备。这是一个非常复杂的过程，需要硬件和软件专业知识来修复。所以不建议新手使用。根据手册，您将经历以下过程:

> -GT-I 9300 的简要 JTAG 流程
> 
> 1)使用普通 GT-I9300 将 JTAG(引导加载程序)文件复制到外部 SD 卡。
> 
> 2)将 SD 卡插入“无电”手机，并将引导程序文件复制到有缺陷的 PBA。
> 
> 3)将引导程序文件下载到有缺陷的手机后，使用手机进入下载模式，并下载完整的软件(PIT、PDA、CSC、手机文件)

简而言之，你会把 bootloader 装在 SD 卡上，放在手机里，用几个硬件的小技巧让它下载到手机上，用 Odin 来刷新固件。还有一个图片和参考难以捉摸的[三星反正夹具](http://www.xda-developers.com/android/what-is-the-samsung-anyway-jig/)。此外，它表明当您使用这种方法时，您将通过一种称为 SDCard 的模式来刷新引导加载程序。

如果你遵循这个过程，你将从一个以前的软砖设备中获得一个功能正常的 Galaxy S III。然而，这仅仅是这份文件意义的一半。这里的大奖是看三星的技术人员如何做到这一点。如果你想了解更多信息，请查看[原始线程](http://forum.xda-developers.com/showthread.php?t=1916796)。

然而，正如 Elite 公认的开发商 AdamOutler 指出的那样:“这里不是 JTAG。它是联合行动试验小组的替代机构，与 JTAG 无关。当你短路一个电阻后，它会从 SD 启动 Odin。它比 JTAG 更接近于“不死之身”