# 如何 Root 你的荣誉 8 并安装 TWRP 和 Xposed

> 原文：<https://www.xda-developers.com/honor-8-root-twrp-and-xposed/>

# 如何 Root 你的荣誉 8 并安装 TWRP 和 Xposed

了解如何根你的荣誉 8 以及安装 TWRP 和 x 曝光。按照这个 XDA 电视教程获得根在您的设备上。

在这个视频中，TK 向我们展示了如何根 FRD-L04 和 FRD-L09 版本的荣誉 8。根，我们将闪存 TWRP 和安装 SuperSU。

在我们开始根教程之前，你需要解锁你手机上的引导程序。参见[这段](https://www.youtube.com/watch?v=C_svTrjyU7o)视频，了解如何解锁 Honor 8 上的引导加载程序。

### 要求:

*   解锁的引导加载程序
*   下载 [TWRP](http://bit.ly/2ff914n) 和 [SuperSU](http://bit.ly/2eBwX6M)
*   确保在开发人员的选项中打开了 USB 调试。
*   下载并安装正确的驱动程序和 ADB 工具。
*   看一遍视频，然后再看一遍，以确保你得到了流程或工作。

一旦您将设备与您的 PC 设置为 ADB 和快速启动连接，我们就可以开始了。

[spacer color="FFFFFF" icon= "选择一个图标"]

### 安装 TWRP

1.  将您的设备连接到您的电脑，并确保通过 ADB 对您的电脑进行身份验证。(当您在命令提示符下键入[ ADB devices ]时，您应该能够看到您的设备)
2.  键入[ adb reboot bootloader ]并等待设备重新启动进入快速启动模式
3.  键入[快速启动设备]以确认您已连接到您的设备
4.  确保保存下载的恢复。img 放在与你正在运行的 Adb/fastboot 工具相同的文件夹中，然后键入[ fastboot flash recovery TWRP 镜像。IMG (替换。具有下载文件的确切名称的 img)
5.  当完成正常重启时
6.  当设备重新启动时，打开 ADB 并键入[ adb 重启恢复
7.  你的设备应该重新启动进入 TWRP
8.  不要更改为“读/写”,保持只读模式并进行备份
9.  备份完成后，通过转到“装载”并禁用只读选项来启用“读/写”

[spacer color="FFFFFF" icon= "选择一个图标"]

### 给设备找根

1.  在恢复模式下连接时，将 Supersu2.78 stable 传输到您的设备并安装。安装后，重新启动
2.  根后，您的设备可能会重新启动 2 至 3 次。这很正常，请耐心等待。
3.  系统将重新启动，你应该有根。用你最喜欢的 root 应用测试 root 权限(我喜欢 XDA 实验室)

[spacer color="FFFFFF" icon= "选择一个图标"]

### 暴露安装

1.  安装 [xposed 安装程序](http://bit.ly/1DLOwEr) 3.11 apk。
2.  通过[ adb 重启恢复 ]或 play store 上您最喜欢的 APM 应用程序重启恢复
3.  安装 86 版 sdk23 arm64 二进制文件 zip 并重新启动
4.  第一次启动大约需要 6 分钟
5.  重新启动后，回到恢复模式，并在 Xposed 安装完成后进行另一次备份
6.  现在你可以开始检查模块了。一次做一个，并且总是在安装暴露的模块之前执行备份

如果你仔细按照说明，你应该都准备好了！