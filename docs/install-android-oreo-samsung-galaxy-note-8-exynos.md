# 如何在 Exynos 三星 Galaxy Note 8 上安装安卓奥利奥

> 原文：<https://www.xda-developers.com/install-android-oreo-samsung-galaxy-note-8-exynos/>

经过漫长的等待，三星终于发布了 Exynos 三星 Galaxy Note 8 的官方 [Android Oreo](https://www.xda-developers.com/tag/android-oreo/) 更新。这就推给了法国 Galaxy Note 8 机型。

这是 Galaxy Note 8 的新版本，还没有像骁龙版本的手机那样泄露。此次更新是在 Android Oreo 所有新功能的基础上推出的 3 月安全补丁，如[画中画模式](https://www.xda-developers.com/picture-in-picture-mode-desktop-google-chrome/)、[通知频道](https://www.xda-developers.com/notification-importance-controls-all-apps-android-oreo/)、[后台应用优化](https://www.xda-developers.com/android-oreo-oem-background-app-limitations/)、[通知休眠](https://www.xda-developers.com/customize-notification-snooze-duration-android-oreo/)等等。在[三星体验 9.0](https://www.xda-developers.com/samsung-experience-9-0-beta-android-oreo-features/) 中也有很多三星特有的变化。

这一更新可能会在未来几天甚至几周内推出，因此遵循本教程将确保您可以立即将您的设备升级到最新的 Android Oreo 版本。本教程将适用于除韩国 Exynos 用户之外的几乎所有 Exynos Galaxy Note 8 设备。

## 如何在 Exynos 三星 Galaxy Note 8 上安装安卓奥利奥

1.检查你的手机型号，看看是不是 N950F。如果不是，**不要继续，因为这可能会损坏您的手机**。

2.为 Note 8 下载 [CRC1 Odin](https://www.androidfilehost.com/?fid=818070582850501773) 文件。

3.提取之前链接的 Odin 固件。这将是一个压缩格式。

4.通过关闭您的设备，然后按住 Bixby 按钮+音量降低+电源，重新启动您的设备进入下载模式。

5.下载 [Odin 工具](https://forum.xda-developers.com/attachment.php?attachmentid=4431749&d=1519672710)，将手机插上电脑。Odin 是三星的官方工具，可以将三星官方固件闪存到三星 Galaxy 设备上。在右边的奥丁中，你会看到 5 个部分，但是其中只有 4 个会被使用。

6.点击 BL 按钮，导航到你解压文件的 Odin 固件文件夹，然后点击以 BL 开头的文件。对 AP、CP 和 HOME_CSC 做同样的事情(不要用 CSC_XXX。它将删除您的数据)

6.点击开始！之后，它会启动和闪烁，然后它会重新启动，你就好了！