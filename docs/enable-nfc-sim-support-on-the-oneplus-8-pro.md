# 在一加 8 专业版上启用 NFC SIM 卡支持

> 原文：<https://www.xda-developers.com/enable-nfc-sim-support-on-the-oneplus-8-pro/>

# 在一加 8 专业版上启用 NFC SIM 卡支持

XDA 成员 timlu85 创建了一个 Magisk 模块，可以解锁一加 8 Pro 上的 NFC SIM 卡支持。点击此处了解更多信息！

NFC 是近场通信的缩写，是一种短程无线通信协议，目前主要用于非接触式支付终端。NFC 论坛也在研究一种无线充电解决方案，让你可以通过 NFC 芯片而不是专用的无线线圈为你的设备充电。然而，智能手机制造商[经常在他们的手机](https://www.xda-developers.com/xiaomi-oppo-lg-alcatel-fewer-nfc-phones/)上放弃 NFC 支持——特别是在中国和印度销售的手机上——因为一些国家主要使用可扫描二维码作为非接触式支付的首选模式。像一加 8 Pro 这样的手机不支持 NFC 模拟人生，即使该设备配备了 NFC 芯片。幸运的是，您可以通过一个简单的 mod 来启用对该特性的支持。

**[一加八大职业 XDA 论坛](https://forum.xda-developers.com/oneplus-8-pro)**

XDA 成员 timlu85 提出了一个 Magisk 模块，可以在一加 8 Pro 的任何地区版本上立即启用 NFC-SIM 卡支持。该模块无系统地挂钩到预定义的 OEM 功能列表，以便手机可以检测此类 sim 的 NFC 部分。它还负责修补供应商(恩智浦半导体)提供的默认 NFC HAL 配置。作为一个通用模块，它可以安装在一加 8 Pro 的每个版本的 OxygenOS 上。

安装模块后，您必须重启手机并重新启用 NFC 开关，以强制操作系统重新加载修改后的配置数据。一加 8 Pro 的当前版本的模块是针对中华电信的 NFC sim 进行测试的，尽管它应该也可以兼容其他已经激活的 NFC sim。

**[一加 8 Pro 的 NFC SIM 卡启用码— XDA 下载与讨论线程](https://forum.xda-developers.com/oneplus-8-pro/themes/magisk-module-enable-nfc-sim-function-t4113839)**

这种模式的概念并不是全新的，因为上面提到的模式是基于同一用户为一加 6T 创建的类似模式。这个补丁背后的实际想法可以追溯到 2017 年，当时 XDA 高级成员 [snowwolf725](https://forum.xda-developers.com/member.php?u=2447659) [演示了](https://forum.xda-developers.com/oneplus-5/themes/mod-nfc-swp-sim-enabler-oneplus-3-3t-t3650482)一种在 OnePlus 3/3T 和 OnePlus 5 上启用 NFC-SIM 支持的方法。