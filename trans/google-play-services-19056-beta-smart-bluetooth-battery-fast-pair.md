# Google Play 服务 19.0.56 测试版提示快速配对设备的智能蓝牙电池估计

> 原文：<https://www.xda-developers.com/google-play-services-19056-beta-smart-bluetooth-battery-fast-pair/>

# Google Play 服务 19.0.56 测试版提示快速配对设备的智能蓝牙电池估计

最新的 Google Play 服务测试版表明，谷歌正在努力为蓝牙快速配对设备提供更智能的电池估计。请继续阅读！

3.5 毫米耳机插孔[正在被淘汰](https://www.xda-developers.com/samsung-galaxy-note-10-specs-features-price-availability/)，我们将见证配件制造商对蓝牙音频设备的更多尝试。早在 2017 年，谷歌曾[宣布快速配对](https://www.xda-developers.com/fast-pair-quick-bluetooth-pairing-headphones/)作为一种实现与兼容设备快速蓝牙配对的方式，使这一过程更容易和方便当时即将推出的 [Pixel Buds](https://www.xda-developers.com/google-pixel-buds-google-assistant/) 用于[谷歌 Pixel 2](https://forum.xda-developers.com/pixel-2) 。在 Google I/O 2019 上，谷歌宣布，它正致力于为真正无线耳机的电池壳在手机上显示电池通知，从 Android Q 开始。现在，Google Play 服务的最新测试版表明，谷歌正在扩展这些电池通知，使其更智能地用于快速配对设备。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些功能目前还没有在 live build 中实现，可能会在未来的版本中随时被 Google 拉出来。

Google Play Services v19.0.56 包含一些字符串，表明您很快就可以看到您连接的蓝牙设备的估计电池寿命:

```
 <string name="fast_pair_headset_smart_battery_hr_min">%1$s • %2$d hr %3$d min left</string>
<string name="fast_pair_headset_smart_battery_min">%1$s • %2$d min left</string> 
```

目前，蓝牙无线耳机的电池寿命以百分比表示。上述字符串表明，谷歌现在将试图对电池寿命做出更智能的估计，将电池的百分比转化为预测的可用小时数和分钟数。

在 Android Q 中，谷歌正在改造蓝牙设置页面，作为所有通过蓝牙连接的设备的中央管理页面。Google 快速配对服务(GFPS)是适用于 Android 6.0 以上设备的 Google Play 服务的一部分，有助于通过 A2DP 或 HFP 配置文件连接的配件实现更轻松的连接和通信功能。谷歌维护着一个快速配对提供商模型的数据库，所以他们已经有了这些设备的实际物理电池容量的技术数据。谷歌在明智地估计电池寿命时，是否会考虑到由于经常使用而导致的正常电池退化，还有待观察。谷歌还宣布，他们正在与原始设备制造商合作，支持额外的蓝牙配置文件和 BLE 专用设备，因此我们应该期待在这方面看到更多的成果。

* * *

*感谢 PNF 软件为我们提供了使用许可 [JEB Decompiler](https://www.pnfsoftware.com/?aid=xdadev) ，这是一款针对 Android 应用的专业级逆向工程工具。*