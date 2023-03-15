# 谷歌为最新的 Android Studio 更新带来快速启动

> 原文：<https://www.xda-developers.com/google-quick-boot-android-studio/>

# 谷歌为最新的 Android Studio 更新带来快速启动

谷歌在 Android Studio 的最新稳定版本中引入了快速启动，这是 Android Emulator 的一个新的保存状态功能。

Android Studio 在金丝雀频道的最新分支 3.x 版本是 edge。自从几个月前首次亮相以来，Google 一直致力于改善集成开发环境(IDE)的用户体验。Android Studio 3.0 引入了一个名为快速启动的新功能，今天，谷歌将其带入稳定版本。

快速启动的目标是使恢复 Android 模拟器会话更快更容易。第一次在 Android 模拟器中启动 Android 虚拟设备(AVD)时，它会经历所谓的“冷启动”以前，随后的启动没有什么不同，但具有快速启动的 Android Studio 版本在关机时保存系统状态，并在重新打开模拟器时恢复它。(据谷歌称，它可以在不到 6 秒的时间内恢复会话。)

谷歌的人能够通过完全重新设计遗留仿真器快照架构来实现这一点，以便它可以与虚拟传感器和 GPU 加速一起工作。快速启动不需要额外的设置——它在 Android 模拟器 v27.0.2 中是默认启用的。

快速启动并不是 Android Studio 稳定分支的唯一新特性。Android 兼容性测试套件(CTS)集成正在进行中，内存管理器可以按需分配系统内存，新的 Android 系统映像包括 Play Store 应用程序。

如果你没有下载 Android Studio 的 canary 版本，也没有机会体验 Quick Boot，那就点击源代码链接开始吧。

* * *

[**来源:安卓开发者博客**](https://android-developers.googleblog.com/2017/12/quick-boot-top-features-in-android.html)