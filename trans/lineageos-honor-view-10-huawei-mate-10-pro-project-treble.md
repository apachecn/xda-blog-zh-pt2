# LineageOS 15.1 现可用于 Honor View 10、华为 Mate 10 Pro 和其他 Project Treble 兼容设备

> 原文：<https://www.xda-developers.com/lineageos-honor-view-10-huawei-mate-10-pro-project-treble/>

投射高音。你们中的一些人可能已经厌倦了听到这个消息，而另一些人对任何与这个计划相关的消息都欣喜若狂。我们在 XDA [对它带来的东西感到无比兴奋](https://www.xda-developers.com/how-project-treble-revolutionizes-custom-roms-android-oreo/),每周都有新的事情发生，增加了这种兴奋感。最近，一名开发者能够为[小米 Redmi Note 4](https://www.xda-developers.com/xiaomi-redmi-note-4-project-treble/) 带来完整的项目三重兼容性。一部采用联发科 SoC 的[不起眼的手机](https://www.xda-developers.com/obscure-mediatek-phone-kernel-source-android-oreo-project-treble/)也能够启动通用的 Android 版本，为延长设备寿命铺平了道路——远远超过官方制造商支持的期限。现在，一名开发人员已经使基于 Treble 的定制 rom 对用户更具吸引力，因为第一个 LineageOS 15.1 版本可用于 Honor View 10 和华为 Mate 10 Pro(它也可用于其他 Treble 兼容设备！)

* * *

## Honor View 10、华为 Mate 10 Pro 和其他高音设备的 LineageOS 15.1

概括地说，Project Treble 是 Android 工作方式的一个非常低级的架构变化，从 Android 8.0 Oreo 开始。基本上，所有供应商硬件抽象层(HALs，Android 与硬件组件交互的二进制文件)都被移动到一个单独的供应商分区，并通过 HAL 接口定义语言(HIDL)以更标准化的方式与 Android 框架(OS)交互。谷歌通过供应商测试套件(VTS)强制执行这一标准化，设备必须通过该套件才能获得认证，以便与 Google Play 应用和服务一起发布。VTS 的要求之一是 Treble 兼容设备必须能够引导通用系统映像(GSI)，这基本上只是从 Android 开源项目(AOSP)构建的股票 Android Oreo 系统映像。

这一要求对定制 ROM 社区的好处是，Treble 兼容设备至少不需要太多的黑客来启动和运行一个基本的 AOSP ROM。事实上，像华为 Mate 10 Pro(T1)、T2 Honor 8 Pro、Honor 9(T3)和 T4 Honor View 10(T5)这样的设备都有非常简单的 AOSP Android Oreo rom。但大多数用户对运行 XDA 资深会员 phhusson 的 AOSP ROM 不感兴趣，因为它缺少太多开箱即用的功能:没有夜灯，没有自适应亮度，没有环境显示，等等。当然，你可以通过安装一个[定制框架覆盖](https://forum.xda-developers.com/project-treble/trebleenabled-device-development/overlay-enable-night-light-adaptive-t3741965)、[暴露框架](https://www.xda-developers.com/xposed-framework-for-android-oreo-beta/)，或者安装[底层](https://www.xda-developers.com/tag/substratum-tutorials/)来使事情变得漂亮一点，但是在设置这一切的时候需要付出很多努力。

对于那些只想快速忘记的人来说，这就是 XDA 认可的开发者 [Luk1337](https://forum.xda-developers.com/member.php?u=5075128) 和[Luca 020400](https://forum.xda-developers.com/member.php?u=5778309)LineageOS 15.1 的用武之地。它基于[安卓 8.1 奥利奥](https://www.xda-developers.com/android-8-1-oreo-final-release-imminent/)，就像以前的 GSIs 一样，但它也带有 LineageOS 众所周知的所有酷的附加功能。这包括 LiveDisplay、隐私保护、按钮定制等等。如果你有一个项目高音兼容设备，并有兴趣尝试 AOSP，这可能是你的完美选择。

激动吗？想要在您的[高音兼容设备](https://www.xda-developers.com/project-treble-android-oreo/)上刷新 LineageOS 15.1？在我引导你到可以下载 ROM 的论坛之前，有一件非常重要的事情我们必须解决。

警告:创建这个 ROM 的 LineageOS 开发者在 Honor View 10 论坛上发布了这个消息，并声明它可以在任何装有海思麒麟 970 的设备上工作。你可以尝试在你的 Treble 兼容设备上刷新这个 ROM，但是要注意，如果你遇到任何错误，开发者可能不会支持你。值得注意的是，[开发者由于](https://www.xda-developers.com/honor-announces-developers-honor-view-10-recipients/)[荣誉开源项目](https://www.xda-developers.com/honor-open-source-program-honor-view-10/)而获得了他们的荣誉 View 10 设备，因此这是他们官方支持的唯一设备。

既然已经解决了这个问题，下面介绍如何在 Project Treble 兼容设备上安装 LineageOS 15.1。

* * *

## 如何在 Honor View 10、华为 Mate 10 Pro 或其他 Treble 兼容设备上安装 LineageOS 15.1

1.  对所有重要文件进行设备外备份。很有可能你需要一个完整的数据擦除才能启动。
2.  解锁您的设备的引导加载程序。[这是](https://forum.xda-developers.com/honor-view-10/development/honor-view-10-bootloader-unlock-t3749426)Honor View 10 的指南，[这是](https://www.xda-developers.com/unlock-bootloader-root-huawei-mate-10/)Mate 10 系列的指南。
3.  重新启动引导程序。最简单的方法是插上你的手机，关机，然后按住电源+音量键。
4.  从本论坛线程下载 linegeos 15.1[。](https://forum.xda-developers.com/honor-view-10/development/rom-lineageos-15-1-t3753000)
5.  打开命令提示符或终端窗口，导航到从上面下载系统映像的同一目录。
6.  输入以下命令:`fastboot flash system system.img`
7.  注意:用您下载的映像的确切名称替换“system.img”。在本文发表时，它将是“system_20180221.img”
8.  重启手机。如果你的手机开始引导循环，让它继续，直到它把你带到华为的恢复屏幕，要求你做一个低级数据擦除。用电源按钮选择那个选项，让它做它自己的事。
9.  数据擦除完成后，您应该可以成功启动 LineageOS 15.1。

之后，你可以在设备上自由定制你想要的任何东西。

* * *

*专题图片致谢:XDA 资深会员[胡森](https://forum.xda-developers.com/member.php?u=1915408)。从左到右显示的设备:未公开的 MSM8937 Treble 兼容设备，华为 Mate 9，Honor View 10，Allview Viper V3。*