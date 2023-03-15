# OPPO 寻找 X2 和寻找 X2 专业与骁龙 865 接收 GPU 驱动程序更新

> 原文：<https://www.xda-developers.com/oppo-find-x2-and-find-x2-pro-with-snapdragon-865-receive-gpu-driver-update/>

# OPPO 寻找 X2 和寻找 X2 专业与骁龙 865 接收 GPU 驱动程序更新

继小米之后，OPPO 发布了高通骁龙 865 驱动的 OPPO Find X2 和 Find X2 Pro 上 Adreno 650 GPU 的 GPU 驱动程序更新。

将操作系统的内部组件模块化是一项艰巨的任务，但结果是未来的软件更新变得更容易执行。Project Treble 是 Android 生态系统中这种努力的完美例子。当谷歌[正在探索不同的方式](https://www.xda-developers.com/android-q-apex-biggest-thing-since-project-treble/)来减少操作系统和内核的碎片化时，芯片制造商自己也在与原始设备制造商合作[将低级驱动程序与 Android 操作系统本身](https://www.xda-developers.com/arms-next-mali-gpu-updateable-drivers-google-play-store/)分离，并减少更新碎片化。少数当代高通 SOC 支持可更新的 GPU 驱动程序，这些驱动程序可以像独立的驱动程序更新一样安装在 PC 上。小米已经采用了该设计，[在其中国应用商店上发布了一款“GPU 驱动程序更新程序”应用](https://www.xda-developers.com/xiaomi-adreno-gpu-driver-update-snapdragon-865/)，该应用兼容骁龙 865 驱动的 [Mi 10](https://forum.xda-developers.com/xiaomi-mi-10) 、 [Mi 10 Pro](https://forum.xda-developers.com/xiaomi-mi-10-pro) 和 [Redmi K30 Pro](https://www.xda-developers.com/tag/redmi-k30pro/) 。跟随小米的脚步，OPPO 现在已经为 OPPO Find X2 和 Find X2 Pro 发布了类似的 Adreno 650 GPU 驱动程序更新程序。

**[OPPO 找 X2 XDA 论坛](https://forum.xda-developers.com/oppo-find-x2) ||| [OPPO 找 X2 亲 XDA 论坛](https://forum.xda-developers.com/find-x2-pro)**

就像小米一样，OPPO 的驱动更新程序(标签为“ [OplusGpudriver](https://forum.xda-developers.com/showpost.php?p=83131633) ”)截至目前只在国内提供下载。app 的包名是`com.oplus.gpudrivers.sm8250.api29`，最新 build 的版本号是 0.0474.0。著名的 Android 开发者[艾萨克·陈](https://github.com/TingyiChen)，在我们的论坛上被称为 XDA 资深会员[丁一辰](https://forum.xda-developers.com/member.php?u=7500669)，设法得到了 APK 的文件，其中包含一堆来自高通的 GPU 驱动程序以及 OpenGL ES 和 Vulkan 相关的库。

虽然 APK 文件也可以手动加载到 OPPO Find X2/X2 Pro 的国际版本上，但我们论坛上的用户报告说 [OpenGL 版本没有增加](https://forum.xda-developers.com/showpost.php?p=83150079&postcount=33)。因此，似乎图形驱动程序只能在“寻找 X2”系列的 ColorOS 中文版上更新。

将 GPU 驱动从基础 OS 上解耦无疑是向 Android 完全模块化迈进的一大步。令人兴奋的是，越来越多的 OEM 厂商正在利用新的驱动程序更新模式，尽管除了 GPU 之外，它还没有获得对不同硬件元素的支持。