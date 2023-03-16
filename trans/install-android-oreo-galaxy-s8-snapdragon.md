# 骁龙 Galaxy S8 和 S8+如何安装安卓奥利奥

> 原文：<https://www.xda-developers.com/install-android-oreo-galaxy-s8-snapdragon/>

# 骁龙 Galaxy S8 和 S8+如何安装安卓官方奥利奥

三星 Galaxy S8 和 S8+的官方 Android Oreo 更新现已推出。如果你想现在安装它，你可以按照这个指南。

经过数月的等待，威瑞森终于发布了 Galaxy S8 和 S8+的 Android Oreo 更新。这个版本还没有被任何其他运营商正式推出，但他们应该很快就会推出更新。

这些更新适用于 Galaxy S8 和 S8+的骁龙版本。这款手机的 [Exynos 变体](https://www.xda-developers.com/how-to-install-android-oreo-on-the-samsung-galaxy-s8-s8-exynos/)已经[收到了安卓奥利奥](https://www.xda-developers.com/samsung-galaxy-s8-android-oreo-project-treble/)。该更新已在 Play Store 获得认证，并通过了[安全网](https://redirect.viglink.com/?format=go&jsonp=vglnk_152117465287212&key=c253a561fbe84b0cd1cd9012f5136c6e&libId=jetg3ymj0102gzl9000DAn4en2yfn&loc=https%3A%2F%2Fwww.xda-developers.com%2Fsamsung-galaxy-note8-android-oreo-update%2F&v=1&out=https%3A%2F%2Fforum.xda-developers.com%2Fapps%2Fmagisk%2Fguide-magisk-troubleshooting-t3641417%2Fpost73145987%23post73145987&ref=https%3A%2F%2Fwww.xda-developers.com%2Fauthor%2Fmweinbach%2F&title=Official%20Samsung%20Galaxy%20Note%208%20Android%20Oreo%20Update%20Rolling%20Out%20Soon%20As%20Beta%20Builds%20Pass%20SafetyNet&txt=SafetyNet)。该版本包括 2 月份的安全补丁和 Android Oreo 的典型功能，如[通知通道](https://www.xda-developers.com/notification-importance-controls-all-apps-android-oreo/)、[画中画模式](https://www.xda-developers.com/picture-in-picture-mode-desktop-google-chrome/)、[通知休眠](https://www.xda-developers.com/customize-notification-snooze-duration-android-oreo/)、[后台应用优化](https://www.xda-developers.com/android-oreo-oem-background-app-limitations/)等等。正如你所料，三星 Experience 9.0 也有很多三星特有的变化。

此更新应该很快就可以使用，但如果你想现在安装它，你可以按照下面的指南。

### 如何将 Galaxy S8 和 S8+更新到 Android Oreo:

1.  检查你手机的型号，看看它是 **G950U** 还是 **G955U** 。
2.  你需要下载 S8 的 [BRB1 Odin 和 S8](https://androidfilehost.com/?fid=818070582850498730) 的[更新，S8+](https://samsung.firmware.science/download?url=48927/1488/SS-G950USQS2BRB1-to-U2CRB9-UP) 的 [BRB1 Odin 和 S8+](https://androidfilehost.com/?fid=890129502657588932) 的[更新。](https://samsung.firmware.science/download?url=48926/1488/SS-G955USQS2BRB1-to-U2CRB9-UP)
3.  将 OTA 文件复制到手机的 SD 卡上。如果你没有 SD 卡，你可以跳过这一步，但你仍然需要在你的电脑上的 OTA 文件。提取之前链接的 Odin 固件。这将是一个压缩格式。
4.  通过关闭设备电源，然后按住 Bixby 按钮+音量降低+电源，重新启动设备进入下载模式
5.  下载 [Odin 工具](https://forum.xda-developers.com/attachment.php?attachmentid=4431749&d=1519672710)，将手机插上电脑。Odin 是三星的官方工具，可以将三星官方固件闪存到三星 Galaxy 设备上。在右边的奥丁中，你会看到 5 个部分，但是只有 3 个会用到。
6.  单击 BL 按钮并导航到您提取文件的 Odin 固件文件夹，然后单击以 BL 开头的文件。对 AP 和 CP 做同样的事情。
7.  点击奥丁底部的开始。
8.  等待您的设备刷新，然后重新启动。一旦重启，再次关闭你的手机。然后，通过按住 Bixby 按钮+音量增大+电源再次启动恢复。
9.  如果您有 SD 卡，请选择“从 SD 卡应用更新”您可以使用音量摇杆进行导航，使用电源按钮进行选择。选择选项后，找到名为“update.zip”的文件，用电源键选择。
10.  如果您没有 SD 卡，请选择“从 ADB 应用更新”在您的计算机上，通过按 Windows 键+ R 并键入“cmd”来打开命令提示符这个命令提示符打开后，键入“adb sideload”并按回车键。如果您还没有设置 ADB，您可以按照这些快速说明来加快速度。