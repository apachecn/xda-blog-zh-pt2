# 开发者将 Android 10 和 Project Treble 带到 HTC U11

> 原文：<https://www.xda-developers.com/developers-bring-android-10-project-treble-htc-u11/>

HTC 的智能手机部门[可能还没有死](https://www.xda-developers.com/htc-still-making-phones-will-launch-5g-smartphone-this-year/)，但是围绕现有 HTC 手机的整个软件更新情况是一团乱麻。这家台湾手机制造商很难向其手机提供 Android 10 更新，由于其 Android One 品牌， [HTC U11 Life 是一个例外](https://forum.xda-developers.com/u11-life/how-to/htc-u11-life-android-one-android-10-t4062763)。例如，HTC U11 的常规版本[被安卓派](https://www.xda-developers.com/htc-u11-android-pie-taiwan/)卡住了。谢天谢地，这款手机的用户现在有机会品尝 Android 10 了。由于 XDA 辉煌的开发社区，HTC U11 不仅可以启动 LineageOS 17.1，而且该设备还符合 Project Treble。

**[HTC U11 XDA 论坛](https://forum.xda-developers.com/u11)**

XDA 资深成员 [Golv](https://forum.xda-developers.com/member.php?u=4445238) ，以及 XDA 认可的开发商 [tomascus](https://forum.xda-developers.com/member.php?u=4675360) 和 XDA 认可的开发商 [Flinny](https://forum.xda-developers.com/member.php?u=4350964) ，目前正在为 HTC U11 维护 LineageOS 17.1 的非官方构建。ROM 在许可模式下有 SELinux，VOIP 呼叫体验可能会很挑剔，但除此之外，作为日常驱动程序还是很稳定的。那些运行 HTC Sense 固件的人必须在刷新 ROM 之前格式化数据分区(这将删除内部存储的内容),所以请执行完整的备份。

**[为 HTC U11](https://forum.xda-developers.com/u11/development/rom-lineageos-17-1-ocn-updated-2020-03-t4075493)** 下载非官方 LineageOS 17.1

基于 Snapdragon 835 的 HTC U11 最初发布时搭载了 Android 7.1 牛轧糖，因此这款手机正式与 Project Treble 不兼容。在一次“tre Belize”it 的任务中，XDA 认可的开发人员 [mikalovtch](https://forum.xda-developers.com/member.php?u=3184278) 和来自 Team Venom 的其他几名开发人员决定通过修改股票分区表来创建一个专用的供应商分区，以便为适当的项目 Treble & [通用系统映像](https://www.xda-developers.com/tag/generic-systemimage/) (GSI)提供支持。这个 mod 本质上延长了这款手机的寿命，因为未来版本的 Android 理论上可以轻松移植到智能手机上。

**[项目高音为 HTC U11 — XDA 下载讨论线程](https://forum.xda-developers.com/u11/development/05-31-project-treble-alpha-1-htc-u11-t4107669/)**

请记住，对您的设备进行**重新分区将会擦除所有内容**，因此请准备好足够的备份。如果您需要恢复旧的分区布局，还建议用户预先下载特定型号的 RUU 包。请注意，这些模块不适合普通用户，仅推荐给有经验的用户。