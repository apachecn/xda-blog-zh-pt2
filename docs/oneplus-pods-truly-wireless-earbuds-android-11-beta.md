# 一加豆荚真正的无线耳塞出现在 Android 11 测试版中

> 原文：<https://www.xda-developers.com/oneplus-pods-truly-wireless-earbuds-android-11-beta/>

一加可能因其智能手机而闻名，但该品牌也生产一些优秀的音频配件。[子弹无线](https://www.xda-developers.com/oneplus-bullets-wireless-review/)和[子弹无线 2](https://www.xda-developers.com/oneplus-7-pro-accessories-review-cases-bullets-wireless-2-warp-charge-30-car-charger/) 是我们在 2018 年和 2019 年推出的一些最受欢迎的蓝牙无线耳机，这要归功于它们持久的电池寿命、快速充电支持和整体的性价比。今年，一加宣布了更加实惠的[子弹无线 Z 耳机](https://www.xda-developers.com/oneplus-bullets-wireless-z-announced-ip55/)，但我们真正期待的是他们即将推出的真正的无线耳塞，可以被称为一加豆荚。

自五月中旬以来，著名的推特泄密者 [Max J.](https://twitter.com/MaxJmb) 一直暗示将从一加推出 [TWS 耳塞。如上图所示，他最新泄露的消息透露了新耳塞的可能设计。他建议新的音频配件可能在 7 月份推出，这可能与一加 8T](https://www.xda-developers.com/oneplus-truly-wireless-earbuds/) 在[的推出相吻合。在深入研究为一加 8 系列](https://www.xda-developers.com/community-designed-oneplus-jacket-launch-alongside-the-oneplus-8t/)新发布的 [Android 11 测试版时，经常访问 XDA 门户网站的消息人士和资深会员](https://www.xda-developers.com/oneplus-8-oneplus-8-pro-android-11-beta-download/) [Some_Random_Username](https://forum.xda-developers.com/member.php?u=8234677) 发现了来自一加的新 TWS 耳塞存在的证据。

在 Android 11 测试版的新设置 APK 中，Some_Random_Username 发现了以下字符串:

```
 <string name="oneplus_tws_pods_funtion">Headset function</string> 
```

字符串标题中的“oneplus_tws_pods”激起了我们的兴趣，因此我们对固件进行了更深入的研究。与一加·TWS 耳塞相关的唯一其他参考资料包含在设置应用程序的反编译代码中。我们在包括 BluetoothDashboardFragment、BluetoothDeviceDetailsFragment、OnePlusPodDevice 和 OnePlusUpdate 的类中发现了对“一加豆荚”和名为“com.oneplus.twspods”的配套应用程序包的多个引用。

在 BluetoothDashboardFragment 类中，有读取左右耳塞各自电池电量的代码，这是真正的无线耳塞才需要的，因为每个耳塞都有自己的电池。在某些部分，提到了“oppoPodsService”，这可能暗示了一加 Pods 和 OPPO 现有的真正无线耳塞之一之间的关系——也许是 [OPPO Enco W31](https://www.xda-developers.com/oppo-find-x2-pro-neo-and-lite-available-germany-free-bluetooth-audio-accessories/) 或 [OPPO Enco Free](https://www.xda-developers.com/realme-buds-air-india-launch-oppo-enco-free-announced-apac-region-truly-wireless-earphones/) ？BluetoothDeviceDetailsFragment 类引用双击动作来播放/暂停音乐或跳到下一首/上一首歌曲，OTA 更新，以及“查找我的蓝牙耳机”设置，这可能与谷歌新的[快速配对设备的“查找我的配件”功能](https://www.xda-developers.com/fast-pair-location-tracking-battery-notifications-new-settings/)有关。

我刚刚提到的都是任何像样的真正无线耳塞的预期功能，但一加可能会有更多惊喜。也许一加豆荚将支持某种快速充电？还有设计、定价、可用性的问题，最重要的是音频质量。我们对这些 TWS 耳塞了解不多，但我们现在非常确定它们确实存在。

* * *

*感谢 PNF 软件为我们提供了使用许可 [JEB Decompiler](https://www.pnfsoftware.com/?aid=xdadev) ，这是一款针对 Android 应用的专业级逆向工程工具。*