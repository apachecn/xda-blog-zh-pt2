# Xposed Installer v3.15 和 Xposed Framework v90-beta2 发布了 Android Oreo 修复和优化

> 原文：<https://www.xda-developers.com/xposed-installer-v3-15-android-oreo-fixes/>

# Xposed Installer v3.15 和 Xposed Framework v90-beta2 发布了 Android Oreo 修复和优化

本月早些时候，我们看到了为 Android 8.0 和 Android 8.1 Oreo 发布的 Xposed Framework 的第一个测试版，今天 rovo89 宣布了 Xposed Installer v3.15 和 Xposed Framework v90-beta2，修复了一些测试版错误。

让 Xposed 框架在 Android Nougat 上工作可能需要 XDA 资深公认开发人员 [rovo89](https://forum.xda-developers.com/member.php?u=4419114) 一段时间，但 Android Oreo 不是这种情况。在 Xposed 为 Nougat 发布三个月后，【Android 8.0 和 Android 8.1 Oreo 的首个测试版框架发布。今天，Xposed 安装程序——x posed 框架的前端安装和管理工具——已经更新到 3.15 版本。

正如我们所看到的，几乎每一个测试版都有一些工作要做，这个 Android Oreo 的 Xposed 框架的初始版本也不例外。随着 Xposed Installer 升级到 3.15，我们有了一些小的变化和一些更重要的变化。以下是完整的[变更日志](https://forum.xda-developers.com/showthread.php?p=75248580#post75248580):

## 已发布的安装程序 3.15 版更改日志

*   修正了奥利奥下载列表搜索的崩溃。
*   修正了在奥利奥上发送日志时的崩溃。
*   “立即优化应用程序”菜单项，将触发`cmd package bg-dexopt-job`。它从奥利奥开始提供，如果设备正在充电，它将开始通常每晚运行一次的工作。如果你在安装 Xposed 后感觉到性能下降，可能是因为所有的应用程序都纯粹运行在 JIT 和解释器上。这是因为 Xposed 需要额外的信息来标识它必须使之无效的方法，这些信息将在下一次编译时确定。如果您希望现在就实现，请使用这个新功能。我的像素花了大约 20 分钟。更多背景信息，请看[这里](https://source.android.com/devices/tech/dalvik/jit-compiler)。
*   检测[验证的引导](https://source.android.com/security/verifiedboot/) (dm-verity)是否激活。如果是，对系统分区的任何更改都将被检测到，您将进入引导循环。检测可能还不是 100%完美，所以如果你注意到误报或漏报，请[报告一个错误](https://github.com/rovo89/XposedInstaller/issues)和`adb shell getprop`的输出。

## 暴露的框架 v90-beta2

rovo89 还发布了 **v90-beta2** 和**卸载程序 20180117** ，你可以通过 Xposed 安装程序和[x posed 网站](http://dl-xda.xposed.info/framework/)找到这些。这些支持通过 TWRP 在 Google Pixel 和其他“系统根映像”设备上安装(卸载)Xposed，rovo89 将这些设备描述为系统分区作为根目录安装的设备，而/system 实际上只是一个子目录。最后，以前的卸载程序有一个打字错误，这可能会导致所有设备的引导循环，所以一定要始终使用最新的卸载程序！