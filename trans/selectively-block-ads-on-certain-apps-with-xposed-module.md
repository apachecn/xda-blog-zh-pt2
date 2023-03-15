# 通过 Xposed 模块有选择地阻止某些应用程序上的广告

> 原文：<https://www.xda-developers.com/selectively-block-ads-on-certain-apps-with-xposed-module/>

没有人喜欢侵扰性广告，尤其是当它们以闪烁霓虹灯的形式试图让我们购买我们不想要的东西时。但它们是非常必要的，因为大多数独立开发者利用广告赚取少量的钱来满足他们的基本需求。不久前，我们谈论了一个由 XDA 资深会员 [DragonHunt3r](http://forum.xda-developers.com/member.php?u=4772048) 创建的[广告拦截 Xposed 模块](http://www.xda-developers.com/android/get-rid-of-ads-with-xposed-module/)，它允许用户拦截广告。

通常广告拦截器会在原始广告的位置留下一个空格。XDA 论坛成员 [FatMinMin](http://forum.xda-developers.com/member.php?u=4981793) 创建了一个 Xposed 模块，能够完全删除应用程序中的广告，以及它们留下的空白空间。然而，这还不是最好的部分。相反，您可以将某些应用程序添加到白名单或黑名单中，以便只排除或包括您选择的应用程序。通过这样做，你可以让独立开发者为他们的辛勤工作赚钱，同时阻止来自大型出版商的侵入性广告。因为它是一个 Xposed 模块，所以您的设备必须是根设备并且安装了 Xposed Framework。

这个模块是去除广告的好机会，同时保留独立应用上的广告。但是，如果你打算禁用你最喜欢的应用程序中的广告，可以考虑捐赠以示感谢，或者将某些应用程序保留在白名单中。该模块可以在[原始线程](http://forum.xda-developers.com/showthread.php?t=2597332)中找到。