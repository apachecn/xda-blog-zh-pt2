# Mod 在小米 POCO F1 上为 4K@30fps 视频启用 EIS

> 原文：<https://www.xda-developers.com/mod-eis-4k30fps-videos-xiaomi-poco-f1-and-mi-mix-3/>

# Mod 为小米 POCO F1 和 Mi Mix 3 上的 4K@30fps 视频启用 EIS

在 MIUI 10 相机的改进版的帮助下，用 Xaiomi Poco F1 或 Mi MIX 3 以 30fps 拍摄 4K 视频时使用 EIS。

小米的 POCO F1 以令人难以置信的价格包装了令人惊叹的规格和值得夸耀的功能。虽然整体包装功能丰富，但小米已经偷工减料或忽略了某些领域，这使得 POCO F1 无法与其他旗舰竞争。

虽然 [POCO F1](https://www.xda-developers.com/xiaomi-poco-f1-design-display-gaming-performance-review/) 可以捕捉分辨率高达 4K 的视频，但电子图像稳定功能仅限于全高清(1080p)录制。幸运的是，有一个非官方的模式来添加这个功能。mod 还允许你在基于 AOSP 的定制 rom 上安装官方的 [MIUI 10 相机应用。](https://www.xda-developers.com/miui-10-camera-port-xiaomi-poco-f1/)

要开始，请按照下列步骤操作:

*   确保您的 POCO F1 是根用户
*   使用本指南安装 Magisk
*   从[此链接](https://github.com/XEonAX/ANXCamera10/releases/tag/20.beryllium)下载 Magisk 模块 ZIP(搜索设备的代号“铍”)并激活它
*   前往“设置”>“应用”>“高级”>“特殊应用访问”>“使用权限”>“相机”,授予用户访问权限，并将其设置为“允许”

您可以开始正常使用您的设备，EIS 现在将默认激活。

一位用户指出，这种模式也适用于小米 MIX 3，可以在小米的旗舰智能手机上以 30fps 的速度支持 4K 的 EIS。要让它运行，从[这里](https://github.com/XEonAX/ANXCamera10/releases/download/ZeroRelease/ANXMiuiCameraMagisk_18.RobustDenseThrasher.zip)下载 Magisk mod ZIP，并遵循与上面相同的程序。