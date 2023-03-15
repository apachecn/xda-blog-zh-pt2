# rCast 将你的 Chromecast 变成一个独立的媒体播放器

> 原文：<https://www.xda-developers.com/turn-your-1st-gen-chromecast-into-a-stand-alone-media-player/>

智能电视的出现给我们带来了很多享受。它允许我们将(大部分)屏幕打开时间整合在一台设备上(无需并排的屏幕)，并且允许我们在电视上做以前没有高价游戏控制台或计算机系统的帮助就无法做的事情。

最重要的是，这一趋势也催生了将“哑”电视变成智能电视的廉价解决方案。一个这样的解决方案是谷歌对库比蒂诺苹果电视的回应，Chromecast。这个小设备自 2013 年 7 月进入市场以来并没有太大的变化(通过与最新版本的 HDMI 加密狗进行比较就可以看出这一点)。然而，正是因为有了像 XDA 资深会员 [rundgong](http://forum.xda-developers.com/member.php?u=4687087) 这样的开发者，这款设备(和拥有者)才为它区区 35 美元的价格赢得了更多的好评。

Chromecast 在没有互联网连接的情况下基本上是无用的，谷歌通过添加大量锁来防止定制固件之类的事情，从而确保了这一点。事实上，这是它的致命弱点...或者至少曾经是。[输入 rCast](http://forum.xda-developers.com/hardware-hacking/chromecast/rom-rcast-chromecast-standalone-media-t3218203) 。这是一个定制的 ROM，基本上使用户能够通过启用本地媒体播放来充分利用 Chromecast 的内部存储器。此外，该设备不需要互联网连接就能工作。开发人员继续解释说，ROM 使用打了补丁的二进制文件对 Google 服务器进行 ping 操作，然后将 ping 操作定向到本地服务器。

> cast_shell 和 net_mgr 向 google 服务器发出 http 请求。我已经修补了这些二进制文件，所以它们改为向本地 web 服务器发出请求。
> 
> *-设备向服务器 8.8.8.8 发送 dns 查询。我通过在本地主机上为 8.8.8.8 创建一个别名并运行一个 dns 服务器来解决这个问题。*
> 
> 在从 pool.ntp.org 收到更新的时间之前，设备不会完成启动。通过在 hosts 文件中将 pool.ntp.org 添加为 127.0.0.1，并在本地运行 sntp 服务器，可以解决此问题。
> 
> *这些解决方法将使设备即使在网络中断的情况下也能正常启动。*

不用说，该设备必须能够在其上刷新定制固件，因为这是一个基于 Eureka 的 ROM。如果你想用你的旧 Chromecast 做一些“有趣”的事情，就去试试吧。

你可以在 [rCast 原始线程](http://forum.xda-developers.com/hardware-hacking/chromecast/rom-rcast-chromecast-standalone-media-t3218203)中找到更多信息和完整指南。