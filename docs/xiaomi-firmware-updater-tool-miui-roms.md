# 小米固件更新器是一个工具，可以创建可刷新的 MIUI ROMs 文件

> 原文：<https://www.xda-developers.com/xiaomi-firmware-updater-tool-miui-roms/>

# 小米固件更新器是一个工具，可以创建可刷新的 MIUI ROMs 文件

来自 XDA 的小米固件更新程序是公认的开发者 yshalsager 自动创建新 MIUI ROMs 的可闪存 ZIP 文件，节省了开发者必须更新他们的定制固件的麻烦。

尽管小米每年都会发布很多设备，但该公司一直坚持向旧款智能手机推出新版的定制安卓皮肤 MIUI。这表明了它对 ROM 的承诺，但它有意想不到的副作用，阻止了社区中的一些开发人员更新他们的定制固件。这也是 XDA 认可开发者 [yshalsager](https://forum.xda-developers.com/member.php?u=6084385) 发布小米固件更新工具的原因之一，它将更新 Xiaomi 设备固件的权力放在了用户手中。

小米管理着几个不同版本 MIUI 的更新渠道。它的一个 OEM ROM 版本是专门针对中国的，有稳定版和开发者版。在其他市场销售的设备使用 MIUI 的全球版本，该版本也有稳定版和开发者版。开发者 OEM rom 每周五由小米更新，而稳定的 OEM rom 每两周更新一次。随着新软件的快速发布，很容易理解为什么一些社区开发者选择不在每次 MIUI 更新可用时更新他们的固件。

小米固件更新工具通过为十几款设备自动下载官方 MIUI ROMs 的全球/中文和稳定/开发者版本，解决了这个问题。它获取 MIUI 固件并提取**固件更新**文件夹，用自动编写的“更新程序脚本”生成一个可刷新的 ZIP 文件，并自动上传到 yshalsager 为此设置的两台服务器上。

该工具并不支持每一款小米设备，但开发者已经很大方地给了我们一份小米固件更新程序支持的智能手机的完整列表。

### 小米固件更新程序支持的设备

*   HM3:小米红米 3 (ido)
*   HM3S:小米红米 3S/Prime/3X(陆地)
*   HM4:小米红米 4(普拉达)
*   HM4A:小米红米 4A(劳力士)
*   HM4Pro:小米红米 4 Prime (markw)
*   HM4X:小米红米 4X(桑托尼)
*   HM5:小米红米 5(玫瑰色)
*   HM5A:小米红米 5A (riva)
*   HM5Plus:小米红米 5Plus(文斯)
*   HMNote3Pro:小米红米 Note 3 Pro (kenzo)
*   HMNote3ProtwGlobal:小米红米 Note 3 特别版(凯特)
*   HMNote4:小米红米 Note 4 (nikel)
*   HMNote4X:小米红米 Note 4X (mido)
*   HMNote5A:小米红米 Note 5A Prime (ugg)
*   HMNote5ALITE:小米红米 Note 5A (ugglite)
*   HMPro:小米红米 Pro(欧米茄)
*   米 4c:小米米 4c(天秤座)
*   MI4s:小米米 4S (aqua)
*   MI5:小米米 5(双子座)
*   米 5S:小米米 5s(摩羯座)
*   米 5SPlus:小米米 5s Plus(纳)
*   MI5X:小米米 5X(蒂芙尼)
*   MI6:小米 Mi 6 (sagit)
*   MIMAX:小米 Mi Max(氢)
*   MIMAX2:小米 Mi Max 2(氧气)
*   MIMAX652:小米 Mi Max Prime(氦)
*   MIMIX:小米 Mi MIX(锂)
*   MIMIX2:小米米 MIX 2 (chiron)
*   MINote:小米 Mi Note(处女座)
*   减 2:小米记 2(天蝎座)
*   MINote3:小米米 Note3(杰森)
*   MIPAD3:小米 mi pad 3(capu)

小米固件更新程序可以在 XDA 论坛和 Github 上免费获得。

* * *

[**在我们论坛**](https://forum.xda-developers.com/android/software-hacking/devices-xiaomi-firmware-updater-t3741446) 查看小米固件更新器