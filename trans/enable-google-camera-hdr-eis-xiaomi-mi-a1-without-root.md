# 在无 Root 的小米米 A1 上启用谷歌相机 HDR+和 EIS

> 原文：<https://www.xda-developers.com/enable-google-camera-hdr-eis-xiaomi-mi-a1-without-root/>

小米 Mi A1 是小米的第一款 Android One 智能手机。它是在 9 月份发布的，规格清单相当不错，包括高通骁龙 625 片上系统，4gb 内存搭配 64GBs 存储，5.5 英寸全高清(1920x1080) IPS 显示屏，双 12MP + 12MP(广角+长焦)后置摄像头，以及 3080mAh 电池。这款手机配备了几乎库存的 Android 7.1 牛轧糖，上个月它收到了 Android Oreo 更新。

Mi A1 的双后置摄像头设置价格合理，12MP 主后置广角摄像头与 12MP 带“长焦”镜头的摄像头配对。[在我们对这款手机](https://www.xda-developers.com/xiaomi-mi-a1-xda-android-review/)的评测中，我们发现它的摄像头比 Redmi Note 4 的摄像头有明显的改进，但仍有改进的空间。值得注意的是，电子图像稳定(EIS)仍然没有出现。

这就是非官方的谷歌相机 HDR+端口来拯救。从 Redmi Note 3 到 [Essential Phone](https://www.xda-developers.com/essential-phones-camera-app-updated-automatic-hdr-mode/) 等一系列手机上的端口被发现在许多情况下显著提高了相机性能。在小米设备上使用该端口的问题是，小米设备没有默认启用 Camera2 API。启用它需要[通常要求用户](https://www.xda-developers.com/camera2api-magisk-module-enables/)启动他们的设备并且[编辑 build.prop](https://www.xda-developers.com/enable-night-light-camera2-api-xiaomi-mi-a1-magisk/) ，这通常意味着他们不能接收 OTA 更新。所以，那些不想 root 设备或者想接收 OTA 更新的用户，到目前为止都不太走运。

然而，[有一种方法可以在不修改任何系统文件的情况下启用 Camera2 API，本周](https://www.xda-developers.com/enable-camera2-api-xiaomi-mi-a1/)XDA 公认的开发者 flex1911 详细介绍了这种方法。它包括解锁引导加载程序并通过 Magisk 启动设备，通过 setprop 命令启用 [Camera2 API](https://www.xda-developers.com/enable-night-light-camera2-api-xiaomi-mi-a1-magisk/) ，然后完全移除 Magisk 并重新锁定引导加载程序。这意味着仍然能够接收 OTA 更新。

更进一步，XDA 成员 [AridaneAM](https://forum.xda-developers.com/member.php?u=8676627) 发布了一款**自动化工具，无需 root 即可安装谷歌摄像头 HDR+端口**。为了安装端口，用户需要执行以下步骤:

*   禁用模式/密码安全锁
*   启用开发人员选项
*   启用 OEM 解锁和 USB 调试
*   安装 ADB / fastboot 驱动程序
*   启用 HAL3 和 EIS
*   安装 Google Camera zip，同时使用 ADB 将手机连接到 PC。

该工具会自动解锁引导加载程序，临时安装 TWRP，安装谷歌摄像头端口，然后重新锁定引导加载程序，而根本不需要对设备进行根操作。用户可以使用这种方法来安装端口，而根本不需要启动他们的设备。

[**在小米米 A1 上下载谷歌摄像头安装程序**](https://forum.xda-developers.com/mi-a1/how-to/tool-google-camera-root-magisk-enable-t3747585)