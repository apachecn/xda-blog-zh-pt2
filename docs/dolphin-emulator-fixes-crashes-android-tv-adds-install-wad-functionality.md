# Dolphin Emulator 修复了 Android TV 上的崩溃，并在 Android 上添加了安装 WAD 功能

> 原文：<https://www.xda-developers.com/dolphin-emulator-fixes-crashes-android-tv-adds-install-wad-functionality/>

如果 Android 设备足够强大，你也可以选择在 Android 设备上模仿它们，而不是从地下室找到你的旧游戏机来播放你最喜欢的复古游戏。Dolphin Emulator 是任天堂 GameCube 和 Wii 上最受欢迎的开源仿真器，它实际上可以很好地处理高端设备上的仿真工作，如[一加 7 Pro](https://www.xda-developers.com/oneplus-7-pro-review-gamecube-wii-emulation/) 或[英伟达盾电视](https://www.xda-developers.com/nvidia-shield-tv-super-mario-galaxy/)。Dolphin Emulator 项目背后的开发团队最近发表了一篇博客文章，概述了他们在 4 月份的进展，其中也包含了大量针对 Android 客户端的更改。

## 固定的安卓电视支持

linegeos/TWRP 撰稿人 [webgeek1234](https://github.com/webgeek1234) 修复了一个导致安卓电视客户端崩溃的 bug。显然，Dolphin 模拟器在 Android 电视设备上崩溃了，因为模拟器以“不赞成的方式”弹出了一个弹出窗口。对这一问题的修复是对一行代码的修改，这实质上带回了大屏幕上复古游戏的所有刺激。

## 将 SD 卡设置添加到 GUI

任天堂 Wii 有一个用于存储游戏数据的 SD 卡插槽，但它在 Dolphin Emulator 上基本上没有用，因为它的目标平台(个人电脑和当前一代 Android 设备)提供了更多的存储空间。不过《超级粉碎兄弟》Brawl 的一些 mod 使用了 SD 卡，导致 Android 版海豚模拟器中的那些 mod 很难启用。在最新的 Dolphin 模拟器版本中(准确地说是从 [*5.0-11849*](https://dolphin-emu.org/download/dev/master/5.0-11849/) )，您可以启用“插入 SD 卡”选项来创建一个 128MB 的虚拟 SD 卡。然而，Dolphin 仍然不能使用真正的 SD 卡。

当配置 Wii 遥控器时，你必须完全重启 Dolphin 才能使更改生效。现在，更改会立即反映出来，并在您重新配置 Wii 遥控器设置时生效。

## 添加安装 WAD 功能

WiiWare(来自任天堂 Wii 网上商店的软件包)以。wad 文件。由于[构建 *5.0-11909*](https://dolphin-emu.org/download/dev/master/5.0-11909/) ，安装这些很容易。Android 中 Dolphin 模拟器中的 WAD 文件，带有新的“安装 WAD”菜单选项。

该团队还简化了外部纹理加载机制，以及一些图形渲染和网络修复。你可以看看下面链接的完整博文，了解所有的变化。

[app box Google play " org . dolphine mu . dolphine mu "]

* * *

**来源:[海豚模拟器博客](https://dolphin-emu.org/blog/2020/05/05/dolphin-progress-report-april-2020/)**