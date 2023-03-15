# Magic ToolFlash 可让您直接从 Android 设备中刷新 ZIP 包

> 原文：<https://www.xda-developers.com/magic-toolflash-magisk-module/>

当大多数人安装 [Magisk 模块](https://www.xda-developers.com/best-magisk-modules/)时，他们只是通过 Magisk 应用程序刷新它，然后重新启动进入 Android。说到安装常规的 flash ZIP 包，有像 TWRP 这样的定制恢复项目可以完成这项工作。然而，如果你打算开发和修补你的设备，你应该习惯命令行界面。除了知道一些 shell 命令很有用这一显而易见的事实之外，学习使用它们可能意味着除非绝对必要，否则不必通过另一个应用程序刷新或者将智能手机连接到 PC 进行侧加载。这就是**神奇工具 Flash** 项目的用武之地。

由 XDA 资深会员 [huskydg](https://forum.xda-developers.com/m/huskydg.11455139/) 创建的 Magic ToolFlash 是对 Android 闪烁机制的独特采用。这是一个命令行闪存工具，不需要定制的恢复环境。你所需要做的就是在你的设备上下载一个可闪存的压缩文件。接下来，通过任何具有 root 权限的终端仿真器 app 调用该工具，执行刷机操作。

除了为安全起见创建一个隔离的命名空间，Magic ToolFlash 还向最终用户显示详细的 Flash 日志。安装 Magisk 模块后，您可以使用`flash`命令从手机的 CLI 窗口刷新不同的 Magisk 模块、Magisk 应用程序本身以及其他 mod ZIP 文件。然而，该工具还不能用于从运行的 Android 系统安装 ROM。

请记住，`/tmp`目录不存在于 Android 根文件系统中。因此，在使用 Magic ToolFlash 时，您可能需要修改更新程序脚本并使用`/dev/tmp`作为临时目录。此外，如果目标 flashable zip 包含硬编码的`/sbin`命令，它可能会在 Android 11 及以上操作系统上失败。

如果你是一名开发人员，并且想探索 Magic ToolFlash 的代码库，那么看看该项目的 GitHub 库。在 repo 的*版本*部分，还可以下载一个现成的 Magisk 模块版本。

**魔法工具 Flash: [下载](https://github.com/Magisk-Modules-Alt-Repo/magic-flash/releases) || [GitHub 资源库](https://github.com/Magisk-Modules-Alt-Repo/magic-flash)**