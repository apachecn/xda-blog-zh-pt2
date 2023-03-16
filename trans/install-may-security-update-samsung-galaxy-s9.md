# 如何在骁龙 Galaxy S9/S9+上安装 May 安全更新

> 原文：<https://www.xda-developers.com/install-may-security-update-samsung-galaxy-s9/>

# 如何在骁龙 Galaxy S9/S9+上安装 May 安全更新

本指南中的更新适用于 Galaxy S9 和 S9+的骁龙版本。这个版本包括 5 月的安全补丁和错误修复，尽管我们不知道任何特定的错误被修复。

三星 Galaxy S9 和 S9+已经上市一个多月了。自第一天更新以来，三星和运营商尚未发布手机更新。几乎每台骁龙 Galaxy S9 和 S9+仍在运行 2 月份发布的安全补丁。

本指南中的更新适用于 Galaxy S9 和 S9+的骁龙版本。这款手机的 Exynos 变种已经收到了 3 月份的安全更新，但除此之外没有别的了。该更新尚未在 Play Store 中得到认证，也没有通过 SafteyNet，但当我在自己的设备上运行该更新时，Google Pay 和所有谷歌应用程序仍在工作。这个版本包括 5 月的安全补丁和错误修复，尽管我们不知道任何特定的错误被修复。这次更新还为 AT & T 用户增加了聊天机器人。

### 如何将 Galaxy S9 和 S9+更新到 5 月安全补丁:

1.  检查你的手机型号，看看它是 G960U 还是 G965U。
2.  你需要下载 S9 的 [ARC6 Odin 和 S9](https://www.androidfilehost.com/?fid=962187416754478442) 的[更新以及 S9+](https://firmware.science/download?url=52758/1488/SS-G960USQU2ARC6-to-U2ARDA-UP) 的 [ARC6 Odin 和 S9+](https://www.androidfilehost.com/?fid=746163614322262254) 的[更新。](https://firmware.science/download?url=52759/1488/SS-G965USQU2ARC6-to-U2ARDA-UP)
3.  将 OTA 文件复制到手机的 SD 卡上。如果你没有 SD 卡，你可以跳过这一步，但你仍然需要在你的电脑上的 OTA 文件。提取之前链接的 Odin 固件。这将是一个压缩格式。
4.  确保在你继续禁用你的设备上的所有底层主题。安装更新后，您将能够重新启用它们。
5.  通过关闭设备电源，然后按住 Bixby 按钮+音量降低+电源，重新启动设备进入下载模式
6.  下载 [Odin 工具](https://forum.xda-developers.com/attachment.php?attachmentid=4431749&d=1519672710)，将手机插上电脑。Odin 是三星的官方工具，可以将三星官方固件闪存到三星 Galaxy 设备上。在右边的奥丁中，你会看到 5 个部分，但是其中只有 4 个会被使用。
7.  单击 BL 按钮并导航到您提取文件的 Odin 固件文件夹，然后单击以 BL 开头的文件。对 AP 和 CP 以及 HOME_CSC 做同样的事情，**不要使用 CSC_OYN，因为这会擦除你手机上的所有数据。**。
8.  点击奥丁底部的开始。
9.  等待您的设备刷新，然后重新启动。一旦重启，再次关闭你的手机。然后，通过按住 Bixby 按钮+音量增大+电源再次启动恢复。
10.  如果您有 SD 卡，请选择“从 SD 卡应用更新”您可以使用音量摇杆进行导航，使用电源按钮进行选择。选择选项后，找到名为“update.zip”的文件，用电源键选择。
11.  如果您没有 SD 卡，请选择“从 ADB 应用更新”在您的计算机上，通过按 Windows 键+ R 并键入“cmd”来打开命令提示符这个命令提示符打开后，键入“adb sideload”并按回车键。如果你还没有安装 ADB，你可以按照这些快速的说明来快速上手。