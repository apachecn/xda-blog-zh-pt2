# [更新:在 Q Beta 3 中添加] Android Q 将为运营商提供更多 SIM 锁手机的方式

> 原文：<https://www.xda-developers.com/android-q-carriers-sim-lock-phones/>

**更新 1(美国东部时间 2019 年 5 月 8 日下午 5 点 55 分:**为 Android Q beta 3 版本上传的文档确认了最新版本中添加了对多 SIM 卡设备的运营商限制。

从[我们发布 Android Q 早期版本的独家](https://www.xda-developers.com/android-q-dark-theme-desktop-mode-permission-revamp/)到现在已经一周了。根据我们得到的版本，该操作系统的最新版本包括一些期待已久的功能，如全系统的适当黑暗模式，改进和更详细的权限控制，等等。但是，每个版本的 Android 都包含一个没人要求的功能。这一次，它比来自 Android Pie 的不想要的导航手势或来自 Android Oreo 的赤裸裸的白色界面要严重得多。显然，谷歌将让运营商使用更简单的方法来锁定设备。

Google 注意到 Android 开源项目 Gerrit 上有四个关于这些变化的提交。所有的提交都被称为“Android Q 的运营商限制增强”。 *9to5Google* 报道称，在查看消息来源后，他们可以证实 Android Q 将允许运营商加入黑名单和白名单。从即将发布的 Android 版本开始，运营商也将能够限制该设备的双卡功能。他们将能够完全锁定第二个 SIM 卡插槽，除非第一个插槽中有经过验证(由运营商添加到白名单中)的 SIM 卡。

我认为这是正式开始推荐解锁手机而不是运营商锁定手机的时候了。的确，他们有很好的计划，有时听起来好得令人难以置信，但我认为人们不应该为了省钱而牺牲引导程序、SIM 卡插槽、更新速度、网络可靠性、热点功能和许多其他功能。所有这些“限制增强”肯定会让开发者更难为某些设备提供定制的 rom、内核和其他类型的 mod。如你所知，解锁引导加载程序大多与 SIM 锁有关。

Android Q 仍处于早期开发阶段，因此这些功能可能不会出现在最终版本中。我们会留意的。

[**Via:9 to 5 Google**](https://9to5google.com/2019/01/21/android-q-carriers-sim-lock/)

[**来源:AOSP·格里特**](https://android-review.googlesource.com/q/topic:%22aosp_simlock_q_enhancements%22)

## 更新 1:在 Q Beta 3 中添加

在 [TelephonyManager](https://developer.android.com/reference/android/telephony/TelephonyManager.html#MULTISIM_ALLOWED) 类中添加的新字段，尤其是“MULTISIM _ NOT _ SUPPORTED _ BY _ CARRIER”，确认了 Android 支持 MULTISIM 设备上的运营商限制。对上述整数字段的描述表明:

> #### 硬件支持同时使用多个 SIM 卡在网络上注册(例如，双待机或双活动)，但运营商对此有所限制。

我们必须等待，看看这是否会增加运营商锁定多 SIM 卡设备的频率。在美国销售的大多数设备都只有一个 SIM 卡，因此这可能是运营商销售双 SIM 卡设备的一种方式，同时保留控制权。