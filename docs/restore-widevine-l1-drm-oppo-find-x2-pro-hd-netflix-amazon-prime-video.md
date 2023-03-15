# 在 OPPO Find X2 Pro 上启用 Widevine L1 以传输高清网飞

> 原文：<https://www.xda-developers.com/restore-widevine-l1-drm-oppo-find-x2-pro-hd-netflix-amazon-prime-video/>

OPPO Find X2 Pro ( [第一印象](https://www.xda-developers.com/oppo-find-x2-pro-hands-on-first-impressions/))是中国智能手机品牌[最新旗舰产品](https://www.xda-developers.com/oppo-find-x2-specifications-features-pricing-availability/)之一。这款由高通骁龙 865 驱动的庞然大物配备了 6.7 英寸 QHD+ AMOLED 显示屏，刷新率高达 120Hz，三摄像头设置，48MP 索尼 IMX689 主传感器，12GB lpddr 5 内存和 512 GB UFS 3.0 存储。此外，这款智能手机配备了 PixelWorks 的专用[“Iris 5”显示芯片，这无疑有助于 OPPO 找到 X2 Pro 以](https://www.xda-developers.com/oppo-find-x2-pro-pixelworks-iris-5-display-chip-goodix-new-voice-audio-technology/)[获得“YouTube 签名设备”认证](https://www.xda-developers.com/oppo-find-x2-pro-certified-youtube-signature-device/)。该设备还被网飞列入白名单，可以在高清流媒体上播放 HDR——如果没有 Widevine Level 1 DRM 状态，这两项功能都是不可能的。

**[OPPO 找 X2 Pro 论坛](https://forum.xda-developers.com/find-x2-pro)**

然而，有一个问题。我们论坛上的一些用户报告说，他们的 OPPO Find X2 Pro 设备的 Widevine 级别设置为 L3。因此，他们只能观看网飞或亚马逊 Prime Video 的视频，最高画质为 540p。我们已经看到[原始设备制造商通过软件更新解决 Widevine 故障](https://www.xda-developers.com/xiaomi-redmi-note-9-pro-v11-0-5-0-update-fixes-widevine-l1-hdr-related-bugs/)，但是解决这个特殊问题的过程完全不同。

事实证明，受影响的 OPPO Find X2 Pro 设备需要在授权服务中心进行物理处理。整个情况与 OnePlus 5/5T 的情况非常相似，智能手机没有在 TrustZone 界面中安装所需的密钥，并且[用户必须亲自将他们的设备发送到一加](https://www.xda-developers.com/oneplus-5t-netflix-amazon-prime-video-hd/)才能安装密钥。有趣的是，OPPO 和一加都是步步高电子的子公司，这在某种程度上解释了相似之处。只是这一次，你实际上可以自己修理，而不用去服务中心！

XDA 高级成员 [trapcoder666](https://forum.xda-developers.com/member.php?u=8571899) 已经设法得到了 OPPO 技术人员用来安装 Widevine DRM 相关密钥的内部工具。该工具被称为“Widevine 服务”，是一个通用的 Android 应用程序，不需要任何认证。只需将 APK 加载到你的 OPPO Find X2 Pro 上，点击“安装”，就大功告成了。清除网飞应用程序的缓存和数据将有助于强制应用程序查看新的 Widevine 级别。

维修工具(链接如下)也有可能与其他 OPPO 设备兼容，但我们还没有找到任何具体的证据来支持这一理论。尽管这是 OPPO 的一个官方(尽管已泄露)应用程序，但在尝试自己安装 Widevine keys 之前，备份手机上的所有重要数据始终是一个好主意。

**Widevine L1 为 OPPO Find X2 Pro 安装的安装程序:[下载](https://drive.google.com/file/d/1-a07h9lX2LO1IwEzifbmQWxg0hchSUDj/view?usp=sharing) ||| [XDA 讨论线程](https://forum.xda-developers.com/find-x2-pro/how-to/widevine-issue-l3-l1-t4115977/)**