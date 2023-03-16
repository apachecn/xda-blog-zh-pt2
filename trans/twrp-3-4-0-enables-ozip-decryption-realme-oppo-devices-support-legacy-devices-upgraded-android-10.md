# TWRP 3.4.0 支持 Realme/OPPO 设备的 OZIP 解密，并支持升级到 Android 10 的传统设备

> 原文：<https://www.xda-developers.com/twrp-3-4-0-enables-ozip-decryption-realme-oppo-devices-support-legacy-devices-upgraded-android-10/>

无论你是一个经验丰富的 flashinging 爱好者，还是一个 flash 场景的新手，你都可能在某个时候使用过 Team Win Recovery Project，或者简称为 TWRP。定制恢复解决方案正式支持数百款安卓设备(包括[电视盒子](https://www.xda-developers.com/twrp-adds-official-support-xiaomi-redmi-note-7-lenovo-k10-note-vivo-y51l-amlogic-x96-max/)和[智能手表](https://www.xda-developers.com/zte-quartz-twrp-factory-images-kernel-source/))。另一方面，修改社区已经设法在非官方版本中集成了独特的功能，如[真正的双引导](https://www.xda-developers.com/unofficial-twrp-enables-true-dual-boot-oneplus-7-pro-5g/)。由于 Android 世界的不断变化，TWRP 需要适应更新的分区方案和加密逻辑，同时保持与传统设备的兼容性。该项目现在已经收到了一个重大更新，将 TWRP 的版本号提升到 3.4.0。

正如你们许多人所知，TWRP 开发者[在实现定制恢复与 Android 10 完全兼容的过程中面临了几个挑战](https://www.xda-developers.com/twrp-lead-explains-android-10-support-custom-recovery/)。TWRP 代码库的很大一部分需要修改，以支持谷歌在 AOSP 恢复实施中引入的变化。TWRP 3.4.0 还不支持动态/逻辑分区，这是支持 Android 10 设备所必需的。然而，它确实修复了对升级到 Android 10 的传统设备的支持，但保留了旧的分区方案。

除了具有增强的解密模块，最新版本的 TWRP 在系统根和 [A/B 双分区](https://www.xda-developers.com/how-a-b-partitions-and-seamless-updates-affect-custom-development-on-xda/)处理方面有很多改进。A/B 安装程序 zip 格式完全是基于 XDA 资深认可开发者 [osm0sis](https://forum.xda-developers.com/member.php?u=4544860) 和 XDA 认可开发者 [arter97](https://forum.xda-developers.com/member.php?u=4898097) 的贡献从零开始重新编写的。此外，OZIP 解密现在得到了原生支持，这要归功于 XDA 公认的开发者 mauronofrio。这意味着 OPPO 和 Realme 智能手机用户可以直接从 TWRP 闪存官方固件包，而无需事先将其转换为标准 ZIP 文件。

更新的完整变更日志可以在下面找到:

### twrp 3.4.0-0 变更日志

*   系统作为根(SAR)
    *   使用 SAR - dianlujitao 修复备份和恢复
    *   系统挂载点- Chaosmaster
    *   ORS 混沌大师
    *   Zip 安装- Chaosmaster
    *   system_root 绑定挂载到/system - Chaosmaster
    *   合成孔径雷达混沌主控的自动检测
*   摘要
    *   修复子分区摘要的创建(从去年开始，bugfix 被应用到许多设备上)
*   加密
    *   ext4Crypt 包装密钥更新- Peter Cai
    *   如果导出失败，修复升级加密密钥- Peter Cai
    *   修复对没有元数据分区的设备的包装密钥支持
    *   使用块映射文件写入 ORS - CaptainThrowback 中的/data 时，不要跳过解密
    *   FDE -首先解密主密钥-机器人
    *   vold_decrypt -自动设置 Android 版本和补丁级别
    *   通过 twrp 标志设置包装解密支持- Peter Cai
    *   除非需要，否则不要尝试包装支持- mauronofrio
    *   还原/data/cache - Bigbiff 上的 ext4 策略
    *   多用户解密-诺亚·雅各布森
    *   FDE 重试-机器人
*   WRP 应用程序
    *   检查 app - Bigbiff 后卸载系统
*   预建更新-
    *   Android . hardware . confirmation ui @ 1.0-cryptomilk
*   编译修复:
    *   TW_EXFAT_FUSE 编译修复- Bigbiff
    *   libuuid -隐乳
    *   “找不到 system/etc/ld.config.txt”错误- Martin Dünkelmann
*   语言更新:
    *   葡萄牙-瓦斯科·马查多
    *   荷兰人伊恩·麦克唐纳
    *   土耳其-征服者面包师
    *   备份本地化 _Tar: Ian Macdonald
*   ld.config.txt
    *   8.x 树的更新- CaptainThrowback
    *   修复/sbin - CaptainThrowback 的搜索路径
    *   /sbin 应该出现在搜索路径的第一位- Ian Macdonald
*   一般错误
    *   修复持久日志存储-syberxen
    *   压缩持久日志- Bigbiff
    *   FB2PNG 编译错误- Bigbiff
    *   从备份中排除 per _ boot-Darth 9
    *   卸载所有指向同一个块设备的目录
    *   空白屏幕修复-肖恩·霍伊特
    *   android-9+ - mauronofrio 上的默认工具箱
*   清理-
    *   注释中的拼写错误修复- VDavid003
    *   ext4crypt - CaptainThrowback 中的换行
    *   TW_OEM_BUILD 编译问题- Patrick Zacharias
    *   修复依赖性要求- Dees_Troy
    *   修复 BB 和工具箱的符号链接
*   引导程序消息
    *   清理-亚历山德罗阿斯顿
    *   添加可配置的偏移
*   错误清除
    *   事件错误和解密错误- mauronofrio
    *   使用 copy_file 从/etc - CaptainThrowback 复制文件
    *   对/acct 的 ueventd 访问-init-cryptomilk 中的早期目录创建
*   触觉论
    *   TSP 驱动程序- LameMonster82
    *   QTI 输入- AndroidableDroid
*   更新引擎
    *   阅读所有断言-埃尔南·卡斯塔尼翁
*   重置 prop
    *   从 Magisk-CaptainThrowback & mauronofrio 添加 Resetprop
    *   从源代码编译- Chaosmaster
    *   修复 android-7 和更早版本的混乱大师
    *   清理 properties - AndroidableDroid 中的空格
*   性能
    *   添加属性覆盖- Chaosmaster
*   备份工具
    *   用于备份工具的 A/B 安装的装载系统和供应商- Chaosmaster
*   twrpTar
    *   修复使用 pigz 和 openaes 时备份冻结的问题
*   Zip 安装
    *   A/B zip 安装到非活动插槽的信息- Chaosmaster
    *   重新启动到系统按钮现在允许在 zip 安装后重新启动到不同的分区
    *   进度条返工-混沌大师
*   神奇的更新
    *   从源代码更新二进制文件- AndroidableDroid
*   A/B 更新程序 Zip 模板
    *   使用新的通用模板和最新的 magiskboot - osm0sis 从头开始重写 A/B 安装程序 zip
    *   较新的 2SI SAR A/B 设备上 recovery_a/recovery_b 分区内存磁盘的安装程序 zip 支持- osm0sis
    *   为所有产品 A/B 设备生成安装程序 zip
    *   提高安装程序的 zip 转储/写入速度，并添加更多的错误捕获功能
*   OZIP 加密支持
    *   添加 OZIP 加密- mauronofrio
*   文件选择器
    *   文件选择器支持更多的扩展名

添加的 resetprop 支持用于在 TWRP 源代码中创建 libresetprop，这使得只读 prop 很容易被设备维护人员覆盖。这有助于确保广泛的兼容性股票只读存储器，解密等。但不影响最终用户。

您可以从以下链接的官方网站为您的设备下载最新版本的定制恢复。不要忘了看看特定于设备的讨论线程，它们通常是在各自的 XDA 分论坛下创建的。

**[为您的设备下载 TWRP](https://twrp.me/Devices/)**

TWRP 官方应用是从你的设备上下载最新版本的另一个选择。通过 root 访问权限，这个方便的工具还可以用来安装更新的 TWRP 版本，而无需重启进行恢复。

[应用程序框 Google play me . twp . twp . twp 纸]