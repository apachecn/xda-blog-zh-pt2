# 通过 Magisk 模块启用 Camera2API 以获得更多相机选项

> 原文：<https://www.xda-developers.com/camera2api-magisk-module-enables/>

# Magisk 模块启用 Camera2API

一个新的 Magisk 模块可以在你的智能手机上启用 Camera2API，这样你就可以使用最近移植的具有 HDR+功能的谷歌相机应用程序。

我们最近看到了用于新骁龙设备的谷歌摄像头的[端口，允许 HDR+在其上工作。然而，要做到这一点，需要启用 camera2api，因为它依赖于该 api。你可以通过 build.prop 编辑来实现，或者你可以安装一个来自 XDA 资深会员](https://www.xda-developers.com/google-camera-hdr-ported/) [otaconremo](https://forum.xda-developers.com/member.php?u=6039818) 的新 Magisk 模块。该模块需要 Magisk 版本 13 及以上，可通过 Magisk 管理器安装，或在 TWRP 刷新。之后，您可以在终端中运行“getprop | grep camera”命令，并查找“persist.camera.HAL3.enabled 1”以确保它正常工作。

* * *

[**在我们的 Magisk 论坛**](https://forum.xda-developers.com/apps/magisk/module-camera2api-enabler-t3656651) 查看 Camera2API 启用程序