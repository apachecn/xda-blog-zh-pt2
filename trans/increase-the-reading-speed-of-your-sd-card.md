# 提高 SD 卡的读取速度

> 原文：<https://www.xda-developers.com/increase-the-reading-speed-of-your-sd-card/>

SD 卡读取速度因您选择的 SD 卡类别而异。然而，当比较我们的电脑和 Android 设备的阅读速度时，许多人都感到失望。XDA 论坛成员 [brainmaster](http://forum.xda-developers.com/member.php?u=377757) 声明，如果你有一个快速 10 级 SD 卡也没关系——它都在缓存中。

在 Android 设备上读取 SD 卡的缓存大小被设置为 128KB，在一些 rom 上甚至设置为 4KB！

要亲自检查，您需要导航到/sys/devices/virtual/BDI/179:0/read _ ahead _ kb。这可以手动更改，但不会在重新启动时保留。为了使更改持久化，需要在启动时通过 init.d 加载脚本。或者，XDA 成员提供了 CWM.zip 文件以使事情变得更容易。

要找出 SD 卡的最佳缓存大小和改变它的最佳方法，请访问[修改线程](http://forum.xda-developers.com/showthread.php?t=1010807)。