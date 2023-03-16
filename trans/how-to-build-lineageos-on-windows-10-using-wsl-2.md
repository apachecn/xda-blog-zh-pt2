# 如何使用 WSL 2 在 Windows 10 上构建 LineageOS

> 原文：<https://www.xda-developers.com/how-to-build-lineageos-on-windows-10-using-wsl-2/>

用于 Linux 的第二代 Windows 子系统，通常被称为 **WSL 2** ，在微软的 Build 2019 开发者大会期间[宣布](https://www.xda-developers.com/microsoft-announces-windows-terminal/)。与[遗留的 WSL 实现](https://www.xda-developers.com/microsoft-announces-important-features-at-build-2017/)相比，由于主要的架构重写，WSL 2 在文件系统繁重的操作上表现得更好。Windows 10 最新的稳定通道构建，即[Windows 10 2020 年 5 月更新](https://www.xda-developers.com/microsoft-windows-10-may-2020-update-wsl-2-revamped-cortana-assistant-your-phone-calls-arm-devices/)，使 WSL 2 可供所有用户使用。使用 WSL 2，Windows 用户可以很容易地从零开始编译 AOSP 或定制 rom，如 LineageOS，而无需安装一个完整的 GNU/Linux 发行版。

这不是我们第一次[强调](https://www.xda-developers.com/build-lineageos-windows-10/)[使用 WSL 在 Windows](https://www.xda-developers.com/build-lineageos-16-windows-10-pc/) 上构建 LineageOS 的可能性，但是现在情况有点不同了。第一个稳定版本的 [Windows 终端](https://www.xda-developers.com/microsoft-releases-windows-terminal-1-0-package-manager-announces-linux-gui-app-support-gpu-acceleration-subsystem-linux-wsl-2/)已经发布，CLI 爱好者现在可以原生获得 GPU 加速的文本渲染、自定义键绑定、带有自定义配色方案的选项卡式外壳以及许多其他有用的功能。鉴于您可以像终端中的另一个选项卡一样直接调用 WSL，Windows 10 的用户可以在编译 LineageOS 时应用不同的配置和快捷方式(就像预配置的 Linux 环境一样)。

XDA 资深成员/LineageOS 团队成员 [Uldiniad](https://forum.xda-developers.com/member.php?u=7350242) 已经[更新了他的论坛帖子](https://forum.xda-developers.com/showpost.php?p=82684345)关于如何在使用 WSL 2 的 Windows 10 PC 上编译基于 Android 10 的最新版本 LineageOS、 [LineageOS 17.1](https://www.xda-developers.com/lineageos-17-1-android-10-officially-available/) 。在尝试执行本地构建之前，确保你有足够的免费存储空间和无限制的互联网计划。例如，考虑到同步的源代码以及构建输出，Uldiniad 为 [OnePlus 6](https://forum.xda-developers.com/oneplus-6) (代号“enchilada”)编译一个干净的 LineageOS 17.1 构建需要大约 340GB 的存储空间。

如果你的 PC 满足从源代码构建 Android 的[硬件要求](https://source.android.com/setup/build/requirements#hardware-requirements)，那么按照以下步骤在 Windows 10 中设置一个 WSL 2 构建环境，并编译 LineageOS 17.1:

1.  打开[微软商店](https://aka.ms/wslstore)
2.  搜索并安装 Ubuntu 应用程序
3.  打开应用程序，按照首次设置步骤进行操作
4.  更新软件包并安装以下软件

    ```
     sudo apt update && sudo apt full-upgrade -y && sudo apt install -y build-essential ccache libncurses5 libssl-dev m4 unzip zip 
    ```

5.  为源代码创建一个目录(并转到该目录):

    ```
     mkdir -p ~/android/lineage && cd android/lineage 
    ```

6.  初始化 LineageOS 源存储库:

    ```
     repo init -u https: 
    ```

7.  同步信号源:

    ```
     repo sync 
    ```

8.  [打开缓存](https://wiki.lineageos.org/devices/klte/build#turn-on-caching-to-speed-up-build)加速构建。这一步是可选的，但是建议在后续的构建中使用。
9.  运行

    ```
     source build/envsetup.sh 
    ```

10.  准备设备专用代码:

    ```
     breakfast your_device_codename 
    ```

11.  将以下内容添加到`.repo/local_manifests/roomservice.xml` :

    ```
     <project name="TheMuppets/proprietary_vendor_your device brand" path="vendor/your device brand" remote="github" /> 
    ```

12.  再次同步信号源:

    ```
     repo sync 
    ```

13.  开始构建:

    ```
     brunch your_device_codename 
    ```

**[用 WSL 2 在 Windows 10 上构建 linegeos 17.1——XDA 讨论线程](https://forum.xda-developers.com/android/software-hacking/guide-how-to-build-lineageos-15-1-t3750175)**

根据 Uldiniad 的说法，他的 AMD 锐龙 9 3950X 驱动的 PC(完整规格可在此处找到)花了 22 分钟来编译上述填充了 ccache 的 LineageOS 17.1 构建。

* * *

你认为你的电脑足够强大来处理编译工作吗？请在下面的评论中告诉我们你在 WSL 上使用 LineageOS 的体验！