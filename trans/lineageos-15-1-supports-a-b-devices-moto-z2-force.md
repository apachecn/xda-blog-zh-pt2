# LineageOS 15.1 现在支持 A/B 设备，如 Moto Z2 Force

> 原文：<https://www.xda-developers.com/lineageos-15-1-supports-a-b-devices-moto-z2-force/>

Android Nougat 7.0 带来的更令人兴奋的变化之一是为使用该 OS 版本推出的设备引入了 A/B 双分区方案。这一变化解决了 Android 系统更新如何应用于设备的问题，旨在为用户提供无缝升级体验，只需简单快速的重启即可将他们带入更新的操作系统。这一变化还增加了故障保护的好处，确保在 OTA 更新期间至少有一个可用的引导系统保留在设备上，允许设备在 OTA 引导失败时“回滚”到旧系统。

遗憾的是，并不是每台已经收到 Android 7.0 的设备都支持这种 A/B 双分区方案。这种 A/B 分区方案主要出现在最初装有 Android Nougat 7.0+的设备上，因为将设备更新到 Nougat 并支持这一更改将需要重新分区，这被许多原始设备制造商认为是一个有风险的提议。[以下是支持 A/B 无缝更新的设备列表](https://www.xda-developers.com/list-android-devices-seamless-updates/)。或者，你也可以[手动检查你的设备是否支持无缝更新](https://www.xda-developers.com/how-to-check-android-device-supports-seamless-updates/)。

虽然 A/B 双分区方案很受欢迎，但它确实对定制 ROM 社区构成了挑战。 [A/B 设备没有恢复分区](https://source.android.com/devices/tech/ota/ab/ab_implement),因为 Android 系统不需要这些分区，所以社区必须适应它的方式。 [TWRP v3.1.0 发布支持 A/B 设备](https://www.xda-developers.com/twrp-v3-1-0-is-now-rolling-out-with-support-for-adb-backup-ab-ota-zips-and-more/)，而 [Magisk 带来 14.1 版本支持 A/B 设备](https://www.xda-developers.com/magisk-14-1-official-google-pixel-support/)。

现在，LineageOS 15.1 增加了对 A/B 设备的支持。由于 LineageOS 团队正在修复他们的 addon.d 脚本，支持在 15.1 延迟。这个脚本负责备份 GApps 和 Lineage 的 SU 插件，它需要修改才能正确地与 A/B 设备一起工作。以下人员参与了这一发展的发生(如果我们错过了任何人道歉。)

### 为 LineageOS 15.1 提供 A/B 支持的贡献

*   XDA 认可开发人员 [invisiblek](https://forum.xda-developers.com/member.php?u=2385005) -编写了 addon.d-v2/backuptool_ab 并为 A/B 更新程序贡献了原始补丁
*   XDA 资深会员 [npjohnson](https://forum.xda-developers.com/member.php?u=5848265) -维护了 addon.d-v2/backuptool_ab 并实现了一些修复。与外部项目(OpenGApps/Magisk)合作，帮助他们与新工具兼容。
*   XDA 资深会员 [abhishek987](https://forum.xda-developers.com/member.php?u=6070905) -维护 addon.d-v2/backuptool_ab，一路上帮忙调试/修复，
*   [gmrt](https://github.com/gmrt) -设置 A/B 无缝更新器，在 updater 中增加了对各种 A/B 函数的支持，build.prop 曝光启动 releasetools for A/B，切换到 unrestrict update _ engine(WIP)
*   XDA 认识到开发者 tdm 带来了沿袭恢复，这个平台作为内置恢复在 A/B 上发布
*   XDA 认可的开发商 raymanfx 各种恢复补丁，允许安装旧风格的拉链和新的有效载荷风格的拉链，一些 AVB 工具工作，使 addonsu A/B 兼容
*   XDA 资深会员 [intervigil](http://forum.xda-developers.com/member.php?u=1815755) - Android 验证启动逻辑，以及禁用/处理它的工具
*   XDA 非活跃公认开发者 [Rashed97](https://forum.xda-developers.com/member.php?u=4662457) - addon.d 贡献和平台登录

最初，只有摩托罗拉 Moto Z2 Force (nash)被添加到名册中，预计未来将支持更多设备。**Moto Z2 Force 的[版本将于明天](https://download.lineageos.org/nash)推出。Z2 部队的建设由 XDA 资深成员 [npjohnson](https://forum.xda-developers.com/member.php?u=5848265) 负责维护。**

我们预计，一旦修复了所有特定于设备的错误，以下设备将很快获得支持:

事实上，鉴于此处的评论，我们预计小米 A1 将很快获得支持。同样，一个与蓝牙 MAC 相关的 [bug 需要在基本手机发布前修复。一旦其他 A/B 设备的官方 LineageOS 15.1 版本开始推出，我们将随时向您更新。](https://review.lineageos.org/#/c/LineageOS/hudson/+/218594/)