# 使用 Got Brickbug 确定您设备的硬件故障风险

> 原文：<https://www.xda-developers.com/determine-your-devices-hard-brick-risk-with-got-brickbug/>

到目前为止，我们都很熟悉在更新到 IC 的泄露版本时困扰各种三星的[硬砖错误。这个 bug 已经出现在各种基于三星 Exynos 4210 的设备上，包括](http://www.xda-developers.com/android/hard-brick-bug-on-galaxy-s-ii-and-note-leaked-ics-kernels/ "Hard Brick Bug on Galaxy S II and Note Leaked ICS Kernels") [Galaxy Note GT-N7000](http://forum.xda-developers.com/forumdisplay.php?f=1346) 、 [Epic 4G Touch](http://forum.xda-developers.com/forumdisplay.php?f=1281) 、[AT&Galaxy S II](http://forum.xda-developers.com/forumdisplay.php?f=1301)以及韩国的 SHW-M250S/K/L

然而，我们很快发现，并不是所有的 eMMC 修订版都受到同样的困扰。相反，0x19 修订版被突出显示为已知错误，而 0x25 被认为是安全的。0x19 和 0x25 之间的版本被认为可能是坏的，而比 0x25 新的版本可能是安全的。雪上加霜的是，热衷于十六进制的人会很快注意到，0x19 换算成十进制就是 25！

自然，有人会创造一种更简单的方式来确定你的设备的状态，而那个人就是 XDA 精英公认的开发者。通过他的新应用 Got Brickbug，用户可以轻松地检查他们的设备，以查看他们对硬砖错误的风险状态。正如 Chainfire 自己解释的那样:

> 附上一个简单的 APK，读出你的芯片的类型和 CID，并让你知道我们是否知道芯片是危险的或安全的。
> 
> 使用后再次卸载即可。
> 
> 显然，这是“按现状”来的，我们对你用你的设备做什么不负责，等等。程序的输出不能派生出任何权限！
> 
> 使用的内部数据:
> 
> MAG4FA、VYL00M 或 KYL00M fwrev 0x19 ->已知不良
> 
> MAG4FA、VYL00M 或 KYL00M fwrev >= 0x25 ->可能安全
> 
> MAG4FA，VYL00M，或者 KYL00M fwrev！= 0x19 && < 0x25 -->可能不好
> 
> 其他一切:未知芯片

由于这是任何 flash 爱好者的相关信息，我们建议您前往[应用程序线程](http://forum.xda-developers.com/showthread.php?t=1693704)来测试您的设备。

[图片摘自 egzthunder1 关于此事的[精彩文章](http://www.xda-developers.com/android/hard-brick-bug-on-galaxy-s-ii-and-note-leaked-ics-kernels/)。]