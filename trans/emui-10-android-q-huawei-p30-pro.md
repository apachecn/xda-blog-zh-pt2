# 基于 Android 的 EMUI 10 问:先看华为 P30 Pro

> 原文：<https://www.xda-developers.com/emui-10-android-q-huawei-p30-pro/>

自从特朗普政府将华为加入实体名单以来，这家智能手机巨头是否能继续提供主要的 Android 平台更新一直不确定。如果美国和中国未能达成协议，谷歌将被迫撤销[华为的安卓许可](https://www.xda-developers.com/google-revoke-huawei-android-ban-blacklist/)，这将使华为无法向搭载谷歌移动服务(包括 Google Play 服务和谷歌 Play 商店)的用户提供任何更新。大多数用户认为华为没有可能升级基于 Android Q 的 EMUI 10 设备，但由于谷歌[已经向华为](https://www.xda-developers.com/android-q-beta-3-released/)提供了预发布源代码，该公司很有可能已经在下一次重大更新中取得了重大进展。现在我们有证据证明这确实是事实:这是你在华为 P30 Pro 上第一次看到 EMUI 10。

这第一眼是由 [FunkyHuawei.club](https://funkyhuawei.club/) 提供的，这项服务可以让你付费更新、更名或[引导程序解锁](https://www.xda-developers.com/huawei-honor-unlock-bootloader-fee/)你的华为或 Honor 设备。他[在我们的论坛](https://forum.xda-developers.com/showpost.php?p=79724894&postcount=258)上分享了一种方法，可以让你在华为 P30 Pro 上安装预发布的 EMUI 10 版本，供那些喜欢冒险的人使用。XDA 自己的 Max Weinbach 将它加载到他的 P30 Pro 上，以确认它是真的。

[**华为 P30 Pro 论坛**](https://forum.xda-developers.com/huawei-p30-pro)

一开始，用户界面似乎没有太多变化，至少视觉上没有。启动器、通知、状态栏、快速设置、设置似乎和基于 Android 9 Pie 的 EMUI 9.1 没什么变化。然而，Android Q 的[新权限控制](https://www.xda-developers.com/android-q-security-privacy-features/)，尤其是新的位置访问仅在使用中功能，在 EMUI 10 中存在。相机应用程序的用户界面也进行了细微的调整。

我们应该注意到，我们认为这个版本将被称为 EMUI 10，这是基于预发布固件包本身的名称，而不是上面显示的任何截图中的名称。不过，使用 [DevCheck 应用](https://www.xda-developers.com/devcheck-hardware-system-information-app/)，我们可以显示这款手机确实运行在 Android 平台版本“10”(Android q .)上

另一位消息人士@ [wildlime](https://twitter.com/wildlime/) 向 FunkyHuawei 分享了他们对华为 P30 Pro 的第一印象。总而言之:

*   在此过程中，他的电话区域更改为 C675E1(原来是 432)
*   没有通过 CTS
*   他拥有 8GB RAM 的国际双卡华为 P30 Pro，这是系统识别的
*   荷兰语被激活，并按预期工作
*   打电话，照相，OK 谷歌工作正常
*   HiSuite 再也认不出这个电话了
*   有一个新的标志(如上图所示)
*   相机应用程序中相机模式的新布局
*   总体性能似乎有所提高
*   关于手机的页面显示手机运行 EMUI 9.1 和 Android 9 Pie，但伪造构建字符串是华为为防止泄露而经常做的事情。
*   除此之外，到目前为止，一切正常，没有大的问题。

我们将继续比较这个泄露的 EMUI 10 版本和我们从[两部分](https://www.xda-developers.com/emui-9-review-design-behavior-huawei-honor-android-pie/) [评论](https://www.xda-developers.com/emui-9-review-features-apps-huawei-honor-android-pie/)中了解的关于 EMUI 9 的一切。肯定会有大量的变化尚未被发现，所以我们将深入固件，看看是否有任何功能仍在开发中。我们还将关注华为可能放弃的其他版本，因为该公司已经[宣布](https://www.xda-developers.com/huawei-p30-mate-20-pro-honor-view20-magic-2-android-q-emui/)华为 Mate 20、华为 Mate 20 Pro、华为 Mate 20 X、华为 Mate 20 RS、华为 P30、Honor View20 和 Honor Magic 2 将是首批获得更新的华为和 Honor 设备。

* * *

## 更新 1:动手视频

来自 XDA 电视台的 Max 在华为 P30 Pro 上录制了 EMUI 10 测试版的动手视频。如果你有兴趣听听他用了一天后的想法，看看下面的视频。

**注意:华为已经停止为其设备提供官方 bootloader 解锁代码。因此，他们设备的引导加载程序无法解锁，这意味着用户无法 root 或安装自定义 rom。**