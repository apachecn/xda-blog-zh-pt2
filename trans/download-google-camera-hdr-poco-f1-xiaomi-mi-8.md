# 为 Poco F1 和 Mi 8 下载带 HDR+和肖像模式的谷歌相机

> 原文：<https://www.xda-developers.com/download-google-camera-hdr-poco-f1-xiaomi-mi-8/>

带有 HDR+的谷歌相机是谷歌 Pixel 智能手机的定义功能之一。它使用计算摄影技术，例如将多达 10 张曝光不足的照片合并成一张更亮的图像。自 Nexus 5 以来，HDR+一直是谷歌智能手机的支柱，但 Pixel 引入零快门延迟(ZSL)使其更受欢迎。谷歌不再正式允许谷歌相机安装在第三方设备上，该公司也不共享 HDR+背后的专有代码。然而，在 2017 年 8 月，具有工作 HDR+的谷歌相机被独立开发者移植到许多设备上。

许多谷歌摄像头端口现在可用于在高通骁龙和 Exynos SoCs 上工作的各种设备。我们做了一个[谷歌摄像头端口集线器](https://www.xda-developers.com/google-camera-port-hub/)，这样用户就可以轻松地为他们的设备下载最稳定的谷歌摄像头端口。

引发这一港口热潮的人被称为 B-S-G，他是一名乌克兰开发者，只在 4PDA(一个俄罗斯论坛)上发帖。4PDA 最近通过众筹向开发者发送了一台小米 Mi 8，开发者现在已经发布了他最新的谷歌相机 5.1.018 端口，可以在 Mi 8 上工作。由于小米 Poco F1 在硬件上与米 8 相似，所以相同的端口在 Poco F1 上工作，尽管缺少几个重要的功能。

小米 8 和 Poco F1 的谷歌相机 5.1.018 端口已经在源链接中链接的 XDA 论坛线程上共享。用户可以安装它们，从他们的 Mi 8 或 Poco F1 相机获得潜在的更好的图像质量。以下功能**在 Poco F1 上发挥作用**:

*   纵向模式(正面和背面)
*   HDR+
*   显像记录

但是，以下功能**在 Poco F1 上不起作用**:

应该注意的是，许多小米设备没有启用 Camera2 API，而这是谷歌相机端口工作所必需的。感谢 Poco F1 用户，[所有搭载高通骁龙 845 或骁龙 710 的小米设备都启用了 camera 2 API](https://www.xda-developers.com/google-camera-port-xiaomi-poco-f1-xiaomi-mi-8-se-ee-xiaomi-mi-mix-2s/)。这意味着他们不需要解锁他们的引导加载程序和修改任何文件(这通常需要 root)。

XDA 撰稿人 [Kishan Vyas](https://www.xda-developers.com/author/kristinspradlin/) 在他的 Poco F1 赛车上试用了谷歌相机端口，下面展示了他拍摄的一些快速图像样本。他观察到他的手机端口滞后，因为按下快门按钮后需要 10-15 秒才能拍照。它在几次拍摄中运行良好，但随后稳定性变差。还应该注意的是，用户不能在 HDR+开关关闭的情况下拍照。

* * *

[**为小米 Mi 8 和 Poco F1** 下载谷歌摄像头端口 ](https://forum.xda-developers.com/poco-f1/themes/b-s-g-google-camera-port-developed-mi-8-t3843130)