# phh 的定制 Android 10 GSI 增加了对 Razer 手机的更好支持和新的“我的设备”设置

> 原文：<https://www.xda-developers.com/phh-custom-android-10-gsi-adds-better-support-razer-phone-new-my-device-settings/>

谷歌首次宣布 Android 8.0 Oreo 的 Treble 项目，旨在为 Android 设备带来更快的更新，并最大限度地减少长期存在的碎片化问题。XDA 的开发者社区很快发现了这种模块化方法的另一个有趣的好处:能够在任何支持的设备上通过可解锁的引导程序引导 AOSP 通用系统映像(GSI)。在通过在华为 Mate 9 上成功引导 AOSP·GSI 创造历史之后，XDA 公认的开发者 [phhusson](https://forum.xda-developers.com/member.php?u=1915408) 已经成为社区定制 GSI 领域的首席导师。这位开发者现在已经用一个新选项更新了他基于 Android 10 的项目 Treble GSI，又名*嘎嘎 Phh-Treble* ，该选项极大地简化了各种特定于设备的 Treble 应用预设的设置过程。

**[嘎嘎 Phh——高音——XDA 讨论线程](https://forum.xda-developers.com/project-treble/trebleenabled-device-development/aosp-10-0-quack-phh-treble-t3992559)**

被称为“**我的设备**”的新部分可以在高音设置下找到。通过这个选项，终端用户只需用手指轻轻一点，就可以直接联系他们的设备维护人员，还可以访问该设备的用户社区。另一方面，想成为维护者的开发者可以通过[提交一个简单的拉请求](https://github.com/phhusson/treble_presets/)来登记他们的名字。该部分也是您需要应用的大多数设备特定修复的中心位置，以便为您的 Android 设备微调 GSI(例如，调整特定供应商的指纹属性)，消除繁琐的试错部分。下面是由 [phhusson](https://forum.xda-developers.com/member.php?u=1915408) 提供的屏幕录像，展示了新推出的“我的设备”设置。

最新版本的嘎嘎 Phh-Treble，标签为 *v220* ，也引入了几个平台修复和一些新功能，如使用家庭硬件按钮唤醒设备。此外，有一个新的修复，可以正确地暴露 Razer 手机上所有支持的刷新率。Android 安全补丁级别(SPL)没有变化，尽管 [phhusson](https://forum.xda-developers.com/member.php?u=1915408) 已经[将 2020 年 6 月的安全补丁与他的定制项目 Treble GSI 整合。](https://www.xda-developers.com/custom-aosp-project-treble-gsi-gets-updated-with-june-2020-security-patches-netflix-hd-support-for-the-xiaomi-mi-9-and-redmi-note-9s-and-more/)

完整的变更日志如下:

*   修复启动 [Moto One 宏](https://www.xda-developers.com/motorola-one-macro-launches-with-budget-specs-and-a-macro-camera/)
*   修复馅饼供应商的媒体
*   主页硬件按钮可以唤醒设备
*   高音设置现在列出了分辨率除了 FPS，一些设备可以暴露多个分辨率和多个 FPS。
*   修正双击唤醒[银河 A51](https://forum.xda-developers.com/galaxy-a51)
*   在 [Moto One Action](https://forum.xda-developers.com/one-action) 上修复指纹手势
*   修复各种 SELinux 修复，以改善三星设备上的集成 su
*   修复某些三星设备上的最近/主页/返回键
*   曝光 Razer 手机上的所有刷新率(最初只有 120Hz 可用)

**[下载呱呱 Phh-高音 v220](https://github.com/phhusson/treble_experimentations/releases/tag/v220)**

打算试用 phh 的 Android 10 GSI？您应该首先使用下面链接的 Treble Info 应用程序确定您的设备型号。还建议用户进行设备外备份，因为刷新过程将要求您对设备进行出厂重置。

[app box Google play " tk . hack 5 . treble check "]