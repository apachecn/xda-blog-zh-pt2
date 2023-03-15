# 使用 XPrivacy 管理单个应用权限

> 原文：<https://www.xda-developers.com/manage-individual-app-permissions-with-xprivacy/>

不可否认的是，隐私对于所有操作系统的大量移动用户来说都是一个巨大的问题。除非砸碎你的无线路由器，换成 3310，把 T2 放在一个有铅线的盒子里，直到你需要打电话，否则很难跟踪你的个人信息在哪里、什么时候、向谁泄露了。

Android 应用程序需要各种权限，这一点你现在肯定已经很熟悉了。大多数人出于正当的理由需要这些。但是，有些人可能会利用特定的权限，做一些您可能没有意识到或没有预料到的事情。除了只安装您绝对需要和信任的应用程序之外，尝试并消除权限被滥用的可能性的最佳方式是使用 OpenPDroid 之类的工具来调整每个应用程序的权限。这种修改的唯一缺点是对于普通用户来说很难实现。XDA 的高级成员 [M66B](http://forum.xda-developers.com/member.php?u=2799345) 在 [Xposed 框架](http://www.xda-developers.com/android/say-goodbye-to-custom-stock-roms-and-hello-to-xposed-framework/)的一点帮助下，朝着使权限管理更加容易的方向迈出了一步。

XPrivacy 是一个公开的模块，允许用户查看他们设备上当前安装的所有应用程序，然后调整应用程序可以使用的个人权限。不是简单地阻止应用程序收集它正在寻找的数据，这可能导致强制关闭， XPrivacy 将提供虚假数据，如空的联系人列表或欺骗的位置。从 [M66B 的 Github](https://github.com/M66B/XPrivacy) 中可以获得可能的限制和任何其他你可能想要的信息的完整列表。该模块也是开源的，这很好。

如果你担心隐私，看看[原始帖子](http://forum.xda-developers.com/showthread.php?t=2320783)了解更多信息。