# Magisk v13.0 Beta 可供测试，带来了统一二进制、手动注入等功能

> 原文：<https://www.xda-developers.com/magisk-v13-0-beta-available-to-test-brings-unified-binary-manual-injection-and-more/>

三周前，XDA 知名开发者和贡献者 [topjohnwu](https://forum.xda-developers.com/member.php?u=4470081) [宣布](https://www.xda-developers.com/magisk-v13-android-o-single-binary/)，Magisk v13.0 将被重写，以拥有统一的二进制。经过数周的编码和调试，该项目的测试版终于可以测试了。

本月早些时候，Magisk 管理器[已经从 Google Play 中移除](https://www.xda-developers.com/magisk-manager-removed-from-play-store-developer-responds-on-the-future-of-magisk/)。这个[项目现在托管在](https://labs.xda-developers.com/store/app/com.topjohnwu.magisk) [XDA 实验室](https://www.xda-developers.com/xda-labs/)的上，如果你想继续的话，但是传统的论坛下载也可以。然而，Play Store 的惨败并没有阻止 topjohnwu 发布他备受推崇的项目的新测试版本。

如前所述，最新的测试版带有统一的二进制文件。二进制本身可以作为 *resetprop，su，magiskpolicy，magiskhide* 。所有操作现在都在同一个*统一守护进程*中运行。将分散的二进制文件合并成一个应该可以改善它们之间的通信，并使应用程序的响应速度更快。

统一二进制并不是唯一的新特性，因为新的测试版带来了其他值得一提的改进。从 v13.0 Magisk 开始，**将允许在没有根** **和自定义恢复**的安卓设备**上修补引导镜像**。关于手动注入的消息应该会让一些开发人员高兴，因为现在实现 root 应该容易多了。Topjohnwu 计划很快发布补丁，并贴出说明。一旦发布，将会进入 Magisk 管理器的稳定版本。

MagiskSU 也进行了更新。新版本提供了多用户支持、重新认证支持以及对稳定性和性能的错误修复。不幸的是，也有一些坏消息。在此版本中， [SuperSU](https://forum.xda-developers.com/apps/supersu) 兼容性已暂时取消。开发商说**这不是针对 SuperSU** 的举措，并计划提供一个可行的解决方案。那些不打算切换根应用的用户应该暂时屏住呼吸。

如果你想测试新特性，你应该访问新创建的测试版线程。请记住，任何应用程序的测试版都不可能完全没有错误。您也可以通过 XDA 实验室获得 Magisk v12.0 的稳定版本。

* * *

[**获取 Magisk v13.0 BETA**](https://forum.xda-developers.com/apps/magisk/beta-magisk-v13-0-0980cb6-t3618589) [**在我们的论坛中查看 Magisk！**](https://forum.xda-developers.com/apps/magisk/official-magisk-v7-universal-systemless-t3473445/)