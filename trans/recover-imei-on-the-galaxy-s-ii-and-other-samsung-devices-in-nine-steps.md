# 用九个步骤恢复 Galaxy S II 和其他三星设备上的 IMEI

> 原文：<https://www.xda-developers.com/recover-imei-on-the-galaxy-s-ii-and-other-samsung-devices-in-nine-steps/>

有时候不好的事情发生了，你甚至不知道。闪存模块会破坏你的 WiFi，内核会破坏你的相机，闪存一些只读存储器会扰乱你的 EFS 文件夹，从而影响你的 IMEI 在三星设备上，包括流行的 [Galaxy S II I9100](http://forum.xda-developers.com/forumdisplay.php?f=1055) 。

XDA 论坛成员 vaskodogamagmail 发布了一个方法，可以帮助用户恢复他们的 IMEI，如果非常重要的 EFS 文件夹被意外修改的话。简而言之，恢复备份的 IMEI 需要删除损坏的 EFS 文件夹，创建一个新的文件夹，并使用根支持的文件资源管理器做一些文件修改。用开发商的话说:

> 所以我研究了一下。搜遍了所有的论坛也没找到什么能治好我手机的 IMEI 设置成原来的 IMEI 号的。所以我做了实验，几个小时后，我修复了我的 IMEI。
> 
> 一件事使我得出这样的结论。nv_data”文件是我需要修复 IMEI 的东西，因为它们共享一个看起来非常相似的名称，并且它们具有相同的 2MB 大小。

虽然该指南是在考虑 Galaxy S II 的情况下编写的，但方法*应该*适用于所有带有 EFS 文件夹的三星设备。那些希望恢复他们的 IMEI 应该访问[原始线程](http://forum.xda-developers.com/showthread.php?t=1264021)的额外信息和完整的方法。在开始之前，请务必备份您的设备，包括 EFS 文件夹的内容。