# 新的 Android Oreo 开发者命令创建虚拟 SD 卡进行测试

> 原文：<https://www.xda-developers.com/virtual-sd-card-android-oreo/>

# 新的 Android Oreo 开发者命令创建虚拟 SD 卡进行测试

Android Oreo 有一个开发者命令来启用虚拟 SD 卡，以防您在开发设备上测试应用程序时需要它。

学分:Dotmana

Android Oreo 正在成为我们最喜爱的移动操作系统的开发者和爱好者友好的迭代。我们已经发现了[为主题化设备添加的新命令(这导致了非根底层支持)](https://www.xda-developers.com/android-oreo-rootless-system-theme/)和[编辑电池保护程序](https://www.xda-developers.com/customize-battery-saver-mode-android-8-0/)，而且发现还不止于此。现在，我们发现了一个命令，允许开发人员测试他们的应用程序如何在带有物理 SD 卡的设备上工作，而不需要这样的设备！这很有用，因为有很多原因，例如确保应用程序可以在 SD 卡的较慢速度下运行，或者查看当其数据移动到 SD 卡时会发生什么。这种增加是必要的，因为许多旗舰手机(用于开发)没有 SD 卡插槽。

* * *

## 在 Android Oreo 上启用虚拟 SD 卡

Android Oreo 的 AOSP 源代码上的 commit 声明创建一个 512 兆字节的文件，并将其挂载为虚拟磁盘，供系统用作 SD 卡。该命令通过 adb 访问。如果你还没有建立亚行，首先[按照这个教程](https://www.xda-developers.com/install-adb-windows-macos-linux/)。

一旦 adb 启动并运行，您需要的命令如下。注意，该命令接受“真”或“假”，因为它是一个布尔值。

```
 adb shell 
```

```
 sm set-virtual-disk true/false 
```

然后，您的设备将创建并安装一个大小为 512 兆的虚拟 SD 卡。此虚拟 SD 卡不是为正常操作而设计的，因此不要在其中存储文件。虚拟磁盘严格用于应用程序开发人员的测试目的，用于测试他们的应用程序在真实 SD 卡分区上的运行情况。如果您是一名开发人员，其唯一的测试设备是 Google Nexus 或 Pixel 设备(这两种设备都无法访问 SD 卡插槽)，那么您可能会发现这个命令很有用。