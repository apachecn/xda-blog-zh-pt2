# 使用简单的恢复切换器轻松恢复库存

> 原文：<https://www.xda-developers.com/simple-recovery-switcher/>

# 使用简单的恢复切换器轻松恢复库存

使用简单的恢复切换器在自定义和库存恢复分区之间切换。厌倦了玩弄复苏？简单的恢复切换器为您做到这一点。

作为 OTA 包发布的 Android 更新非常容易应用，但也让定制 ROM 爱好者非常头疼。每次 OTA 出来，我们都需要回到股票恢复，刷新更新，然后刷新我们最喜欢的定制恢复，如 TWRP 或 ClockworkMod，以恢复我们所有的恢复功能，如 Nandroid 备份和刷新 SuperSU 的能力。我甚至不用开始解释这个过程是多么的耗时和令人沮丧。

如果你的设备经常获得这些更新，你可能会有兴趣测试一个由 XDA 论坛版主和公认的开发者 [graffixnyc](http://forum.xda-developers.com/member.php?u=3537886) 创建的工具。简单的恢复切换器，顾名思义，轻松切换股票和自定义恢复。整个过程可以很快完成，这比使用标准 USB 电缆和快速启动方法要快得多。

该应用程序应该可以在每一个使用*/dev/block/platform/MSM _ sdcc . 1/by-name/recovery*结构并以安装的 Busybox 为根的高通设备上正常工作。恢复必须命名为 stock.img 和 custom.img，并且必须放在内部 SD 卡的根文件夹中。在使用此工具之前，请仔细检查一切，因为扰乱恢复可能会导致设备阻塞。

Android L 或柠檬蛋白派正在路上，所以在不久的将来(或不太近的将来)可能会有一些 OTA 更新。通过访问[简单恢复切换器应用线程](http://forum.xda-developers.com/android/apps-games/app-simple-recovery-switcher-t2857554)，为 OTA 做好准备。