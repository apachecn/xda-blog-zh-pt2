# Android 模拟器支持 ARM ABIs 的 Android 11 x86 系统镜像

> 原文：<https://www.xda-developers.com/android-11-x86-system-images-android-emulator-arm-abis/>

# Android 模拟器支持 ARM ABIs 的 Android 11 x86 系统镜像

面向 x86 硬件的 Android 11 系统映像现在支持在面向 x86 PCs 的 Android Studio 中的 Android 仿真器上进行 ARM 仿真。

谷歌在本月早些时候发布了 Android 11 开发者预览版 2。在这个版本中，谷歌做了一个关键的改变，在 [Android Studio](https://www.xda-developers.com/android-studio-3-6-stable-release/) 中的 Android 模拟器上实现了更高效的应用程序调试。面向 x86 CPUs 的 Android 11 系统映像现在允许具有 C 或 C++依赖性的应用程序更流畅地运行，而无需完整的 ARM 仿真，并利用 x86 硬件的硬件加速和 CPU 虚拟化。

用本机代码(即 C 或 C++)编写的 Android 应用程序必须考虑不同的 CPU 架构进行编译。必须有针对不同 CPU 架构的不同版本的应用程序，如 ARM、ARM64、x86 或 x86-64。这是因为本机代码直接编译成特定架构的机器指令，而不是在 Android 运行时(ART)上执行的 Kotlin 或 Java 应用程序。

为了通过在基于 x86 的计算机上运行的 Android 模拟器测试您的应用程序，您需要不同版本的 x86 CPU。该应用的 x86 版本无法在智能手机上运行，因为智能手机通常基于 ARM 或 ARM64 CPUs。到目前为止，这个问题的唯一解决方案是要么使用物理 Android 设备，要么为 x86 CPUs 安装带有完整 ARM 仿真的仿真器映像。后一种选择是性能密集型的，不能充分利用 x86 CPUs 提供的硬件加速和 CPU 虚拟化。

为了解决这个问题，谷歌现在发布了兼容 ARM 的新 Android 11 x86 系统映像。这些系统映像利用 ABI(应用程序二进制接口),在用不同语言编写的应用程序之间或应用程序和操作系统之间充当中介。ARM 二进制文件中的 ARM 指令被专门翻译成 x86，而其余代码继续在 x86 中执行。由于 ARM 二进制文件的这种隔离，该过程对性能的要求较低，甚至可以在低级硬件上运行。

除了使用 C++依赖关系更容易调试 Android 应用程序之外，它还允许开发人员在未来发布他们的应用程序的 ARM 版本以及 ABIs，而不是 Chromebooks 的 x86 版本。这将刺激各种 Chromebooks 支持更多针对 Android 11 的应用程序。

使用 [Android 虚拟设备管理器](https://developer.android.com/studio/run/managing-avds#createavd)或 SDK 管理器，可以在 [Android Studio](https://developer.android.com/studio) 中下载新的兼容 x86 的 Android 11 系统映像。