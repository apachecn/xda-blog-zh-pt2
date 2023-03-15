# OxygenOS 11 beta 暗示 8K 960fps 视频录制，一加芽 Z 的存在

> 原文：<https://www.xda-developers.com/oxygenos-11-beta-hints-8k-960fps-video-recording-oneplus-buds-z/>

谷歌刚刚[宣布了官方 Android 11](https://www.xda-developers.com/android-11-stable-google-pixel-oneplus-xiaomi-realme-oppo/) ，在稳定分支上推出支持谷歌 Pixel 的设备。除了这些稳定的版本，[其他 OEM 厂商也加入了 Android 11 派对](https://www.xda-developers.com/android-11-update-tracker/)，发布了新的测试版。一加已经来到现场，为一加 8 和一加 8 Pro 推出了 Android 11 和 OxygenOS 11 的开放测试版。当用户挖掘新的操作系统更新并体验谷歌和一加添加的新东西时，我们发现了即将到来的功能的暗示，如 8K 960fps 视频录制，以及一加 Buds Z 的存在

拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在此提到的任何功能都有可能不会出现在未来的版本中。这是因为这些特性目前还没有在实时构建中实现，并且可能会被开发人员在未来的构建中随时引入。

### OxygenOS 11 中的 8K 960fps 视频录制

适用于一加 8 和一加 8 Pro 的 OxygenOS 11 Open Beta 1 在一加相机应用程序中包括了这些新字符串:

```
 <string name="action_item_video_1080p_960fps">1080P 960FPS</string>
<string name="action_item_video_4k_120fps">4K 120FPS</string>
<string name="action_item_video_4k_240fps">4K 240FPS</string>
<string name="action_item_video_4k_480fps">4K 480FPS</string>
<string name="action_item_video_4k_960fps">4K 960FPS</string>
<string name="action_item_video_8k">8K 30FPS</string>
<string name="action_item_video_8k_120fps">8K 120FPS</string>
<string name="action_item_video_8k_240fps">8K 240FPS</string>
<string name="action_item_video_8k_480fps">8K 480FPS</string>
<string name="action_item_video_8k_60fps">8K 60FPS</string>
<string name="action_item_video_8k_960fps">8K 960FPS</string> 
```

这些字符串表明，一加正在努力为其智能手机引入 8K 960fps 视频录制支持，很可能是在高端旗舰产品上。然而，我们并不确定该公司如何在目前可用的硬件上实现 8K 960fps。高通骁龙 865 上的 Spectra 480 ISP 支持捕获 720p @ 960fpos，持续时间不受限制，不会过热。但是 ISP 本身不能处理 8K、4K 甚至 1080p 的 960fps 所需的那么多帧。ISP 可以处理 8K 30fps，正如我们在今年的几艘骁龙 865 旗舰上看到的那样，但超出这个范围将是第一次。

如前所述，我们不确定一加会如何执行。这些字符串可能是为高通下一代 SoC 的未来设备做准备。或者，一加可以求助于使用一些疯狂的放大和插值来达到这种效果。

### 一加芽 Z

XDA 资深会员*[Some _ Random _ Username](https://forum.xda-developers.com/member.php?u=8234677)*发现在*/vendor/etc/Dolby/DAX-default . XML*中提到了尚未发行的一加 Buds Z:

```
 <tuning name="oneplus_bluetooth_BudsZ" endpoint_type="headphone" mono_device="false" tuned_rate="48000" orientation="2" output_channels="2"> 
```

需要明确的是，已经有一个单独的 *oneplus_bluetooth_Buds* 调谐配置文件，所以这些 Buds Z 与已经发布的[一加 Buds](https://www.xda-developers.com/oneplus-buds-gray-color-us/)并不相同。一加的蓝牙音响配件阵容目前包括[一加子弹无线](https://www.xda-developers.com/oneplus-bullets-wireless-review/)、[一加子弹无线 2](https://www.xda-developers.com/oneplus-bullets-wireless-2-impressions/) 、[一加子弹无线 Z](https://www.xda-developers.com/oneplus-bullets-wireless-z-earphones-review/) 和[一加 Buds](https://www.xda-developers.com/oneplus-buds-review/) 。因此，一加 Buds Z 可能是下一个到来的蓝牙 TWS，如果该公司遵循其定价传统，可能比一加 Buds 的价格更低。

更清楚的是，这种单一的提及并不是 Buds Z 肯定存在的确凿证据，但它是一个*可能在未来*发布的设备。我们没有任何关于 Buds Z 的进一步信息。如果允许我们猜测，该公司可能会将它与一加 8T 一起推出。

### 一加 8T - " *肉串*"呈现

一加设置应用程序发现了一些细微的变化。早前发现的一加 8T 渲染图(标题为“*oneplus _ 8T . webp*”)[不见了](https://www.xda-developers.com/oneplus-8t-design-leak/)。相反，我们有一个名为“ *oneplus_kebab.webp* 的新文件，尽管其中的渲染与一加 8 相同。

设置应用程序也有字符串暗示有两种一加 8T - *烤肉串*和*烤肉串*，其中*烤肉串*将到达加拿大和印度，而*烤肉串*将到达美国。