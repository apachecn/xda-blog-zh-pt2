# 使用此应用程序控制华硕 ROG 手机 II 的 RGB 徽标[Root]

> 原文：<https://www.xda-developers.com/control-asus-rog-phone-ii-rgb-logo-custom-roms/>

# 这个应用程序使用根访问，让你控制华硕 ROG 手机二的 RGB 标志

正在寻找一种方法来定制华硕 ROG Phone II 上 RGB 徽标的照明模式？检查这个根应用程序！

华硕 ROG 手机 II 已经[有了今年的继任者](https://www.xda-developers.com/asus-rog-phone-3-gaming-smartphone-snapdragon-865-plus-144hz-display-6000mah-battery-launch/)，但 2019 年的游戏旗舰仍然有一些重要的影响。它的强大规格包括[高通骁龙 855+](https://www.xda-developers.com/qualcomm-snapdragon-855-plus/) 芯片组，高达 12GB 的内存，高达 1TB 的内部存储，6000 毫安时的巨型电池，以及流畅的 120 赫兹 AMOLED 显示屏。ROG Phone II 也有一个开发者友好的 OEM，这意味着你可以在这款智能手机上尝试[大量的 mod 和定制 rom](https://www.xda-developers.com/asus-rog-phone-ii-developments-google-camera-lineageos-17-1/)。不过，如果你运行的是定制 ROM，你可能会注意到 ROG Phone II 的“玩家国度”标志缺少 RGB 控件。令人欣慰的是，有一个新的应用程序在城里，你可以控制 RGB 照明，甚至当你运行一个定制的 ROM。

**[华硕 ROG 手机 II XDA 论坛](https://forum.xda-developers.com/rog-phone-2)**

XDA 初级会员 [Terminal_Heat_Sink](https://forum.xda-developers.com/member.php?u=10420213) 开发了这个应用程序，它不仅允许你在每个应用程序的基础上定制 ROG 标志的照明模式，还让你能够利用第二个 LED 进行通知。这款名为“华硕 ROG 手机 2 RGB”的应用程序在内部与 RGB 驱动程序挂钩，这就是为什么 root 访问是使用它的先决条件。据开发者称，该应用程序也可以在普通 ROM 上运行，但你必须升级到[官方 Android 10 固件](https://www.xda-developers.com/asus-rog-phone-ii-android-10-kernel-source-code-release/)，以确保完全兼容。

下面你可以找到该应用程序支持的自定义动画列表。请注意，色轮并不适用于所有颜色。

1.  没有人
2.  纯色
3.  呼吸一种颜色
4.  眨眼
5.  彩虹 1 号
6.  彩虹 2
7.  彩虹呼吸
8.  雷
9.  雷电彩虹
10.  快速闪烁两下
11.  快速闪烁两次彩虹
12.  呼吸彩虹 1
13.  呼吸彩虹 2
14.  缓慢的闪光彩虹
15.  黄灯

**华硕 ROG 手机二代 RGB: [下载](https://github.com/ArtiomSu/Asus-ROG-Phone-2-RGB/releases) ||| [源代码](https://github.com/ArtiomSu/Asus-ROG-Phone-2-RGB)| |[XDA 讨论线程](https://forum.xda-developers.com/rog-phone-2/themes/app-asus-rog-phone-2-rgb-t4124299)**

该应用程序的编码方式使您不必在每次重新安装时设置自定义通知的所有设置。有一个选项可以将所有设置导出到一个名为`.terminal_heat_sink.asusrogphone2rgb.xml`的文件中，您可以在内部存储器的根目录中找到该文件。要导入，只需将 XML 文件放在相同的位置，并使用应用程序中的“导入设置”向导。