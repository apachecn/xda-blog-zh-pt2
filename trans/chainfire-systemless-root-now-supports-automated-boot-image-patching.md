# Chainfire 的无系统根支持启动镜像补丁

> 原文：<https://www.xda-developers.com/chainfire-systemless-root-now-supports-automated-boot-image-patching/>

继续进行[无系统根](http://www.xda-developers.com/chainfire-releases-root-for-android-6-0-without-modifying-system/)实验，XDA 高级认可开发商 Chainfire 的 SuperSU Beta 最新版本包括在安装时自动启动映像补丁。

这基本上消除了为设备上传特定启动映像的需要，因为 SuperSU 的 zip 安装程序将在 Android 6.0 和基于 Android 5.1 的 Touchwiz 上以无系统模式安装 SuperSU，然后修补启动映像。

此测试版的开发说明如下:

> 引导镜像补丁目前只支持 gzip 压缩 ramdisks 和标准的 Android 引导镜像格式。一些设备不使用标准格式，许多定制内核使用 gzip 以外的压缩格式。在修补之前，会对原始内核进行备份(/data/stock_boot_.img.gz)。
> 
> ...ZIP 中的脚本通常包含许多特定的文档，但是对于 systemless，我还没有写那部分。sukernel 工具做了很多修补工作，它非常健谈，告诉你它到底做了什么和如何做。在 TWRP，你可以在安装 ZIP 文件后看到它的输出“adb shell cat /tmp/recovery.log”。

这次安装说明有几个步骤。本质上，从/system 分区中的普通 SuperSU 安装迁移的用户必须在安装之前刷新系统分区的内容。这通常是通过刷新备用 ROM 实现的，但每个设备的说明可能略有不同。之前安装 SuperSU 无系统的用户在刷新测试版 zip 之前，仍然需要刷新普通内核。Chainfire 确保未来对无系统根的更新将更容易执行，因此对于一次性设置来说，这些步骤不是很繁琐。

开发者已经在相当多的设备上测试了测试版，包括基于 Android 6.0 Marshmallow 和 CyanogenMod 13 的 Nexus 设备，以及基于 Android 5.1.1 的 Galaxy S6。你可以自己尝试一下，但是和 XDA 上的其他东西一样，**在安装**之前做个备份。如果有疑问，我们也建议搜索线程或论坛，了解兼容性或设备特定的问题。

如需下载，请前往[论坛帖子](http://forum.xda-developers.com/showpost.php?p=64161125&postcount=3)。开发人员要求讨论应该在[超级测试线程](http://forum.xda-developers.com/apps/supersu/2014-09-02-supersu-v2-05-t2868133)上进行，所以请前往那里进行一般性讨论。请记住，这是**的实验版**，很可能会有错误，所以风险自担。