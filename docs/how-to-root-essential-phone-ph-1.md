# 如何使用 Magisk 找到基本电话(PH-1)

> 原文：<https://www.xda-developers.com/how-to-root-essential-phone-ph-1/>

# 如何使用 Magisk 找到基本电话(PH-1)

来自 XDA 社区成员的最新出版的一步一步指南显示了如何使用 Magisk 找到新的基本电话。

安迪·鲁宾的[基本产品](https://www.essential.com/)以[基本手机](https://www.xda-developers.com/tag/essential-phone/)(或 PH-1)成为头条新闻，这是一款全钛智能手机，配有模块化配件、双摄像头和靠近屏幕顶部的独特切口。在此期间，该公司进行了几次[摸索](https://www.xda-developers.com/essential-sued-keyssa-wireless-connector/)，但它不会很快放弃。最近的价格下跌重新激起了人们对这款基本手机的兴趣，我们看到社区对它的支持也开始活跃起来。

周二，我们谈到了 XDA 如何认可开发商 [invisiblek](https://forum.xda-developers.com/member.php?u=2385005) 发布的[基本手机](https://www.xda-developers.com/unofficial-factory-images-essential/)的非官方工厂图片。既然有恢复映像可以在出现问题时刷新，我们开始看到开发人员的额外工作。今天早些时候，XDA 资深成员 [bmg1001](https://forum.xda-developers.com/member.php?u=4550123) 整理了一份指南，展示如何使用 [Magisk](https://labs.xda-developers.com/store/app/com.topjohnwu.magisk) 为基本手机找到根。

该过程需要一个解锁的引导加载程序和一台安装了 Android 调试桥(ADB)和快速引导实用程序的计算机。(如果你以前没有使用过 ADB 或 Fastboot，[我们建议按照我们的指南](https://www.xda-developers.com/install-adb-windows-macos-linux/)。)你可以从这里(或者从这里【T4 镜】 )和 [Magisk v14.3 下载](https://forum.xda-developers.com/apps/magisk/beta-magisk-v13-0-0980cb6-t3618589)[的基本兼容版本。该指南还要求您拥有与您的手机内部版本号(](https://www.invisiblek.org/twrp-mata_2.img) [NMJ32F](https://drive.google.com/open?id=1t0MFnELEIUWKp5e9jFIemKWANI8ygCvX) - [NMJ20D](https://drive.google.com/open?id=1U9GOxoVgNhZS49Cv4PASAHq9GPy2l9ks) )匹配的 boot.img(内核)修改版本。

一旦您满足了先决条件，请按照以下步骤对您的手机进行 root:

1.  通过重启手机并同时按住**音量降低**和**电源按钮**，重启你的基本手机进入快速启动模式。一旦进入快速启动模式，使用以下 ADB 命令刷新 TWRP:快速启动 flash boot twrp.img
2.  从快速启动菜单中，选择并启动到“恢复模式”一旦 TWRP 启动，输入: adb shell twrp sideload
3.  然后输入: adb sideload magisk.zip
4.  Magisk 安装完成后，重新引导至快速启动模式。您可以通过 adb 重启引导程序来完成此操作
5.  当你回到快速启动模式时，抓取修改后的 boot.img(确保选择正确的一个)并通过快速启动 flash boot boot.img 刷新它
6.  现在重启！您现在应该已经通过 Magisk 获得了 root 权限！

* * *

[**在我们的基本电话论坛**](https://forum.xda-developers.com/essential-phone/development/guide-rooting-essential-ph-1-magisk-t3701976) 查看该指南