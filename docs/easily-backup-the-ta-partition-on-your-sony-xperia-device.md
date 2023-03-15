# 轻松备份索尼 Xperia 设备上的 TA 分区

> 原文：<https://www.xda-developers.com/easily-backup-the-ta-partition-on-your-sony-xperia-device/>

前段时间我们谈到了索尼 Xperia 设备上[备份 TA 分区的重要性。在索尼 Xperia 设备上这样做可以保存您的 DRM 密钥。为什么这很重要？要使用一些专有软件，如 Gallery 应用程序中的 Bravia Engine 和 OTA 更新，需要这些键。](http://www.xda-developers.com/android/tutorial-to-backup-your-ta-partition-on-the-sony-xperia-z/)

然而，正如我们之前所了解的，一旦你第一次解锁你的引导程序，这些 DRM 密钥就会不可挽回地丢失，除非你之前创建了备份。幸运的是，有[很棒的教程](http://forum.xda-developers.com/showthread.php?t=2234627)教你如何备份你的 TA 分区，前提是你要在初始引导程序解锁之前备份。

现在，多亏了 XDA 论坛成员 [DevShaft](http://forum.xda-developers.com/member.php?u=5261329) ，有一个精简的 Windows 批处理文件可以帮你做到这一点。您只需下载最新版本，连接启用 ADB 的设备，运行批处理文件，然后从菜单选项中进行选择。

显然，如果你已经解锁了没有备份的引导程序，并且已经丢失了 DRM 密钥，这是没有用的。然而，如果你想第一次解锁你的引导程序，就去使用[原始线程](http://forum.xda-developers.com/showthread.php?t=2292598)来轻松备份你的 TA 分区。下面列出了已知和假定支持的设备。

> **支持的设备**
> 
> **确认:**
> 
> 索尼 Xperia Z Ultra
> 
> 索尼 Xperia Z
> 
> 索尼 Xperia ZL
> 
> 索尼 Xperia ZQ
> 
> 索尼 Xperia ZR
> 
> 索尼 Xperia ION
> 
> 索尼 Xperia S
> 
> 索尼 Xperia SL
> 
> 索尼 Xperia SP
> 
> 索尼 Xperia Acro S
> 
> 索尼 Xperia T
> 
> 索尼 Xperia TL
> 
> 索尼 Xperia TX
> 
> 索尼 Xperia M
> 
> 索尼 Xperia V
> 
> 索尼 Xperia P
> 
> 索尼 Xperia L
> 
> 索尼 Xperia U
> 
> 索尼 Xperia Sola
> 
> 索尼 Xperia Miro
> 
> 索尼 Xperia Tipo
> 
> 索尼 Xperia J
> 
> 索尼 Xperia E
> 
> 索尼 Xperia Tablet Z
> 
> **最有可能:**
> 
> 所有索尼 Xperia 型号
> 
> **不支持:**
> 
> 所有索尼爱立信 Xperia 型号