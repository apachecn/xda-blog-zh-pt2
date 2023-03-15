# UC 浏览器下载管理器

> 原文：<https://www.xda-developers.com/download-manager-for-uc-browser/>

说到网页浏览器，我们都有自己的最爱。对于那些喜欢 UC 浏览器的人，你会发现下面的下载管理器调整非常方便。XDA 成员 [imbunned](http://forum.xda-developers.com/member.php?u=2056651) 制作了 2 个文件，一个用于将文件下载到你的 Windows mobile 设备，另一个用于在使用 UC 浏览器时将 Coreplayer 设为你的默认视频播放器。

Imbunned 还为我们提供了一些全屏观看视频的代码，以及另一个无需下载文件即可观看视频的代码。

> *原帖由* ***转贴***
> 
>  *按取消-输入地址-tab 并按住-全屏编辑和开始菜单-下载与 ucweb
> 
> *非常有用*
> 
> *代码:*
> 
> 鼠标点击(activeWin，100)
> 
> 鼠标点击(activeWin，100)
> 
> 睡眠(20)
> 
> SendCtrlKey( activeWin，" c ")
> 
> 运行(" \存储卡\程序文件\UCWEB\UCWEB.exe ")
> 
> WaitForActive( "UC 浏览器"，10)
> 
> send left soft(“UC 浏览器”)
> 
> send down(“UC 浏览器”)
> 
> send down(“UC 浏览器”)
> 
> SendCR(“UC 浏览器”)
> 
> send down(“UC 浏览器”)
> 
> SendCR(“UC 浏览器”)
> 
> SendLeftSoft(“下载”)
> 
> SendCR(“下载”)
> 
> SendCR("新任务" )
> 
> SendRightSoft("新任务" )
> 
> SendCtrlKey( "v ")
> 
> SendLeftSoft("新任务" )
> 
> 或者比如一个视频下载，但是你不想下载，只想看
> 
> *全屏编辑链接-开始菜单观看 coreplayer*
> 
> *代码:*
> 
> 鼠标点击(activeWin，100)
> 
> 鼠标点击(activeWin，100)
> 
> 睡眠(20)
> 
> SendCtrlKey( activeWin，" c ")
> 
> 运行(" \存储卡\程序文件\CorePlayer\player.exe ")
> 
> WaitForActive( "CorePlayer "，15)
> 
> SendLeftSoft( "CorePlayer ")
> 
> SendDown( "CorePlayer ")
> 
> SendCR( "CorePlayer ")
> 
> SendKeys( "http://)
> 
> SendCtrlKey( "v ")
> 
> 发报机*

 *更多信息可以在[原线程](http://forum.xda-developers.com/showpost.php?p=6679031&postcount=64)中找到。*