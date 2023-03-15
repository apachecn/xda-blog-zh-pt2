# APKTool v0.9.2 -重新设计 apk 文件

> 原文：<https://www.xda-developers.com/apktool-v0-9-2-re-engineer-apk-files/>

APKTool v0.9.2 是由 XDA 成员 [Brut.all](http://forum.xda-developers.com/member.php?u=1922851) 开发的工具，用于重新设计第三方 Android 应用。

它可以用于本地化，或为自定义平台添加功能-它不是为了盗版和其他非法用途。

> 最初由 **Brut.all** 发布
> 
> *   帮助完成一些重复性的任务
> *   将资源解码为近乎原始的形式
> *   资源重新打包后更新应用程序代码中包含的资源 id
> *   支持许多应用程序
> *   内置 Smali、baksmali 和 Android 资源

目前 APKTool 只在 Linux 上运行，但是 Brut.all 已经开始在 Windows 版本上工作。此外，framework-res.apk 无法解密，因为它(和其他系统文件)似乎是使用 Google 的一些私有工具构建的——但希望在未来的开发中会得到解决，例如一个定制的类似 appt 的工具。

为了使用 APKTool，需要 SDK、aapt、PATH 和 smali 的基本知识。

欲了解更多信息并下载该工具，请访问主[应用线程](http://forum.xda-developers.com/showthread.php?t=640592)，或查看他在 [youtube](http://www.youtube.com/watch?v=P_Zyf7jFbx4) 上的视频。