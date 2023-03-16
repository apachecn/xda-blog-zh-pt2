# 小米为其骁龙 865 设备发布了 GPU 驱动程序更新

> 原文：<https://www.xda-developers.com/xiaomi-adreno-gpu-driver-update-snapdragon-865/>

当高通在 12 月宣布骁龙 865 移动平台时，他们引入的最有趣的“骁龙精英游戏”新功能之一是可更新的 GPU 驱动程序。通常，GPU 驱动程序更新包含在发送给用户的 OTA 更新中，这意味着用户必须等待 OTA 更新推出，才能获得更新的驱动程序。通过骁龙 765 和骁龙 865，高通致力于使原始设备制造商通过应用商店发布 GPU 驱动程序更新成为可能。第一家利用这一功能的 OEM 厂商似乎是小米，因为该公司在其中国应用商店发布了 Adreno 650 GPU 驱动程序更新。

小米最近在其中文应用商店上传了一款名为“GPU 驱动更新程序”的应用。该应用程序的软件包名称为“com.xiaomi.ugd”，旨在更新由高通骁龙 865 SoC 驱动的[小米 Mi 10](https://forum.xda-developers.com/xiaomi-mi-10) 、[小米 Mi 10 Pro](https://forum.xda-developers.com/xiaomi-mi-10-pro) 和 [Redmi K30 Pro](https://www.xda-developers.com/tag/redmi-k30pro/) 中的 Adreno 650 GPU。此次更新优化了几款游戏，包括 PUBG Mobile、堡垒之夜和 Honkai Impact 3rd。OpenGL ES 和 Vulkan 的更新也包含在 GPU 驱动程序更新中。

我们得到了我们的手在 GPU 驱动程序更新 APK，看看它包含什么。正如预期的那样，APK 主要包含了高通为骁龙 865 更新的 GPU 驱动程序库(代号为“kona”)。)

我们查看了详细说明 OEM 如何在其设备上启用可更新 GPU 驱动程序的文档。总之，OEM 从高通获取一个空的已签名预发布驱动程序 APK，使用唯一的包名称解包并重新签名这个 APK，将包放在/vendor/apps 中，设置一些系统属性，将新游戏添加到白名单中，修改设置应用程序以在首选项列表中包括 GPU 驱动程序更新程序，并在开发者选项中的游戏驱动程序首选项中启用新驱动程序。我们不知道白名单的确切用途，但有可能只有白名单包才能与更新的 GPU 库一起工作。根据我所读到的，不清楚为什么这些可更新的 GPU 驱动程序不能由高通自己而不是原始设备制造商提供。尽管如此，高通似乎已经让原始设备制造商实现起来非常简单，所以希望我们会看到更多的原始设备制造商为他们的骁龙 765 和骁龙 865 设备实现可更新的 GPU 驱动程序。