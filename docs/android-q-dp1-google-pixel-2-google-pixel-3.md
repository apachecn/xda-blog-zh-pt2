# Android Q Beta 是为谷歌 Pixel、Pixel 2 和 Pixel 3 准备的

> 原文：<https://www.xda-developers.com/android-q-dp1-google-pixel-2-google-pixel-3/>

等待终于结束了——OTA 文件和工厂图像将在第一个公开的 Android Q 测试版中上线。如果你幸运地拥有谷歌 Pixel、谷歌 Pixel XL、谷歌 Pixel 2、谷歌 Pixel 2 XL、谷歌 Pixel 3 或谷歌 Pixel 3 XL(是的，所有三代 Pixel 都受到支持)，那么你现在就有机会测试下一个主要的 Android 版本，要么手动更新，要么注册测试版并通过无线方式接收更新。Android 10 Q 带来了许多新功能，包括全系统黑暗模式和权限管理的改进。第一个测试版将于今天发布，而最终版预计将于八月初登陆。

请记住，这第一次预览是针对开发人员的。在下一个 Android 版本面向公众发布之前的几个月，谷歌给了开发者机会，让他们对照新的 Android 平台 API 测试自己的应用。这第一个版本不会有所有你会联想到 Android Q 的新软件功能。谷歌可能会在 5 月 7 日开始的[谷歌 I/O 2019](https://www.xda-developers.com/google-io-2019-may-7-9/) 上推出一系列新功能。我们当然会广泛报道 Android Q，因为我们知道我们的读者已经迫不及待地想要得到一个官方版本或者一个定制的 ROM。不过，目前谷歌 Pixel 2 和谷歌 Pixel 3 用户可以比任何人都更早享受这一版本。

* * *

## 为 Pixel、Pixel XL、Pixel 2、Pixel 2 XL、Pixel 3 或 Pixel 3 XL 下载 Android Q Beta 1

可以[下载 OTA 镜像文件](https://developer.android.com/preview/download)直接从最新【2019 年 3 月发布的 Pixel 2、Pixel 2 XL、Pixel 3、Pixel 3 XL 的安全补丁更新。如果你有一个解锁的引导加载程序，并修改了引导镜像来安装 TWRP 或 Magisk，你需要刷新出厂镜像文件。在下一节中可以找到如何操作的一般说明。

如果你有兴趣讨论 Android Q 版本，一定要加入 Pixel、Pixel 2 和 Pixel 3 设备的论坛。

[**谷歌像素论坛**](https://forum.xda-developers.com/pixel) [**谷歌像素 XL 论坛**](https://forum.xda-developers.com/pixel-xl)

[**谷歌 Pixel 2 论坛**](https://forum.xda-developers.com/pixel-2) [**谷歌 Pixel 2 XL 论坛**](https://forum.xda-developers.com/pixel-2-xl)

[**谷歌 Pixel 3 论坛**](https://forum.xda-developers.com/pixel-3) [**谷歌 Pixel 3 XL 论坛**](https://forum.xda-developers.com/pixel-3-xl)

如果你安装了更新并注意到一些我们还没有发现的新东西，[给我们发送一个提示](https://www.xda-developers.com/tip-us/)，如果我们根据你的提示写了一篇文章，你就可以得到一个**免费的 XDA 无广告月**！另外，如果你安装了更新，一定要查看一下[反馈](https://developer.android.com/preview/feedback.html)和[错误报告](https://developer.android.com/preview/bug)页面。谷歌也在关注 reddit 上的一个新的子编辑以获取反馈。

* * *

## 如何在 Pixel 2、Pixel 2 XL、Pixel 3 或 Pixel 3 XL 上安装 Android Q Beta 1

如果你的设备是 rooted 的，或者你对系统或供应商分区做了任何更改，你需要使用工厂镜像安装 Android Q。如果你还没有解锁引导程序，并且使用的是最新的 Android Pie 版本，那么你可以下载 OTA 来节省时间。在开始之前，按照本教程设置 [ADB 和 Fastboot。](https://www.xda-developers.com/install-adb-windows-macos-linux/)

### OTA 图像

1.  从上表中下载适合您设备的 OTA 文件。
2.  将你的手机启动到 Android 系统并连接到你的电脑，在你存储 ADB 二进制文件的同一个目录下打开一个命令提示符或终端窗口。
3.  输入以下命令进入恢复模式: **Windows 命令提示符:**`adb reboot recovery`**Windows PowerShell:**`.\adb reboot recovery`**MAC OS/Linux 终端:** `./adb reboot recovery`
4.  在恢复模式下，选择“应用来自 ADB 的更新”
5.  输入以下命令，侧载 Android Q OTA 更新文件: **Windows 命令提示符:**`adb sideload ota_file.zip`**Windows PowerShell:**`.\adb sideload ota_file.zip`**MAC OS/Linux 终端:** `./adb sideload ota_file.zip`其中“ota_file.zip”是您在步骤 1 中下载的 OTA 文件的名称。
6.  通过选择“立即重启系统”选项重启手机。

### 工厂形象

1.  从上表中的链接之一为您的设备下载 Android Q 工厂映像。
2.  提取工厂图像文件。
3.  在该文件夹中，您将看到一个引导程序映像、一个广播映像、一个 zip 文件、一个 Windows 批处理文件和两个。sh 脚本文件。如果你不在乎擦除所有数据，只想立即更新，那么继续双击 flash-all.bat(如果你在 Windows 上)或 flash-all.sh(如果你在 macOS/Linux 上)(在使其可执行之后)。
4.  如果要刷新工厂映像而不擦除数据，请在文本编辑器中编辑 flash-all.bat 脚本(Windows)或 flash-all.sh 脚本(macOS/Linux ),并从“fastboot -w update”行中删除“-w”命令。然后，您可以开始启动 flash-all 脚本。

如果你想看每个步骤的截图，[这个指南](https://www.xda-developers.com/flash-monthly-security-update-google-pixel/)会帮到你。虽然它是为了帮助用户刷新每月的安全补丁更新而编写的，但是刷新一个主要的 Android 版本的步骤是相同的。

* * *

## 安卓 Q，我们来了！

我们团队中的一些作家，包括我自己，已经开始在我们的 Pixel 设备上安装 Android Q。我们将记录我们在第一个预览版中发现的新特性。由于早期的泄露，我们在发布前几周就已经设法揭开了许多关于 Android Q 的细节。请务必关注我们的 [Android Q](https://www.xda-developers.com/tag/android-q/) 标签，了解下一个主要 Android 版本的所有最新消息。以下是我推荐你开始接触的文章: