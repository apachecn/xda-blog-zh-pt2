# 超级马里奥 64 可以在没有任天堂 64 模拟器的情况下在 Android 上运行

> 原文：<https://www.xda-developers.com/super-mario-64-android-port-nintendo-64/>

# 超级马里奥 64 可以在没有任天堂 64 模拟器的情况下在 Android 上运行

多亏了一个开源项目，现在可以在你的 Android 手机上编译和播放超级马里奥 64，而不需要模拟器！

超级马里奥 3D 全明星赛[终于来了](https://www.nintendo.com/games/detail/super-mario-3d-all-stars-switch/)，这意味着你现在可以在你的任天堂 Switch 上玩该系列的前三款 3D 平台游戏——超级马里奥 64、超级马里奥阳光和超级马里奥银河。如果你正在寻找一种在你的 Android 手机上享受桃子公主蛋糕的方法，你可以[用 Switch emulation](https://www.xda-developers.com/shady-nintendo-switch-emulator-android/) 试试运气，或者拿一个兼容的任天堂 64 模拟器潜入超级马里奥 64 的世界。

不幸的是，模仿也有它的缺点。没有什么可以击败本机可执行文件的性能和可扩展性，这是长期以来努力将超级马里奥 64 ROM 反向工程为等效的 C 代码库的驱动力。只要你能获得[人类可读的 C 代码](https://github.com/n64decomp/sm64)，你就有能力将游戏移植到任何平台，包括 Android。

事实上，XDA 成员 [VDavid003](https://forum.xda-developers.com/member.php?u=9671514) 已经加紧准备了一份报告[，其中包含一个准备好的用于 Android](https://github.com/VDavid003/sm64-port-android-base) 的超级马里奥 64 端口，使用简单的 DirectMedia Layer (SDL)和 OpenGL ES 2.0。您可以将 repo 克隆到运行 Microsoft Windows 或 Linux 的 PC 上，准备构建环境，并在编译后最终获得 APK，它可以轻松地加载到 Android 设备上。然而，让移植过程更有趣的是，**它也可以直接在你的 Android 手机上编译**！

* * *

## 如何在 Android 上原生编译和运行超级马里奥 64

免责声明: XDA 不会宽恕盗版游戏。您必须提供您自己的超级马里奥 64 副本，以下过程才能正常工作。

如果命令行 voodoo 是你的东西，那么按照以下步骤来配置 Android 中的构建环境，并从头编译经典的任天堂平台:

1.  安装来自谷歌 Play 商店的 [Termux](https://www.xda-developers.com/termux-the-ultimate-linux-terminal-emulator-for-android-xda-spotlight/) 。
2.  在 Termux 环境中安装所需的依赖项:

    ```
     pkg install git wget make python getconf zip apksigner clang 
    ```

3.  使用 git:

    ```
     git clone https:
    cd sm64-port-android 
    ```

    克隆适当的存储库
4.  使用 Termux 复制游戏的 baserom。再说一次，**你必须提供你自己的副本**。

    ```
     termux-setup-storage
    cp /sdcard/path/to/your/baserom.z64 ./baserom.us.z64 
    ```

5.  获得 SDL 包括:

    ```
     ./getSDL.sh 
    ```

6.  开始构建:

    ```
     make  
    ```

    您可以增加“jobs”参数的值，这取决于您可以为构建过程贡献多少个 CPU 内核。
7.  如果一切顺利，最终的超级马里奥 64 APK 应该在“构建”文件夹中:

    ```
     ls -al build/us_pc/sm64.us.f3dex2e.apk 
    ```

* * *

您是否发现了开发人员尚未修复的编译故障？想提交补丁？前往下面链接的 GitHub repo。

**[超级马里奥 64 安卓端口— GitHub 回购](https://github.com/VDavid003/sm64-port-android)**