# 以下是如何在 x86 PC 上启动 Android 12L 的方法

> 原文：<https://www.xda-developers.com/android-12l-x86-pc-bliss-os/>

由于 Android 的开源特性，人们可以根据自己的需求定制操作系统。例如，Bliss ROMs 的开发者为传统的 x86 平台维护了一个名为 Bliss OS 的 Android 版本。该项目现在已经达到了下一个里程碑，因为人们可以在虚拟机或 PC 上运行的第一个 Android 12L 测试版现在已经可供下载。

值得注意的是，已经有两个基于 Android 12 的 Bliss OS 15 的 alpha 版本，都是在去年 12 月发布的。虽然 Bliss OS 代码库是基于 Android 12L 之上的，但 Jon West，也就是 XDA 公认的贡献者 [electrikjesus](https://forum.xda-developers.com/m/electrikjesus.928479/) ，通过一个正在进行的 vanilla Android-x86 构建，分享了在 PC 上运行的 vanilla Android 12L 的第一瞥。现在，维护者认为 Android-x86 版本对于普通的 PC 配置来说已经足够成熟，因此第一个测试版已经推出。

除了 Android 12L 的常规创新，该版本还通过集成额外的驱动程序和 UI 增强功能来扩展与桌面硬件的兼容性。Android-x86 项目在历史上一直坚持使用接近库存 Android 的界面，但这次定制版本包括一个桌面模式启动器作为替代启动器，它应该更适合键盘和鼠标的使用。

安装工作流针对具有 GUID 分区表(GPT)文件系统的基于 UEFI 的环境进行了优化，但是超级用户也可以修改 GRUB 参数，并使其在传统平台上启动。没有必要[刷新一个单独的 GApps 包](https://www.xda-developers.com/download-google-apps-gapps/)，因为 Play Store 和其他谷歌服务已经预装在版本中。

以下是最初测试版的完整变更日志:

*   增加了智能坞站(桌面模式启动器)
*   已更新至 Linux 内核 5.10.70(带 kernel-SU)
*   更新到 Mesa 22.0.0(介子构建)
*   为图形选项添加了新的 grub 条目
*   增加了谷歌 Play 商店(GMS/gapp)
*   针对 arm 和 arm64 的 libndk 翻译修复
*   通过 libva 和 omx 更新媒体包以获得更广泛的支持

如果你有兴趣在你的电脑上试用 Android 12L 并了解更多关于该项目的信息，请前往 Bliss OS 的官方网站[。请记住，在 PC 上安装 Android 并不像在手机上闪存 ROM 那样简单，所以开发人员要求您在从那里下载 ISO 包之前通过一点测试。尽管如此，直接下载链接可以在下面找到，但请确保在动手之前做好研究并仔细阅读安装说明。](https://blissos.org/index.html)

**[从 Bliss OS 开发者](https://sourceforge.net/projects/blissos-dev/files/Android-Generic/PC/aosp/gapps/12L/)** 处下载 Android-x86 12L Beta 1

* * *

**来源:** [乔恩·韦斯特在推特上](https://twitter.com/electrikjesus/status/1504603431595646983)