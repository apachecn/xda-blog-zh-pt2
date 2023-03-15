# 如何解锁 Bootloader 并 Root 谷歌 Pixel 2 和 Pixel 2 XL

> 原文：<https://www.xda-developers.com/how-to-unlock-bootloader-and-root-the-google-pixel-2-and-pixel-2-xl/>

# 如何解锁 Bootloader 并 Root 谷歌 Pixel 2 和 Pixel 2 XL

XDA 公认的开发者/公认的贡献者 nathanchance 发布了关于如何解锁、闪光和 root 谷歌 Pixel 2 和 Pixel 2 XL 的指南。

许多发烧友预计，在第一代谷歌像素上获得根会像在谷歌的 Nexus 设备上获得根一样容易，但事实证明并非如此。Android Nougat 的 A/B 分区系统一开始就给开发者制造了很多头疼的问题， [Pixel 与最常见的漏洞利用](https://www.xda-developers.com/pixel-phones-not-yet-rootable-with-current-methods/)的不兼容只是增加了挑战。不用说，有理由担心[像素 2](https://www.xda-developers.com/tag/pixel-2/) 和[像素 2 XL](https://www.xda-developers.com/tag/pixel-2-xl/) 。但幸运的是，发展似乎进展顺利。

10 月下旬，[TWRP 的 alpha 端口为 Pixel 2 和 Pixel 2 XL](https://www.xda-developers.com/twrp-recovery-alpha-pixel-2-xl-available/) 提供。本周，XDA 公认的开发者/公认的贡献者 [nathanchance](https://forum.xda-developers.com/member.php?u=6842057) 发布了两款手机的解锁、闪烁和根源指南。

以下是开始的方法:

## 安装快速启动和 ADB

1.  解压缩硬盘上的文件夹。
2.  转到包含 ADB 和 Fastboot 文件的文件夹，在顶部的路径栏中键入“cmd”。
3.  命令提示符应该会打开，并在提示符上显示当前文件夹。
4.  键入以下命令:代码:

    ```
    adb --versionfastboot --version
    ```

此时，您应该会看到一些信息出现。如果是这种情况，那么 Fastboot 和 ADB 已经成功安装。

## 解锁 Pixel 2 / Pixel 2 XL 的引导程序

导读注意到解锁你的 Pixel 2 或者 Pixel 2 XL 的 bootloader 会擦手机。最好对任何重要数据进行备份，以防出现问题。

1.  在你的手机上，打开**设置**，导航到**系统**，然后**关于手机**，点击**构建号**七次。
2.  **开发者选项**现在可以在主设置页面看到。进入后打开 **USB 调试**和 **OEM 解锁**。
3.  将手机插入电脑，在 Windows 命令终端输入以下命令:

    ```
    adb reboot bootloader
    ```

4.  接下来，决定你是要做标准解锁还是关键解锁。一个[关键解锁](https://www.xda-developers.com/pixel-2-failing-flash-factory-images/)允许你直接刷新引导程序文件。否则，当您尝试这样做时，将会得到一个错误。
5.  根据上一步的决定，运行以下命令之一:

    ```
    fastboot flashing unlock
    ```

    或

    ```
    fastboot flashing unlock_critical
    ```

6.  按照设备上的提示进行操作，然后重新启动。

## 求像素 2 /像素 2 XL 的根

1.  从官方线程下载 Magisk Manager 并安装。
2.  抓取一个引导镜像来打补丁(你可以从最新的工厂镜像或者一个定制的内核镜像中选择一个)，然后用这个命令把它推送到你的设备上:

    ```
    adb push <path_to_file> /sdcard/Download
    ```

3.  打开 Magisk Manager 并点击**安装**按钮。
4.  在第一个提示符下点击**安装**，然后选择**补丁启动镜像文件**。将弹出一个文件管理器。
5.  选择要修补的启动映像，并让 Magisk Manager 对其进行修补。
6.  用这个命令把它从你的设备上拉下来:

    ```
    adb pull /sdcard/MagiskManager/patched_boot.img
    ```

7.  重启进入引导程序:

    ```
    adb reboot bootloader
    ```

8.  刷新启动映像并重新启动。代码:

    ```
    fastboot flash boot patched_boot.imgfastboot reboot
    ```

9.  打开 Magisk Manager，您的设备应该是根设备。

查看 Pixel 2 和 Pixel 2 XL 各自的论坛主题，了解解锁、闪烁工厂图像和寻根的技巧。

[**【XDA 论坛线程解锁/闪烁/生根像素 2 (walleye)**](https://forum.xda-developers.com/pixel-2/how-to/guide-unlock-flash-root-pixel-2-walleye-t3702417)

[**【XDA 论坛】线程解锁/闪烁/生根像素 2 XL(台门)**](https://forum.xda-developers.com/pixel-2-xl/how-to/guide-unlock-flash-root-pixel-2-xl-t3702418)