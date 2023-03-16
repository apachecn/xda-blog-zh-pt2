# 摩托罗拉 Moto Z Play & Moto G 2015 获得非官方安卓派端口

> 原文：<https://www.xda-developers.com/motorola-moto-z-play-moto-g-2015-unofficial-android-pie-ports/>

没过多久，开发社区就开始将 Android 9 Pie 移植到更老的设备上。Android Pie 的源代码是在 8 月 6 日谷歌 Pixel/Xl 和谷歌 Pixel 2/XL 的官方更新推出后上传的。对于小米设备，开发社区将 Android Pie 移植到旧设备上的速度特别快。小米红米 Note 4 [获得了一个稳定的 Android 9 Pie 端口，一切正常](https://www.xda-developers.com/xiaomi-redmi-note-4-android-pie/)，然后[该端口被移植到小米红米 4X](https://www.xda-developers.com/xiaomi-mi-3-xiaomi-mi-4-xiaomi-redmi-4x-android-pie-ports/) 。其他小米手机如小米 Mi 3/Mi 4、小米 Mi A1 和小米 Redmi Note 5 Pro [也获得了非官方的 AOSP Android 9 端口](https://www.xda-developers.com/xiaomi-redmi-note-5-pro-xiaomi-mi-a1-android-pie/)。在其他设备制造商方面，受欢迎的华硕 ZenFone Max Pro M1 [已经获得了 AOSP Android 9 Pie port](https://www.xda-developers.com/asus-zenfone-max-pro-m1-android-pie-port/) 。现在，摩托罗拉 Moto Z Play 和 Moto G 2015 加入了获得非官方馅饼端口的手机名单。

最近，摩托罗拉的安卓版本更新记录不是特别好。例如， [Moto G5 和 Moto G5S 系列仍然没有得到 Android Oreo](https://www.xda-developers.com/motorola-moto-g5-android-8-1-oreo-soak/) 的广泛推广。Moto E5 系列[将不会收到官方的 Android Pie 更新](https://www.xda-developers.com/moto-z2-moto-z3-moto-x4-moto-g6-series-android-pie-updates/)，尽管这款手机是在今年 4 月发布的。摩托罗拉通常承诺为预算/较低的中端 Moto G 系列提供单一的 Android 版本更新。这就是为什么开发社区的贡献对于希望延长设备生命周期的用户非常重要。

## 摩托罗拉 Moto Z Play 的 AOSP Android 9 Pie

AOSP Android Pie 已经移植到摩托罗拉 Moto Z Play 上(设备代号:addison)。不起作用的东西包括加密和 VoLTE，SELinux 被设置为 permissive。还有，不支持 Moto Mods。

Moto Z Play 用户需要有一个 Android Nougat 或 Android Oreo 引导程序，否则 TWRP 会通过向用户显示错误引导程序的消息来拒绝安装。用户可以按照[链接线程](https://forum.xda-developers.com/showpost.php?p=74069195&postcount=91)中提到的说明升级到更新的 bootloader。开发者还注意到加密还不被支持(因为高通的消息来源还没有公布)，这意味着用户需要通过 TWRP**格式化数据**或者使用下面的快速启动命令:

```
 fastboot erase userdata 
```

这样做，他们将会丢失内部存储器中的所有数据，包括应用程序、照片和下载。关于如何刷新 ROM 的说明可以在[源码链接](https://forum.xda-developers.com/moto-z-play/development/rom-android-source-project-9-t3829881)找到。

[button link = https://forum . xda-developers . com/Moto-Z-Play/development/rom-Android-source-project-9-t 3829881 " Icon = " Select a Icon " side = " left " target = " " color = " f 85050 " text color = " ffffff "]为摩托罗拉 Moto Z Play 下载 AOSP Android 9 Pie[/button]

## Moto G 2015 的非官方 LineageOS 16.0

LineageOS 16.0 的非官方版本可用于 Moto G 2015(设备代码名称；鱼鹰)。该版本的开发人员声明，它已被修改为挂载/cache 分区，因为/vendor 分区和所有设备 blobs 已被合并并移动到 vendor。旧的 Moto blobs 已被转移到供应商和单独推出，开发人员说，它使 ROM 更快更轻。因此，它处于项目三重支持的早期阶段，但它不是一个完整的项目三重构建。

除了不确定的小错误之外，不工作的列表包括 VoLTE 和强制 SELinux。ROM 需要厂商支持的 TWRP，可以从这里下载[。](https://forum.xda-developers.com/2015-moto-g/development/unofficial-twrp-3-2-3-osprey-t3829999)

[**为 Moto G 2015**](https://forum.xda-developers.com/2015-moto-g/development/rom-lineageos-16-0-t3830213) 下载非官方 LineageOS 16.0