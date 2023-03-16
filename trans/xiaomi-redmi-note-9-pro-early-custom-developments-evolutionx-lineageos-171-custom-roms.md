# 红米 Note 9 Pro 定制开发:LineageOS、TWRP 等

> 原文：<https://www.xda-developers.com/xiaomi-redmi-note-9-pro-early-custom-developments-evolutionx-lineageos-171-custom-roms/>

红米 Note 9 Pro ( [评测](https://www.xda-developers.com/xiaomi-redmi-note-9-pro-review-snapdragon-720g-48mp/))或红米 Note 9S [在一些国家被称为](https://www.xda-developers.com/xiaomi-redmi-note-9-pro-global-note-9s/)，采用了独特的方形后置摄像头排列，同时提供了一些可靠的规格，如[高通骁龙 720G](https://www.xda-developers.com/qualcomm-snapdragon-720g-662-460-navic/) SoC，5，020 mAh 大容量电池，支持 18W 快速充电，以及高达 128GB 的 UFS 2.1 存储。这款手机运行 Android 10，MIUI 11 开箱即用，小米迄今为止已经发布了相当多的[漏洞修复更新](https://www.xda-developers.com/xiaomi-redmi-note-9-pro-v11-0-5-0-update-fixes-widevine-l1-hdr-related-bugs/)以提高可用性。该公司还[发布了相应的内核源代码](https://www.xda-developers.com/xiaomi-redmi-note-9-pro-max-8-android-10-build-kernel-source-release/)以促进第三方开发，因此这里是我们对红米 Note 9 Pro 的第一次定制开发综述。

**[红米 Note 9 Pro XDA 论坛](https://forum.xda-developers.com/redmi-note-9-pro) ||| [在亚马逊印度](https://www.amazon.in/dp/B077PWBC78/?tag=xdaportalin-21)购买红米 Note 9 Pro **

* * *

## 红米 Note 9 Pro 的定制 rom

### 进化 X

如果你是一个普通的 Android 爱好者，并且正在寻找一个 Pixel 风格的 ROM，同时提供一些有用的 UI/UX 定制，那么你绝对应该看看 XDA 高级成员 [QuantumShqipe](https://forum.xda-developers.com/member.php?u=8692360) 的非官方 Evolution X 4.3 ROM。该 ROM 预装了 Google apps 和 Pixel goodies，并提供了一些定制功能，如状态栏可见性切换和游戏模式快速设置磁贴。目前的版本也与[红米 Note 9 Pro Max](https://forum.xda-developers.com/redmi-note-9-pro-max) 兼容。

**[下载非官方进化 X](https://forum.xda-developers.com/redmi-note-9-pro/development/rom-evolution-x-ganja-curtana-t4094495)**

### 线性几何 17.1

多亏了 XDA 成员[the lachite](https://forum.xda-developers.com/member.php?u=9609718)的贡献，最知名的定制 rom 之一 LineageOS 也来到了这款手机上。ROM 在许可模式下有 SELinux，蓝牙音频中断，离线充电不显示电池。如果你能忍受这些，你可以把它当作日常驱动。与 Evolution X 不同，这款手机的非官方 LineageOS 17.1 版本没有谷歌应用程序(通常称为 [GApps](https://www.xda-developers.com/open-gapps-android-10-roms/) )。

**[下载非官方 linegeos 17.1](https://forum.xda-developers.com/redmi-note-9-pro/development/rom-lineageos-17-1-t4096947)**

### 小米. eu ROM

如果你真的喜欢 MIUI，但只想摆脱臃肿的软件和广告，请选择小米. eu ROM。定制 ROM 基于中国 MIUI 11 发行版，但已针对欧洲市场进行了本地化。点击下面链接的小米论坛，你会看到闪烁的说明。

**[下载 Xiaomi . eu ROM](https://xiaomi.eu/community/threads/miui-11-0-stable-release.52628/)**

* * *

## Redmi Note 9 Pro 的定制恢复

### 特平

如果你想在你的 Redmi Note 9 Pro 上安装上述任何定制 rom，像 TWRP 这样的定制恢复是一个强制性的先决条件。谢天谢地，著名的开发者 wzsx150 已经为这款手机带来了非官方的 TWRP 支持。IMG 文件需要通过快速启动刷新，默认的中文语言可以很容易地改为英文。

**[下载非官方 TWRP](https://forum.xda-developers.com/redmi-note-9-pro/development/recovery-lrtwrp-recovery-3-4-1-based-t4095301)**

### 线性地质恢复

LineageOS Recovery 是 XDA 成员 [TheMalachite](https://forum.xda-developers.com/member.php?u=9609718) 在为该装置建造 LineageOS 17.1 时所做工作的衍生物。与 TWRP 相比，它相当简单(例如，不支持数据解密)，但当你只需要刷新一个定制的 ROM 时，它就能完成工作。

**[下载非官方 LineageOS 恢复](https://forum.xda-developers.com/redmi-note-9-pro/development/recovery-lineageos-17-1-recovery-t4094581)**