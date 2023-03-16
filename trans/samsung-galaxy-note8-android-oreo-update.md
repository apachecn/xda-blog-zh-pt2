# 三星官方 Galaxy Note 8 Android Oreo 更新即将推出，因为 Beta 版构建了 Pass SafetyNet

> 原文：<https://www.xda-developers.com/samsung-galaxy-note8-android-oreo-update/>

# 三星官方 Galaxy Note 8 Android Oreo 更新即将推出，因为 Beta 版构建了 Pass SafetyNet

虽然三星 Galaxy S8/S8+和 Galaxy S9/S9+有 Android Oreo，但三星 Galaxy Note8 尚未收到它。这可能很快就会改变，因为为 Note8 构建的测试版奥利奥现在通过了 SafetyNet，标志着即将发布。

经过[多个月的等待](https://www.xda-developers.com/galaxy-note-8-exynos-oreo-firmware-leak/)，三星终于发布了 Galaxy Note 8 的 Android Oreo 更新。这个版本还没有被三星官方推出，但是已经发布到了 AT & T 的服务器上。它已经得到了谷歌的官方认证，并通过了安全网兼容性，这意味着像[谷歌支付](https://www.xda-developers.com/google-pay-android-pay-google-wallet/)这样的应用程序现在可以工作了。

此次更新是针对 Galaxy Note 8 的**骁龙版本**。这是第一款在 Play Store 获得认证并通过 SafetyNet 的产品。这个版本也是对 Android Oreo 所有新功能的更新，如[画中画模式](https://www.xda-developers.com/picture-in-picture-mode-desktop-google-chrome/)、[通知频道](https://www.xda-developers.com/notification-importance-controls-all-apps-android-oreo/)、[通知休眠](https://www.xda-developers.com/customize-notification-snooze-duration-android-oreo/)、[后台应用优化](https://www.xda-developers.com/android-oreo-oem-background-app-limitations/)等等。在[三星体验 9.0](https://www.xda-developers.com/samsung-experience-9-0-beta-android-oreo-features/) 中也有很多三星特有的变化。三月份的安全补丁也包含在更新中。

这个版本可能很快就会被运营商推出。如果您不想等待运营商发布更新，您可以按照下面的说明手动安装。

## 如何将 Galaxy Note 8 更新到 Android 奥利奥:

1.  检查你手机的型号，看看它是 N950U 还是 T2 的 N950U。如果您的型号是 N950U1，那么在使用手机时，您将拥有**运营商应用程序和开机动画。**
2.  你需要下载 [BRA8 Odin](https://androidfilehost.com/?fid=746010030569950432) 和 [update.zip](https://firmware.science/download?url=48993/1488/SS-N950USQS3BRA8-to-U3CRC2-UP)
3.  将 OTA 文件复制到手机的 SD 卡上。如果你没有 SD 卡，你可以跳过这一步，但你仍然需要在你的电脑上的 OTA 文件。
4.  提取之前链接的 Odin 固件。这将是一个压缩格式。
5.  关闭设备电源，然后按住 **Bixby 按钮+音量降低+电源**，重新启动设备进入下载模式
6.  下载 [Odin](https://androidfilehost.com/?fid=673956719939824171) 工具，将手机插上电脑。Odin 是三星的官方工具，可以将三星官方固件闪存到三星 Galaxy 设备上。在右边的奥丁中，你会看到 5 个部分，但是只有 3 个会用到。
7.  单击 BL 按钮并导航到您提取文件的 Odin 固件文件夹，然后单击以 BL 开头的文件。对 AP 和 CP 做同样的事情。8.点击 Odin.9 底部的**开始**等你的设备闪一下再重启。一旦重启，再次关闭你的手机。然后，通过按住 **Bixby 按钮+音量增大+电源**，再次启动进入恢复模式。如果您有 SD 卡，请选择“从 SD 卡应用更新”您可以使用音量摇杆进行导航，使用电源按钮进行选择。选择选项后，找到名为“update.zip”的文件，用电源按钮选择它。11 .如果您没有 SD 卡，请选择“应用 ADB 的更新”在您的计算机上，通过按 Windows 键+ R 并键入“cmd”来打开命令提示符这个命令提示符打开后，键入“adb sideload”并按回车键。如果你还没有设置 ADB，你可以按照[这些快速指令](https://www.xda-developers.com/install-adb-windows-macos-linux)来加快速度。