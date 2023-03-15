# 没有 Root 如何自定义 Android Oreo 中的导航栏

> 原文：<https://www.xda-developers.com/customise-the-navigation-bar-android-oreo/>

Android Oreo 刚刚发布了 T1，随之而来的是一系列新功能、优化和新外观。随着改进而来的是新的 API，因此通过一些修补我们可以获得更多非官方的好东西。[你现在可以安装系统镜像了](https://www.xda-developers.com/android-oreo-download-pixel-nexus/)，而且你可以自定义导航栏，就像你在开发者预览版上做的那样！导航栏修改[甚至存在于 Android Nougat](https://www.xda-developers.com/nav-bar-customization-was-hidden-in-stock-nougat-all-along-and-it-never-needed-root/) 中，隐藏在众目睽睽之下，但在最初的两个 Android O 开发者预览版中用户可以访问一段时间，但它被删除[和其他调谐器](https://android.googlesource.com/platform/frameworks/base/+/2ad83b94d6d4c11af2e0ab5788b2df90a1c87020%5E%21/#F0)，提交消息称“他们还没有完全到位”。

令人欣慰的是，仍然可以像在开发者预览版中一样编辑导航栏(以及以后的 Nougat)！只有面向用户的菜单选项被删除，但如果你知道如何通过 adb 调用它(或者可以忍受使用第三方应用程序)，它实际上仍然完全可用。

本教程是针对安卓奥利奥用户的，然而这个方法和应用程序**也适用于安卓牛轧糖**。Android Oreo 目前仅在谷歌 Pixel、Pixel XL、Pixel C、Nexus 6P、Nexus 5X 和 Nexus Player 上可用。

* * *

## 自定义 Android Oreo 中的导航栏

我们建议您从谷歌 Play 商店安装自定义导航栏调谐器，因为它为从开发者预览版中删除的导航栏自定义调谐器提供了一个漂亮的 GUI 前端(并提供了更多的启动功能)。如果你没有 root 权限，你需要下载 [Minimal ADB & Fastboot](https://forum.xda-developers.com/showthread.php?t=2317790) 或者[官方 Google 二进制文件](https://www.xda-developers.com/google-releases-separate-adb-and-fastboot-binary-downloads/)来启用应用程序所需的 WRITE_SECURE_SETTINGS 权限。

要做到这一点，你需要首先通过进入开发者选项菜单来启用 USB 调试。如果您没有看到开发者选项，向下滚动到“关于”并轻按“内部版本号”七次，直到出现“您现在是开发者”提示。“关于”上面是“开发者选项”菜单。输入此项并启用 USB 调试。启动 adb 从你的电脑按下 shift +右键在同一个文件夹中包含您的 adb 文件，然后选择“打开命令提示符在这里”(如果你是在 Windows 上)。对于 Mac 和 Linux 用户，您需要打开终端，然后打开 cd 到您下载文件的目录。按照应用程序中的说明授予适当的权限。

## 重新排列导航按钮

如果您喜欢不同的顺序，可以重新排列导航按钮。只需进入名为“导航栏”的菜单，并输入实验性的调整。

## 其他用途

有很多你可以做的这个应用程序和 Tasker 的使用！这里有两个例子:

该应用程序允许完全 Tasker 集成，所以你可以用任何你喜欢的方式编程。尝试自定义你的导航条，让我们知道你能想出什么样的用途！