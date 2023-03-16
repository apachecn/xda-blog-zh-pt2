# 如何在装有 MIUI 10 的小米设备上启用私有 DNS

> 原文：<https://www.xda-developers.com/enable-private-dns-xiaomi-devices-miui-10/>

# 如何在基于 Android Pie 的 MIUI 10 的小米设备上启用私有 DNS

小米已经在 MIUI 10 中移除了私有 DNS 功能。谢天谢地，多亏了 XDA 资深会员斯通迪德，我们可以避开这个功能的移除。

小米做了很多工作来反向移植 Android 的一些最新功能，但他们修改了他们的 OEM ROM，这样也删除了一些功能。一个很大的例子就是 MIUI 设备上安全模式的移除。传统的 Android 智能手机和平板电脑可以长按关机选项来获得安全模式提示，但这在 MIUI 设备上是不可能的。我们还可以在这里列举其他例子，但谢天谢地，有些例子是可以绕过的。

随着 Android Pie 的推出，谷歌增加了一个功能，允许用户在他们的设备上配置私有 DNS(或 HTTPS DNS)。 [Cloudflare 的 1.1.1.1 私有 DNS 服务器](https://www.xda-developers.com/cloudflares-android-app-fast-dns/)由于其私密性和速度已经变得相当受欢迎，但小米在 MIUI 10 中移除了该功能(基于 Android Pie)。谢天谢地，我们可以绕过这个功能的移除，XDA 资深成员 [stonedead](https://forum.xda-developers.com/member.php?u=4581814) 向我们展示了如何在 MIUI 10 中将其恢复。

1.  [下载并打开 QuickShortcutMaker](https://play.google.com/store/apps/details?id=com.sika524.android.quickshortcut)
2.  滚动到设置区域并点击 com . Android . Settings . Settings＄NetworkDashboardActivity
3.  点击该条目，它应该带你到网络和互联网设置，你现在可以设置私人 DNS

[**在我们的 POCO F1 论坛上通过 XDA 会员 stonedead 引导**](https://forum.xda-developers.com/poco-f1/how-to/enable-private-dns-miui-10-android-pie-t3899374)