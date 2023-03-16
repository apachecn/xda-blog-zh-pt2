# Bliss OS，一个用于桌面电脑的 Android ROM，现在支持 Vulkan 图形

> 原文：<https://www.xda-developers.com/bliss-os-android-rom-desktop-pc-vulkan-graphics-api-support/>

Android 是世界上最受欢迎的智能手机操作系统，但它在桌面上没有任何显著的存在。如果你曾经想知道如何在你的桌面上运行 Android，那么 [Bliss OS 将自己](https://www.xda-developers.com/early-bliss-os-build-android-pie-pc/)展示为 Android x86 的可能解决方案之一。[早在 2019 年 4 月](https://www.xda-developers.com/bliss-os-android-pie-x86-pc-google-play-store/)，基于 Android Pie 面向 x86 PCs 的 Bliss OS 在谷歌 Play 商店支持下发布。现在，几天前，这个项目背后的团队已经更新了其 Android 9 Pie 版本，支持 Vulkan Graphics API。

Bliss OS 现在支持 Vulkan，只要用户从高级 grub 菜单中选择 Vulkan，或者在 grub 命令行中手动添加“VULKAN=1”。由于 Vulkan 支持，睡眠状态现在也部分工作- CPU 在模拟睡眠状态期间仍然活跃，但活动将下降到几乎没有。如果电源菜单中没有显示，您可能还需要使用第三方工具来触发睡眠状态。

Bliss OS 仍然有一些问题。例如， [Taskbar 是获得桌面体验的一个流行推荐](https://docs.blissroms.com/Bliss%20OS/extras/)，但是当使用 Taskbar 时，navbar 问题持续存在，所以用户需要确保他们在 Blissify 应用程序中设置了一个后退手势方法。默认情况下，睡眠状态在非 Vulkan 和 IA_Hardware-Composer 版本上无法正常工作，在这些情况下，systemUI 可能会重新启动。电源按钮在某些硬件上也可能不起作用。

请注意，Bliss OS 旨在供有经验的用户使用，因为他们的构建仍然被视为开发构建。安装它需要下载 ISO 文件，使用 Rufus 将其刻录到 USB 驱动器上，并禁用与启动安全性相关的选项，然后通过 USB 驱动器启动。你可以在实时模式下运行操作系统进行测试，如果你对结果满意，你可以通过 USB 驱动器安装它。更多详细说明和其他细节，请关注论坛主题。

**[极乐 OS - Android 9 派 PC - XDA 线程](https://forum.xda-developers.com/bliss-roms/bliss-roms-development/bliss-os-pie-beta-preview-t3855917/post80172193#post80172193)**