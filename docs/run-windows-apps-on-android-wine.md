# Wine 是 Windows 程序的兼容层，现在可用于 Android

> 原文：<https://www.xda-developers.com/run-windows-apps-on-android-wine/>

有没有希望在你的 Android 设备上运行成熟的 Windows 应用程序？现在你可以了...算是吧。Wine 是一个用于类 Unix 操作系统的 Windows 兼容层，已经更新到 3.0 版本，现在可以安装在 Android 设备上。

根据发布说明，Wine 3.0 为 Android 实现了一个完整的图形和音频驱动程序，可以作为一个 APK 包来构建，就像一个常规的 Android 应用程序一样。它还支持 OpenGL，尽管它仅限于 Android 上可用的 OpenGL ES API。

不过，它不能在任何安卓设备上运行你的标准 Windows 应用程序。Wine 不是一个模拟器，这意味着你需要一个 x86 Android 平板电脑、智能手机或 Chromebook 来充分利用它。不幸的是，虽然越来越多的 Chromebooks 支持 ARC，但采用 x86 芯片组的 Android 设备并不多。

对于我们大多数拥有基于 ARM 的 SoC 的 Android 设备的人来说，还有一线希望。用于 ARM 设备的 Wine 确实存在，但只有移植到 Windows RT(微软用于 ARM 架构的 32 位操作系统)的 Windows 程序才能运行。在我们自己的 [XDA 论坛](https://forum.xda-developers.com/showthread.php?t=2092348)上，有一个已经被重新编译以在 Windows RT 上运行的桌面应用程序列表，包括 Notepad++和 7-Zip 等流行工具，Python 2.7.3 和 Lua 等脚本语言和运行时，甚至是 Quake 等游戏。

在未来，Wine 将使用 QEMU，一种通过动态二进制翻译虚拟化处理器的开源虚拟机管理程序，在 ARM 上模拟 x86 指令。这将允许原生 x86 Windows 应用在 ARM 设备上运行，无需重新编译，但这项工作尚未完成。

让 Wine 在 Android 上运行非常简单。前往[下载页面](https://dl.winehq.org/wine-builds/android/)并获取两个 apk 中的一个:**“wine-3.0-arm”**如果你的设备有 ARM 芯片，或者**“wine-3.0-x86”**如果它有 x86 芯片。安装并启动应用程序后，您将看到 Windows 7 界面，左下角有完整的开始菜单。

然而，Wine 3.0 并非没有漏洞。由于 Android windows 管理 API 中的限制，图形驱动程序仅支持全屏桌面模式。它现在在软件键盘上也有问题——当你点击空白文本字段和命令提示符时，它们不能被识别和调用。一些用户也报告了谷歌 Pixel 等手机的崩溃。

不考虑这些早期的问题，葡萄酒团队所取得的成就当然令人印象深刻。Codeweavers 在 2016 年发布了 Android 和 Chrome OS 的 [CrossOver](https://www.xda-developers.com/run-windows-apps-chromeos-codeweavers-crossover/) (其专有版本 Wine)的技术预览版，贡献了许多使 Android 移植成为可能的底层代码。

开发团队表示，Wine 3.0 包含超过 6000 项更改，标志着新的年度发布周期的开始。除了 Android 支持之外，它还增加了 Direct3D 命令流，改进了 DirectWrite 和 Direct2D 支持，以及 Direct3D 10 和 11。