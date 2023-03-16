# 这是三星 Galaxy S9 在 AOSP Android Oreo 上运行，这要感谢 Project Treble

> 原文：<https://www.xda-developers.com/samsung-galaxy-s9-aosp-android-oreo-project-treble/>

三星的最新旗舰产品——Galaxy S9 和 Galaxy S9+ ,成了人们谈论的话题。这些设备是去年的[三星 Galaxy S8 系列](https://www.xda-developers.com/samsung-galaxy-s9-s9-plus-hands-on/)的增量升级，尽管它们增加了许多相机增强功能，如可变光圈。重要的是，三星 Galaxy S9 设备是三星首次推出搭载 Android 8.0 Oreo 的设备，这意味着它们兼容[Project Treble](https://www.xda-developers.com/tag/project-treble/)。这意味着，与之前的三星旗舰产品相比，这些设备在启动和运行 AOSP Android Oreo 时应该更容易——事实似乎也是如此。一名测试人员成功地在他的 Exynos Galaxy S9 上启动了 Project Treble Generic System Image(GSI ),我们希望这将为设备的未来开发铺平道路。

在上面的截图中，我们的测试人员，XDA 资深会员 [iamnotkurtcobain](https://forum.xda-developers.com/member.php?u=3117242) ，在 XDA 知名开发者 [minz1](https://forum.xda-developers.com/member.php?u=7652989) 的帮助下，能够在他的 Exynos Galaxy S9 设备上启动 AOSP Android 8.0。他正在运行的 ROM 是 XDA 资深成员 [phhusson](https://forum.xda-developers.com/member.php?u=1915408) 的 [phh-Treble ROM](https://forum.xda-developers.com/project-treble/trebleenabled-device-development/experimental-phh-treble-t3709659) 。根据他的简短测试，Wi-Fi、蓝牙、NFC、指纹扫描仪、摄像头、移动数据等功能都可以工作。与三星 Galaxy S8 仅提供 AOSP ROM 相比，这已经是一个巨大的进步。

目前，Android 8.1 Oreo ROM 没有在设备上启动，因此测试人员必须使用最新的 8.0 系统映像(这也是为什么安全补丁版本看起来如此旧的原因。)我们 Telegram 组的开发人员正在努力解决这个问题，但是考虑到目前只有一个测试人员，协调 bug 修复有点困难。然而，一旦 AOSP Android 8.1 Oreo 工作，将有可能测试基于 Galaxy S9 构建的 [LineageOS 15.1](https://www.xda-developers.com/lineageos-honor-view-10-huawei-mate-10-pro-project-treble/) 或 [CarbonROM](https://www.xda-developers.com/carbonrom-honor-view-10-project-treble-devices/) 。不幸的是，某些硬件功能如虹膜扫描仪将无法工作，因为它不被 AOSP 支持(虽然它[可能会在未来的版本](https://www.xda-developers.com/iris-scanners-native-support-android-p/))。

请记住，这只适用于 Exynos 三星 Galaxy S9，因为刷新 Project Treble GSI 需要解锁的引导加载程序，这在骁龙型号上是不可能的。此外，三星的 bootloader 不支持 fastboot 协议，所以你必须找到一种替代方法来刷新 ROM。当前的[TWRP 版本](https://www.xda-developers.com/samsung-galaxy-s9-official-twrp/)似乎不适用于这个项目，所以我们不得不通过 root 访问将映像直接刷新到他的系统分区来运行我们的测试程序——换句话说，这个过程目前是一个大问题。

不管怎样，我们都很期待这一天的到来。在定制开发方面，骁龙设备一直优于 Exynos 设备，但由于 Project Treble，移植 AOSP ROM 的最困难部分——让它启动并运行最基本的硬件功能——被简化了。有了[内核源代码](https://www.xda-developers.com/samsung-galaxy-s9-kernel-source/)的可用性，剩下的问题也可以得到解决。我们将随时为您更新 Exynos 三星 Galaxy S9 和 Galaxy S9+上 AOSP 的任何未来发展。