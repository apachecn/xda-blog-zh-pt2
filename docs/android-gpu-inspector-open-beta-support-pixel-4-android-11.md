# Android GPU Inspector 现在处于开放测试阶段，支持 Android 11 上的 Pixel 4

> 原文：<https://www.xda-developers.com/android-gpu-inspector-open-beta-support-pixel-4-android-11/>

在今年早些时候的谷歌游戏开发者峰会上，谷歌[首次展示了](https://www.xda-developers.com/google-for-games-new-developer-tools-play-firebase-android-studio/)一款名为 Android GPU Inspector 的新 Android 工作室工具。该工具旨在帮助图形工程师通过访问渲染阶段和 GPU 计数器来优化游戏的帧速率和支持的 GPU 的功耗。当时，该工具只在少数游戏工作室的有限开发者预览版中提供给[，他们已经开始在 Pixel 4、Pixel 4 XL、Galaxy Note 10 和 Galaxy S10 上测试它。现在，Android GPU Inspector 面向所有游戏开发者开放测试。](https://developer.android.com/games/preview)

在 Android 开发者博客的最近一篇文章中，谷歌宣布了其运行 Android 11 的 Pixel 4 设备的 Android GPU Inspector 公开测试版。有兴趣试用该工具优化游戏的游戏开发者可以在这里下载 Android GPU Inspector [，然后按照](https://gpuinspector.dev/)[这篇文章](https://gpuinspector.dev/docs/getting-started)中提供的设置说明进行操作。由于 Android GPU Inspector 依赖更新的固件和视频驱动程序来获取所需的信息，因此它目前仅适用于运行 Android 11 的 Pixel 4 和 Pixel 4 XL。然而，谷歌正在与设备制造商和 SoC 供应商合作，以支持更多设备。

谷歌指出，量化使用 Android GPU Inspector 优化游戏所带来的性能优势:

AGI 与暴雪娱乐公司和网易公司合作，帮助即将推出的暗黑不朽游戏节省了 45%的顶点带宽，这是一款黑暗哥特式动作 RPG 游戏...在与金的合作中，AGI 帮助将 GPU 的帧时间从 11-16 毫秒提高到稳定的 8 毫秒，用于即将到来的崩溃 Bandicoot: On the Run！，使游戏减少电池消耗，运行速度更快，体验更流畅...在与 Jam City 的合作中，AGI 帮助将《世界大战 Doh:实时 PvP》的 GPU 帧时间减少了 45%。”

对于不知道，Android GPU 检查员是由谷歌与高通合作设计的。该工具支持当今 Android 设备中的大多数 GPU，包括高通骁龙 SOC 中的 Adreno GPUs。由于合作关系，Android GPU Inspector 允许开发人员直接与高通分享反馈，并帮助该公司优化 Adreno GPU 软件驱动程序。高通还将让一些开发人员获得测试版驱动程序，以便他们可以快速测试他们的优化，之后将通过谷歌 Play 商店为特定设备发布最终驱动程序。考虑到 ARM 的下一代 Mali GPUs 也将[通过谷歌 Play 商店](https://www.xda-developers.com/arms-next-mali-gpu-updateable-drivers-google-play-store/)支持可更新的驱动程序，该工具也可以使采用联发科、海思麒麟和 Exynos 芯片组的设备受益。