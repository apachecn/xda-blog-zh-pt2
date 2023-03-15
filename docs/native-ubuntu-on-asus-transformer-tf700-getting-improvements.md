# 华硕 Transformer TF700 上的原生 Ubuntu 获得改进

> 原文：<https://www.xda-developers.com/native-ubuntu-on-asus-transformer-tf700-getting-improvements/>

谈到在 Android 设备上运行 Linux，最简单的方法是使用 [chroot](http://www.xda-developers.com/android/htc-desire-users-can-test-an-app-that-installs-ubuntu/) 。它基本上允许用户在 Android 之上的虚拟盒子中运行 Linux。然而，一些开发者已经开始尝试完全取代 Android。华硕变压器 TF 700[在这方面已经取得了长足的进步。](http://forum.xda-developers.com/forumdisplay.php?f=1661)

XDA 论坛成员 rabits 一直致力于在 TF700 上运行 Ubuntu。也不是 chroot，而是真货。它目前发布版本为 0.6.2，安装它的用户将获得 Ubuntu 12.10。以下是一些特色亮点:

> 使用 Android CleanRom 2.7.2 双启动- Initrd 现在支持使用 wifi 双启动 linux(从任何 sd 卡或 usb 设备)和 Android。
> 
> 测试 Linux 引导 AndroidRoot 引导加载程序的临时引导映像。重新启动后，你得到你的机器人回来。
> 
> 图形引导-你可以通过 ubuntu 用户在图形模式下登录。
> 
> 键盘重新映射-特殊键被 evdev keymap 替换为默认值(Esc、F1-12、Ins、Print、Break、Del、Home->Alt、Search->Meta4)。
> 
> 触摸板双指滚动-上下移动双指进行滚动。两指轻敲-是鼠标的第三个按钮。
> 
> WiFi -你可以通过 WiFi 连接互联网或局域网
> 
> OpenGL ES - 3D 和游戏(eduke32，Jagged Alliance 2)以及 Chromium 的良好浏览
> 
> 高达 1080p 的音频和视频-使用 nvgstplayer 对全高清视频进行硬件解码
> 
> nvgstplayer - sas="audioconvert！pulsesink" -i -全屏模式
> 
> nvgstplayer-SVS = " nvxvimagesink "-SAS = " audio convert！pulsesink" -i 窗口模式

为了帮助用户了解开发进度，rabits 列出了一个工作列表，列出了已经实现的内容和仍需改进的内容。大概完成了一半，用户可以没有太大难度的获得真正的 Linux 体验。当然也有一些问题，比如 Unity 有问题，还有一些驱动的问题。

要了解更多信息并关注发展，请查看[发展主题](http://forum.xda-developers.com/showthread.php?t=2026919)或[讨论主题](http://forum.xda-developers.com/showthread.php?t=2014759)。