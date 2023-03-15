# 一些 Pixel 2 用户报告无法解锁引导程序

> 原文：<https://www.xda-developers.com/google-pixel-2-users-reporting-inability-unlock-bootloader/>

2017 年 11 月 21 日更新:谷歌已经发布了一个工厂重置现在将解决这个问题，这在过去没有产生任何结果。

[Pixel 2](https://forum.xda-developers.com/pixel-2) 和 [Pixel 2 XL](https://forum.xda-developers.com/pixel-2-xl) 是旨在展示谷歌软件体验的旗舰设备。但这些手机也有自己的问题，从 Pixel 2 的[无法闪现工厂图像和 OTA 的](https://www.xda-developers.com/pixel-2-failing-flash-factory-images/)和[高音耳机噪音](https://www.xda-developers.com/high-pitched-clicking-google-pixel-2/)到 Pixel 2 XL 的[显示器老化](https://www.xda-developers.com/google-pixel-2-xl-display-burn-issues/)和[音频录制问题](https://www.xda-developers.com/google-fix-audio-recording-pixel-2-xl/)。

不幸的是，问题还不止于此。一些从谷歌商店购买设备的 Pixel 2 用户报告称无法解锁他们手机的引导程序。

问题源于**开发者选项中的 **OEM 解锁**设置。**切换按钮变灰，无法启用。受影响的设备会显示连接到互联网的提示，即使手机已连接到互联网，或者建议用户联系服务提供商。

谷歌客服代表无法确认该问题是硬件问题还是软件问题。

只有一小部分用户报告了这个问题，所以它似乎并不普遍。然而奇怪的是，大多数人从谷歌商店订购 Pixel 2，并将交付时间推迟了多达三周。一些人推测，谷歌无意中向这些客户发送了锁定引导程序的威瑞森模型。

除了把你的手机归还给谷歌并要求更换之外，没有什么自己动手的解决办法。用户报告使用 [ADB 侧载](https://twrp.me/faq/ADBSideload.html)进行工厂重置和刷新工厂图像没有效果。

如果你遇到了这个问题，去 [Google Bug Tracker 开始](https://issuetracker.google.com/issues/68897739)并添加评论。

* * *

**更新 2017 年 11 月 21 日**:此问题[现已修复](https://issuetracker.google.com/issues/68897739#comment119)。用户现在只需在工厂重置手机，并将其连接到互联网进行初始设置即可解锁。

> 标记为固定。请将您的设备重置为出厂设置，并确保它在设置过程中连接到互联网，因为此问题已经解决。
> 
> 恢复出厂设置:设置->系统->重置选项->清除所有数据(恢复出厂设置)。

* * *

*感谢 XDA 资深会员[文龙](https://forum.xda-developers.com/member.php?u=3829405)的提示！*