# 改变你的。使用模块加载器动态 ko 文件

> 原文：<https://www.xda-developers.com/change-your-ko-files-on-the-fly-with-module-loader/>

你喜欢在你的安卓智能手机上摆弄不同的内核模块吗？作为 XDA 的读者，你可能会把一个空的 */system/lib/modules* 目录等同于谋杀。这是有充分理由的，因为模块通过添加对 Samba (cifs.ko)、Fuse (fuse.ko)、TUN/TAP 设备(tun.ko)等的支持，实际上赋予了您的设备生命。

然而，当一个人希望简单地*尝试*一个新模块时会发生什么呢？为了减轻手动文件管理的需要，XDA 论坛成员 [D4rKn3sSyS](http://forum.xda-developers.com/member.php?u=3484876) 创建了模块加载器。该应用程序允许用户快速轻松地选择要启用的模块。用开发商的话说:

> 这个应用是为那些厌倦了手动加载的人设计的。ko 在他们的手机上，或者甚至厌倦了在他们的系统文件夹上有一些额外的重量。
> 
> 基本上，这个应用程序可以读取系统、sd 卡或任何文件夹中的模块，并加载。也有一个启动时加载的选项。
> 
> *这个应用是在 Xperia X10 mini pro 上开发的，我需要所有设备的反馈。*

继续进入[应用线程](http://forum.xda-developers.com/showthread.php?t=1228605)开始模块交换。