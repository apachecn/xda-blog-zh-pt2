# 从 Mi Max 移植到其他小米设备的 MiHome 启动器

> 原文：<https://www.xda-developers.com/mihome-launcher-grid-ported-xiaomi/>

# MiHome 启动器带有新的网格大小选项，可移植到其他小米设备

小米 Mi Max 有一个新的 mihome 启动器，有一个额外的网格大小选项。这个现在已经移植到安卓 7.0 上的其他小米设备上了！

MiHome launcher 已经由 XDA 成员 [Dadovvv，](https://forum.xda-developers.com/member.php?u=2989384)移植，他花了几个小时的时间从[小米 Mi Max](https://www.xda-developers.com/xiaomi-mi-max-xda-review/) 获得它，并使它可以用于其他运行 MIUI，Android 7.0 的小米手机。您将需要 root 访问权限和启用 root 的文件管理器(如 MiXplorer)来下载和安装修改后的应用程序，以及更改您的 DPI。你的 DPI 必须低于 440。

[appbox xda com.mixplorer]

要安装该应用程序，您需要将该应用程序复制到/system/priv-app/MiuiHome，并删除 oat 文件夹(如果存在)。将文件的权限设置为 644 (-rw-r - r -)并重新启动！应用程序应该可以工作，并允许您更改网格大小。看看下面的港口！

* * *

[**MiHome 启动器端口**](https://forum.xda-developers.com/redmi-note-4/themes/port-miuihome-launcher-grid-size-5x6-t3664186)