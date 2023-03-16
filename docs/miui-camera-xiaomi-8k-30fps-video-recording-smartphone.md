# MIUI 摄像头显示小米正在进行 8K 视频录制

> 原文：<https://www.xda-developers.com/miui-camera-xiaomi-8k-30fps-video-recording-smartphone/>

本周，小米再次向我们展示了他们制造不同价格的一流手机的能力。在预算部分，该公司推出了 red mi 8A T1，配有 6.2 英寸高清显示屏、5000 毫安时电池、骁龙 439、18W 充电支持和 12MP 索尼 IMX 363 Rs。6499 (~$92.)在廉价旗舰细分市场，他们宣布了具有 5G 连接、30W 无线充电、10W 反向无线充电的 [Mi 9 Pro](https://www.xda-developers.com/mi-9-pro-5g-miui-11-snapdragon-mi-tv-pro-8k-video/) ，以及售价约 520 美元的骁龙 855 Plus。最后，他们对大约 2800 美元的 [Mi MIX Alpha](https://www.xda-developers.com/xiaomi-mi-mix-alpha-surround-display-china-launch/) 及其 180%的屏幕与机身比例完全着迷，以证明他们可以创新。不过，小米似乎还有更多锦囊妙计，因为我们在 MIUI 相机应用程序中发现了证据，表明未来的智能手机将支持以 30fps 的速度录制 8K 分辨率的视频。

除了小米 9 Pro 5G 和小米 MIX Alpha 发布之外，小米还发布了其基于 Android 的软件 MIUI 的新版本。MIUI 11 更新的主要亮点是新的设计，当然，还有一个更新的相机应用程序。自从 MIUI 11 测试版[开始在中国](https://www.xda-developers.com/download-miui-11-beta-now-for-13-xiaomi-devices-changelog/)推出以来，我们花时间分析了最新的 MIUI 相机 APK，以发现新功能。XDA 初级成员 kackskrz 向我们透露了关于以 30fps 捕捉 UHD/8K 视频的字符串的内容。

```
 <string name="pref_video_quality_entry_8kuhd">UHD 8K, 30fps</string>
<string name="video_ultra_clear_tip_8k">8K UHD</string> 
```

查看代码，我们在与配置视频质量相关的类中发现了证据，表明这个新配置文件的输出分辨率确实是 7680x4320，即 8K。我们还发现了一个新的 8K@30fps 录制模式的可绘制资源。本文顶部展示的特色图片中 Mi logo 旁边的 8K@30fps logo，其实是直接从最新的 MIUI 相机 app 中拉出来的。因此，我们可以得出结论，小米正在努力在未来添加这种视频录制配置文件。

## 8K@30fps 视频录制的未来小米手机

那么，下一个问题是，这个功能最终会出现在什么样的小米手机上？我排除了这是新款 Mi MIX Alpha 上的一种相机模式的想法，因为它没有在任何在线报道中提及，也没有在[官方产品页面](https://www.mi.com/mixalpha/specs)上列出，而且它[超过了三星提供的技术规格](https://www.xda-developers.com/samsung-isocell-bright-hmx-108mp-camera-sensor-xiaomi/)。(三星的 108MP 明亮 HMX 相机传感器能够以 30fps 的速度录制高达 6K 分辨率的视频。)没有其他小米手机支持以这种质量录制视频，因此它肯定会在新设备上首次亮相。有趣的是，[新小米电视 Pro](https://www.xda-developers.com/mi-9-pro-5g-miui-11-snapdragon-mi-tv-pro-8k-video/) 能够播放 8K 视频，因此小米可能会将其 8K 视频录制的新智能手机定位为其新 4K 小米电视的补充。

不过，我不认为这种新的相机模式会在任何装有高通骁龙 855 的新智能手机上首次亮相，因为 Spectra 380 ISP 的[技术规格](https://www.xda-developers.com/qualcomm-snapdragon-855-kryo-485-cpu-adreno-640-gpu-spectra-isp-cv/)将 4K@60fps 列为支持的最高视频录制质量。虽然可以推动 Spectra 380 处理 8K@15fps，如[红色魔法 3](https://www.xda-developers.com/nubia-red-magic-3-review/) 所示，但它很难处理它。在[华硕 ZenFone 6](https://forum.xda-developers.com/zenfone-6-2019) 和[华硕 ROG Phone II](https://forum.xda-developers.com/rog-phone-2) 上，可以 8K@24fps 录制视频(！)在 [FreeDCam](https://play.google.com/store/apps/details?id=troop.com.freedcam) 中使用自定义配置文件(感谢那个提示，XDA 资深会员 [defcomg](https://forum.xda-developers.com/member.php?u=377973) ！)，但是这种体验并不愉快，因为不支持 e is。

我怀疑下一款高通骁龙旗舰 SoC 中的升级版 Spectra ISP 将能够处理 8K@30fps，如果属实，这意味着这种新的相机配置文件将首次出现在小米旗舰上，采用下一款旗舰骁龙芯片。然而，我们没有任何确认的细节可以分享下一款旗舰高通骁龙 SoC，所以我们不能肯定哪个 SoC 将为小米智能手机提供这一功能。一旦我们有了更具体的细节，我们会让你知道。

* * *

*感谢 PNF 软件为我们提供了使用许可 [JEB Decompiler](https://www.pnfsoftware.com/?aid=xdadev) ，这是一款针对 Android 应用的专业级逆向工程工具。*