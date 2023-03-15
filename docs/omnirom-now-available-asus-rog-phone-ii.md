# 为华硕 ROG 手机 II 发布基于 Android 10 的 OmniROM

> 原文：<https://www.xda-developers.com/omnirom-now-available-asus-rog-phone-ii/>

华硕 ROG Phone II 是 2019 年最强大的智能手机之一，提供了 T2 最强大的硬件和独特的游戏设计，在竞争中脱颖而出。除了游戏吸引力之外，这款手机还在定制 rom 社区中产生了极大的兴趣，华硕在[宣传售后市场开发工作](https://www.xda-developers.com/asus-sending-rog-phone-ii-custom-rom-kernel-developers/)中发挥了重要作用。虽然 ROG 的电话 3 已经过时，但 ROG 的电话 2 仍然设法保住了自己的位置。

**[华硕 ROG 手机 II XDA 论坛](https://forum.xda-developers.com/rog-phone-2)**

这款设备得到了 TWRP 和 LineageOS 的官方支持，并且不缺少新的定制 rom 和内核供用户试用。现在，ROG Phone II 用户又多了一个定制 ROM 可以玩了:OmniROM。

由于 XDA 资深成员 micky387 的努力工作，基于 Android 10 的 OmniROM 的第一个官方版本现已为华硕 ROG Phone II 推出。ROM 在日常使用中看起来相当稳定，官方帖子没有提到这个初始版本中的任何关键或已知问题。

要在你的华硕 ROG 手机 II 上安装 OmniROM，请确保你在两个插槽上都运行最新的固件，并且有一个解锁的引导程序。剩下的过程非常简单:你必须进入引导程序模式，从你的电脑上运行 *fastboot boot twrp.img* 命令(按照[这个指南](https://www.xda-developers.com/adb-fastboot-any-directory-windows-linux/)设置 fastboot 和 ADB)来临时引导到 twrp。从那里，闪存 rom 包，擦除用户数据，闪存 Gapps，并重新启动。开发者特别推荐闪 [OpenGApps](https://www.xda-developers.com/open-gapps-android-10-roms/) 的 Nano 包，不要尝试其他任何包。至于 Magisk，可以用[最后一个稳定的 Magisk 版本](https://www.xda-developers.com/magisk-v204-released-script-consistency-changes-bug-fixes/)。

要下载 ROM zip、GApps 包，并获得详细的闪存说明，请访问下面的链接。

**[下载官方 OmniROM](https://forum.xda-developers.com/rog-phone-2/development/rom-omnirom-rog-ii-t4175985)**