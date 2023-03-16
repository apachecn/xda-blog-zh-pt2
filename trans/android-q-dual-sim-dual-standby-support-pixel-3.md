# 在 Android Q 上的 Google Pixel 3 上启用双卡双待[Root]

> 原文：<https://www.xda-developers.com/android-q-dual-sim-dual-standby-support-pixel-3/>

**更新 3(美国东部时间 2019 年 7 月 18 日 7 点 53 分):**我们论坛上的用户发现了如何在运行最新 Android Q betas 的谷歌 Pixel 3 上重新启用 DSDS。但是，该方法需要 root 访问权限。说明可以在下面找到。

**更新 2(美国东部时间 2019 年 5 月 8 日上午 10:20):**Google give th 和 Google taketh。双 SIM，双待已经在 Android Q Beta 3 中移除。

**更新 1(美国东部时间 4/3/19 @下午 3:12):**这个功能在第一个 Android Q beta 中还没有功能，但我们有证据表明它确实在 [Android Q Beta 2 中工作](https://www.xda-developers.com/android-q-beta-2-notification-bubbles/)。

距离 Android Q 的第一个测试版发布仅仅几个小时，但用户已经发现了这次更新中一些非常重要的变化。其中大部分肉眼看不到，也没有包含在[发布的博文](https://www.xda-developers.com/android-q-new-features/)中。其中一个功能是对 Pixel 3 和 Pixel 3 XL 设备的双 SIM、双待机支持。

正如大多数人可能已经知道的那样，自 Pixel 2 和 Pixel 2 XL 以来，像素设备就支持 eSIM。尽管它有一个很大的缺陷:你不能同时使用物理 SIM 网络和 eSIM 网络。你必须禁用至少一个 Sim 卡，因为谷歌 Pixel 2 和 Pixel 3 只有双 Sim 卡，单待机(DSSS)支持。最初，[我们认为](https://www.xda-developers.com/google-pixel-4-dual-sim-rumor/)谷歌将只从 Pixel 4 开始提供双卡双待(DSDS)支持，但他们让我们惊讶得更早。正如*欧文·威廉姆斯*所注意到的，新发布的 Android Q beta 已经在 Pixel 3 上启用了 DSDS 支持。

到目前为止，更好的双 SIM 卡功能是 Pixel 3 用户要求最多的功能之一。在 DSDS 的支持下，谷歌的最新设备在连接性方面终于与最新的 iPhones 不相上下了。双 SIM 卡，双待机意味着您可以提供/注册两个 SIM 卡，但只有一个可以在使用中。在看到 Android Q 中的 DSDS 功能(以及谷歌在 Pixel 3 上启用它)后，如果谷歌 Pixel 4 设备不支持它，我们会感到震惊。我们也可以期待双 SIM 卡，双活动(DSDA)，允许两个 SIM 卡同时使用，甚至是数据。不过，这需要第二台收音机。

## 更新 1:在 Android Q Beta 2 中工作

根据欧文·威廉姆斯在 Twitter 上的说法，Pixel 3 现在可以在 Android Q Beta 2 上同时使用 eSIM 和物理 SIM。

* * *

## 更新 2:在 Beta 3 中消失

[Reddit](https://www.reddit.com/r/GooglePixel/comments/blvfug/any_comments_on_beta_3_and_the_dual_sim/)上的用户报告称，他们无法再通过功能标志或*#*#4636#*#*菜单访问上面更新中显示的切换。事实上，Beta 3 中没有特性标志。如果您在更新到 Beta 3 之前启用它，它看起来确实可以工作。但是，您将无法将其关闭。

[**Via:安卓警察**](https://www.androidpolice.com/2019/05/08/android-q-brings-half-baked-dual-sim-support-to-the-pixel-3/#3)

* * *

## 更新 3:启用 Root 访问权限

XDA 少年成员 JujuYuki [发现](https://forum.xda-developers.com/showpost.php?p=79877277&postcount=211)如果你有 root 权限并在提升的 shell 中输入以下命令，你可以在运行 Android Q beta 3、4 或 5 的 Pixel 3/Pixel 3 XL 上启用 DSDS:

```
 setprop persist.vendor.radio.multisim_switch_support true 
```

重启后，在拨号器中输入*#*#4636#*#*，进入“电话信息”菜单，点击“启用 DSDS”(感谢 Redditor/u/[zh lancer](https://www.reddit.com/user/zhtlancer)指出这部分！)

为了让 Android Q beta 5 在 Pixel 3 上扎根，你需要[安装最新的 Magisk Manager Canary](https://www.xda-developers.com/magisk-google-pixel-3-pixel-3a-android-q/) ，切换到 Canary channel 的应用程序，从工厂映像修补股票启动映像，然后使用 fastboot 刷新这个修补的启动映像。