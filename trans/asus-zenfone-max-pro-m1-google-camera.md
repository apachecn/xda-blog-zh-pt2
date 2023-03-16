# 在没有 root 的华硕 ZenFone Max Pro M1 上使用谷歌相机

> 原文：<https://www.xda-developers.com/asus-zenfone-max-pro-m1-google-camera/>

# 在没有 root 的华硕 ZenFone Max Pro M1 上使用谷歌相机

让谷歌像素的谷歌摄像头端口在华硕 ZenFone Max Pro M1 上工作，而无需解锁引导加载程序或需要 root 访问权限。

华硕 ZenFone Max Pro M1 迅速成为印度最受欢迎的中端手机之一。凭借 6 英寸 FHD+显示屏、高通骁龙 636 片上系统、4 或[6gb 内存](https://www.xda-developers.com/asus-zenfone-max-pro-m1-6gb-ram-variant-india/)、安卓 8.1 奥利奥(Android 8.1 Oreo)和 5000 毫安时大容量电池，不难看出华硕的设备为何不断售罄。(幸运的是，他们已经放弃了闪购模式，[现在提供这种设备 24/7](https://www.xda-developers.com/asus-zenfone-max-pro-m1-flash-sale-available/) 。)购买廉价或中端智能手机的最大缺点之一是相机质量——你无法在更便宜的设备上媲美谷歌 Pixel 2、三星 Galaxy S9 或 OnePlus 6 等旗舰设备的拍照质量。幸运的是，这就是谷歌相机端口的用武之地。

谷歌 Pixel 出色的谷歌相机应用程序及其 HDR+和人像模式功能使谷歌 Pixel 成为市场上最好的移动摄影智能手机之一。谷歌相机应用程序最棒的部分是，由于谷歌令人难以置信的软件算法，它使这一切成为可能。与配备三摄像头的华为 P20 Pro 等设备相比，配备单摄像头的谷歌 Pixel 2 毫不逊色。这就是为什么谷歌相机应用程序的端口在我们的论坛上如此受欢迎，也是为什么我们最近为所有这样的端口开放了一个中心。

毫不奇怪，华硕 ZenFone Max Pro M1 的所有者想要从谷歌相机馅饼中分一杯羹，但不幸的是，安装端口并不像只是从侧面装载 APK 那么简单。那是因为 Google Camera 应用需要启用 Camera2API，通常不修改系统分区中的 build.prop 就无法启用(因此需要 root 权限。)但是最近，我们论坛上的用户发现，你可以通过快速启动命令在华硕 ZenFone Max Pro M1 上启用 Camera2API，从而允许你在没有 root 用户的情况下访问谷歌相机端口！

XDA 资深会员[沙加拉卡](https://forum.xda-developers.com/member.php?u=1813976)发现了这个方法。

* * *

## 启用 Camera2API 在华硕 ZenFone Max Pro M1 上使用谷歌相机

1.  下载适用于您的操作系统的[最新平台工具。我们需要最新版本的快速启动二进制文件。Fastboot 用于向设备的引导加载程序发出命令。](https://www.xda-developers.com/install-adb-windows-macos-linux/)
2.  关闭手机电源，进入引导模式。(启动时按住电源和音量键进入引导程序屏幕。)
3.  在 fastboot 二进制文件所在的同一目录中打开命令提示符或 PowerShell (Windows)或终端窗口(macOS 或 Linux)。
4.  基于您的 OS 输入以下命令: **Windows 命令提示符:**`fastboot oem enable_camera_hal3 true`**Windows PowerShell:**`.\fastboot oem enable_camera_hal3 true`**MAC OS 或 Linux 终端:** `./fastboot oem enable_camera_hal3 true`
5.  重启你的设备。
6.  现在从我们的[中心](https://www.xda-developers.com/google-camera-port-hub/)或者从 [XDA 论坛](https://forum.xda-developers.com/asus-zenfone-max-pro-m1)为你的华硕 ZenFone Max Pro M1 下载最好的谷歌摄像头端口。
7.  或者，您可以通过使用谷歌 Play 商店的 Camera2 API Probe 应用程序来检查 Camera2API 是否已启用。

享受使用华硕 ZenFone Max Pro M1 上的谷歌摄像头端口吧！这种方法之所以有效，是因为它使用内置的 bootloader 命令来启用 [Camera HAL 3](https://source.android.com/devices/camera/camera3) 。这个命令是华硕留下的，所以感谢他们让这成为可能！