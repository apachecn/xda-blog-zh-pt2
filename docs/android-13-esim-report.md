# Android 13 可能支持多个 eSIMs，即使手机不是为它而建的

> 原文：<https://www.xda-developers.com/android-13-esim-report/>

# Android 13 可能支持多个 eSIMs，即使手机不是为它而建的

根据 Android 13 中的代码，谷歌正在研究一种方法，将一个 eSIM 模块用于多个 eSIM。

手机传统上使用称为 SIM 卡的物理卡连接到蜂窝网络，但在转换到称为 eSIM 的数字版本方面进展缓慢。我们没有看到更多手机完全放弃 SIM 卡插槽的原因之一是，Android 对多 e SIM 没有很好的支持，这需要在大多数制造商进行转换之前发生。即将到来的 [Android 13](https://www.xda-developers.com/android-13/) 更新似乎正是为此奠定了基础。

*斯珀*报道称，Android 13 的代码库包含了[的实现，这是谷歌在 2020 年](https://uspto.report/patent/grant/10,708,761)申请的专利，允许在一个嵌入式芯片上使用多个 SIM 卡配置文件。其工作原理是将调制解调器和 eSIM 芯片之间的单个物理数据总线分成多个逻辑接口，这些接口在单个物理接口上多路复用。这有点像大多数现代 CPU 如何将物理 CPU 核心分成逻辑 CPU 核心，因此可以同时执行更多的任务。

与需要在手机或平板电脑侧面安装大型插槽的物理 SIM 卡不同，eSIM 只需要在设备主板上安装一个小型组件。这为更大的电池、相机硬件或其他任何东西在手机中留下了更多空间。然而，还没有多少手机完全放弃了物理 SIM 卡插槽——部分原因是许多运营商仍然不支持 eSIM，部分原因是许多国际销售的设备需要有两个某种 SIM 卡。两个 eSIMs 是一个选项，[这是 iPhone 13 系列提供的](https://www.macrumors.com/2021/09/14/iphone-13-models-support-dual-esims/)，但这增加了更多的复杂性。

谷歌还没有公开提到这项功能，但如果它在最终版本中留在 Android 13 中，我们很可能很快就会听到更多关于它的消息。只要运营商能够相信，新功能可以在手机上获得更广泛的 eSIM 支持。

**来源:** [斯珀](https://blog.esper.io/android-dessert-bites-19-esim-mep-android-13-9683475/)