# Android 11 电池份额暗示为 Pixel 5 反向无线充电

> 原文：<https://www.xda-developers.com/android-11-battery-share-reverse-wireless-charging-pixel-5/>

今天，谷歌[发布了](https://www.xda-developers.com/android-11-developer-preview-1-google-pixel/)第一个针对 Pixel 设备的 Android 11 开发者预览版(不包括第一代机型)，我们正在[详细介绍我们迄今为止发现的一切](https://www.xda-developers.com/tag/android-11/)。在深入研究 Pixel 4 的 Android 11 系统转储时，我注意到了 Pixel 智能手机设置应用 SettingsGoogle 中的一个新活动，名为“电池共享”。出于好奇，我发起了这项活动，并发现了一个即将推出的功能。这个标志显然是一个占位符——它与自适应电池页面上的标志相同——但新的字符串表明，谷歌正在开发反向无线充电功能，可能用于 Pixel 5。

由于活动名称以“com.google.android”开头，而不是“com.android”，这个“电池共享”活动很可能是谷歌的一个功能，而不是 AOSP 的一个功能。这种模式也适用于其他谷歌功能，如 Active Edge 和 Pixel Stand 无线充电，因此我们认为我们正在寻找谷歌反向无线充电功能的开端，而不是通用的 AOSP 实现。电池共享页面的字符串表示“使用电池共享时，您手机的电池会更快耗尽。电池共享可与兼容的耳塞、手表、手机等设备配合使用。”虽然这并没有明确提到无线充电或反向无线充电，但其含义很明显:你正在分享你的手机电池，这意味着它会更快地耗尽，与某些兼容的耳塞，手表和手机。我们可以假设这是指使用您的设备为其他 Qi 兼容配件和智能手机充电。

谷歌的 Pixel 3、Pixel 3 XL、Pixel 4、Pixel 4 XL 支持 Qi 无线充电。Pixel 3 和 Pixel 3 XL 支持使用专有的 Pixel Stand 充电器进行 10W 无线充电，尽管它们也支持在其他无线充电器上进行 5W Qi 无线充电。Pixel 4 和 Pixel 4 XL 也支持 Pixel 支架上的 10W 无线充电，但[谷歌将兼容 Qi 无线充电器的无线充电速率](https://www.xda-developers.com/google-pixel-4-what-you-missed/)提高到 11W。目前没有 Pixel 手机支持反向无线充电；无论哪种设备最终拥有这一功能，很可能是 Pixel 5，都将是谷歌 Pixel 系列中第一个支持这一功能的设备。这项功能将与新的[真正的无线像素芽](https://www.xda-developers.com/new-google-pixel-buds-truly-wireless-earbuds/)很好地配对。

我们将继续挖掘 Android 11 开发者预览版，看看我们是否能找到更多关于该功能、即将发布的 Android OS 稳定版或 Pixel 5 的信息。

## 更新:找到无线充电和像素“Redfin”的链接

在检查新的 BatteryShare 特性的 Java 代码时，我发现 BatteryShareSwitchPreferenceController 中有一个名为“setChecked”的方法，它会显示一条提示消息，说明“无线充电时不能共享电池！”如果设备当前正在无线充电。BatteryShareFakeManager 中一个名为 isSupportedBatteryShare 的方法抓取了一个名为“config_device_model_name”的字符串数组，该数组目前只保存“redfin”作为其值。如果你还记得的话，Redfin 是我们一直在追踪的新像素代号之一。它是高通骁龙 765 的中端设备。虽然我们仍然不知道这款设备在谷歌设备系列中的确切位置，但我们现在知道它将支持反向无线充电。Pixel 5 会有中端处理器吗？