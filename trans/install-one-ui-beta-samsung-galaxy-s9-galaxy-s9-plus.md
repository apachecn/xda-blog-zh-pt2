# 如何在三星 Galaxy S9 和 Galaxy S9+上安装 One UI beta

> 原文：<https://www.xda-developers.com/install-one-ui-beta-samsung-galaxy-s9-galaxy-s9-plus/>

# 如何在三星 Galaxy S9 和 Galaxy S9+上安装 One UI beta

感谢 XDA 资深会员 SoLdieR9312，我们现在有了 Exynos 手机的 OTA 以及骁龙手机的 firmware.science。

三星 One UI 概述。来源:三星

三星最近为 Exynos 三星 Galaxy S9 和 Galaxy S9+推出了他们最新的 [One UI beta](https://www.xda-developers.com/one-ui-beta-android-pie-samsung-galaxy-s9/) 。 [One UI](https://www.xda-developers.com/samsung-one-ui-android-pie-galaxy-s9-galaxy-note-9/) 是三星最新版本的三星体验，正式名称为 TouchWiz，基于 Android Pie。这个测试版在德国、韩国和美国推出。美国要幸运一些，所有骁龙 Galaxy S9 系列设备的版本都已经泄露了。

多亏了 XDA 资深成员 soldier 9312 T1，我们现在有了 Exynos 手机的 OTA 以及骁龙手机的 firmware.science。如果您安装这些更新，您将不会从您的运营商或 Samsung 收到 OTA 更新。

这是 XDA 电视 YouTube 频道上的一个视频，展示了如何在您的设备上安装 OneUI 测试版。使用以下文件和视频的下载链接获取说明。

# Exynos 型号:

1.  首先，[下载 Odin 3.13.1](https://forum.xda-developers.com/attachment.php?attachmentid=4446947&d=1521037501) ，[brj 6 到 ZRKA](https://mega.nz/#!gERiSKZD!jJx6Bxm1GRYiXSC0tdcyH-kc76FBq-M3dIQq3SzeojE) 的 update.zip， [BRJ6](https://www.sammobile.com/firmwares/galaxy-s9/SM-G960F/BTU/download/G960FXXS2BRJ6/243085/) [Odin 文件](https://www.sammobile.com/firmwares/galaxy-s9/SM-G960F/BTU/download/G960FXXS2BRJ6/243085/)。
2.  如果您的 Galaxy S9 中有 SD 卡，请将 update.zip 复制到 SD 卡中。如果你没有 SD 卡，跳过这一步。
3.  打开奥丁文件。该 zip 文件将被命名为 SM-G960F _ 1 _ 20181031161553 _ 2 yj 261 n7q 7 _ fac . zip。在该文件中，您将看到六个文件。在奥丁，你会看到 5 个类别，虽然你只会用 4 个。
4.  关闭 Galaxy S9，然后按住 Power + Volume Down + Bixby 按钮，将它置于 Odin 模式。
5.  打开 Odin，放上对应的 BL，AP，CP，HOME_CSC，但是 Userdata 里什么都没有。这可能会清除你手机上的所有数据。
6.  点击开始。
7.  你的手机将刷新新的固件，然后重新启动。
8.  在你这样做后，等待大约 5 分钟，然后关闭你的手机，并通过保持电源+音量+ Bixby 重新启动进入恢复状态。
9.  现在使用 BRJ6 到 ZRKA OTA 进行此更新。
10.  使用音量按钮和电源来选择“从 SD 卡应用更新”如果您没有 SD 卡，请跳至步骤 12。
11.  再次使用音量按钮选择 update.zip 文件，并使用电源按钮选择它。然后更新将开始。更新可能需要 2 到 10 分钟。完成此步骤后，跳到步骤 13。
12.  如果您没有 SD 卡，请使用音量按钮选择“应用来自 [adb](https://www.xda-developers.com/install-adb-windows-macos-linux/) 的更新”选项。然后在你的电脑上打开一个命令提示符/终端，输入:

    ```
     <span >adb sideload </span><span ><</span><span >file location of update</span><span >.</span><span >zip</span><span >></span> 
    ```

    然后回车。更新将开始，需要 2 到 10 分钟。
13.  重启手机，享受 One UI 测试版。

1.  首先，[下载 Odin 3.13.1](https://forum.xda-developers.com/attachment.php?attachmentid=4446947&d=1521037501) ，【BRJ6 到 ZRKA 的 update.zip， [Odin 文件](https://androidfilehost.com/?fid=11410963190603845166)。
2.  如果您的 Galaxy S9+中有 SD 卡，请将 update.zip 复制到 SD 卡中。如果你没有 SD 卡，跳过这一步。
3.  打开奥丁文件。这个压缩文件将被命名为 G965FXXS2BRJ6.zip。在奥丁，你会看到 5 个类别，虽然你只会用 4 个。
4.  关闭 Galaxy S9+进入 Odin 模式，然后按住电源+音量降低+ Bixby 按钮。
5.  打开 Odin，放上对应的 BL，AP，CP，HOME_CSC，但是 Userdata 里什么都没有。这可能会清除你手机上的所有数据。
6.  点击开始。
7.  你的 Galaxy 手机会刷新新固件，然后重启。
8.  在你这样做后，等待大约 5 分钟，然后关闭你的手机，并通过保持电源+音量+ Bixby 重新启动进入恢复状态。
9.  现在使用 BRJ6 到 ZRKA OTA 进行此更新。
10.  使用音量按钮和电源来选择“从 SD 卡应用更新”如果您没有 SD 卡，请跳至步骤 12。
11.  再次使用音量按钮选择 update.zip 文件，并使用电源按钮选择它。然后更新将开始。更新可能需要 2 到 10 分钟。完成此步骤后，跳到步骤 13。
12.  如果您没有 SD 卡，请使用音量按钮选择“应用来自 [adb](https://www.xda-developers.com/install-adb-windows-macos-linux/) 的更新”选项。然后在你的电脑上打开一个命令提示符/终端，输入:

    ```
     <span >adb sideload </span><span ><</span><span >file location of update</span><span >.</span><span >zip</span><span >></span> 
    ```

    然后回车。更新将开始，需要 2 到 10 分钟。
13.  重启你的手机，享受一个用户界面。

# 骁龙车型:

1.  首先，[下载 Odin 3.13.1](https://forum.xda-developers.com/attachment.php?attachmentid=4446947&d=1521037501) 、U3BRJ5-to-U3CRKE 的 [update.zip、](https://firmware.science/download?url=52758/1488/SS-G960USQU3BRJ5-to-U3CRKE-UP)[Odin 文件](https://www.sammobile.com/firmwares/galaxy-s9/SM-G960U/VZW/download/G960USQU3BRJ5/242654/)。
2.  如果您的 Galaxy S9 中有 SD 卡，请将 update.zip 复制到 SD 卡中。如果你没有 SD 卡，跳过这一步。
3.  打开奥丁文件。这个压缩文件将被命名为 g 960 usqu 3 brj 5 _ g 960 uoyn 3 brj 5 _ vzw . zip。在奥丁，你会看到 5 个类别，虽然你只会用 4 个。
4.  关闭 Galaxy S9，然后按住 Power + Volume Down + Bixby 按钮，将它置于 Odin 模式。
5.  打开 Odin，放上对应的 BL，AP，CP，HOME_CSC，但是 Userdata 里什么都没有。这可能会清除你手机上的所有数据。
6.  点击开始。
7.  您的 Galaxy S9 将刷新新固件，然后重新启动。
8.  在你这样做后，等待大约 5 分钟，然后关闭你的手机，并通过保持电源+音量+ Bixby 重新启动进入恢复状态。
9.  现在使用 update.zip OTA 进行更新。
10.  使用音量按钮和电源来选择“从 SD 卡应用更新”如果您没有 SD 卡，请跳至步骤 12。
11.  再次使用音量按钮选择 update.zip 文件，并使用电源按钮选择它。然后更新将开始。更新可能需要 2 到 10 分钟。完成此步骤后，跳到步骤 13。
12.  如果您没有 SD 卡，请使用音量按钮选择“应用来自 [adb](https://www.xda-developers.com/install-adb-windows-macos-linux/) 的更新”选项。然后在你的电脑上打开一个命令提示符/终端，输入:

    ```
     <span >adb sideload </span><span ><</span><span >file location of update</span><span >.</span><span >zip</span><span >></span> 
    ```

    然后回车。更新将开始，需要 2 到 10 分钟。
13.  重启你的手机，享受一个用户界面。

1.  首先，[下载 Odin 3.13.1](https://forum.xda-developers.com/attachment.php?attachmentid=4446947&d=1521037501) ，[u3brj 5 到 U3ZRKJ](https://firmware.science/download?url=52759/1488/SS-G965USQU3BRJ5-to-U3ZRKJ-UP) 的 update.zip， [Odin 文件](https://androidfilehost.com/?fid=11410963190603841817)。
2.  如果您的 Galaxy S9+中有 SD 卡，请将 update.zip 复制到 SD 卡中。如果你没有 SD 卡，跳过这一步。
3.  打开奥丁文件。这个压缩文件将被命名为 G965USQU3BRJ5.zip。在奥丁，你会看到 5 个类别，虽然你只会用 4 个。
4.  关闭 Galaxy S9+进入 Odin 模式，然后按住电源+音量降低+ Bixby 按钮。
5.  打开 Odin，放上对应的 BL，AP，CP，HOME_CSC，但是 Userdata 里什么都没有。这可能会清除你手机上的所有数据。
6.  点击开始。
7.  您的 Galaxy S9+将刷新新固件，然后重新启动。
8.  在你这样做后，等待大约 5 分钟，然后关闭你的手机，并通过保持电源+音量+ Bixby 重新启动进入恢复状态。
9.  现在使用 update.zip 进行更新。
10.  使用音量按钮和电源来选择“从 SD 卡应用更新”如果您没有 SD 卡，请跳至步骤 12。
11.  再次使用音量按钮选择 update.zip 文件，并使用电源按钮选择它。然后更新将开始。更新可能需要 2 到 10 分钟。完成此步骤后，跳到步骤 13。
12.  如果您没有 SD 卡，请使用音量按钮选择“应用来自 [adb](https://www.xda-developers.com/install-adb-windows-macos-linux/) 的更新”选项。然后在你的电脑上打开一个命令提示符/终端，输入:

    ```
     <span >adb sideload </span><span ><</span><span >file location of update</span><span >.</span><span >zip</span><span >></span> 
    ```

    然后回车。更新将开始，需要 2 到 10 分钟。
13.  重启你的手机，享受一个用户界面。

[**银河 S9 论坛**](https://forum.xda-developers.com/galaxy-s9) [**银河 S9+论坛**](https://forum.xda-developers.com/galaxy-s9-plus)