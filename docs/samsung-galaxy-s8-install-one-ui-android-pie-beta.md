# 在骁龙三星 Galaxy S8 上安装一个 UI Android Pie beta

> 原文：<https://www.xda-developers.com/samsung-galaxy-s8-install-one-ui-android-pie-beta/>

# 如何在骁龙三星 Galaxy S8 上安装 One UI 封闭 Android Pie beta

想在你的骁龙三星 Galaxy S8 上试用一个 UI (Android Pie)吗？我们将向您展示如何在 Galaxy S8 上早期安装封闭测试版！

在过去的几天里，我们已经发布了关于为三星 Galaxy S8+和三星 Galaxy Note 8 的骁龙版本提供 One UI 封闭 Android Pie 测试版的消息。现在，骁龙三星 Galaxy S8 已经有了更新。下面是我们关于如何在自己的 Galaxy S8 上安装它的教程。我们听说其他 Galaxy 8+/Galaxy Note 8 系列测试版运行得相当好，但它们并不完美。请记住，如果你正在安装它，你这样做是在你自己的风险。Galaxy S8/Galaxy Note 8 的新功能包括智能扫描、使用耳机时的杜比全景声和全屏手势。

2019 年 1 月 3 日更新:这篇文章增加了一个新版本。build，DRL7，自带 2019 年 1 月的安全补丁级别。还有一个新的 AT & T 启动动画和相机应用中的场景优化开关。锁屏下拉延迟似乎也被修复了。

如果你有骁龙三星 Galaxy S8+，那么我们的教程是[这里](https://www.xda-developers.com/samsung-galaxy-s8-snapdragon-install-closed-one-ui-android-pie-beta/)。如果你有骁龙三星 Galaxy Note 8，那么我们针对该设备的教程是[这里](https://www.xda-developers.com/samsung-galaxy-note-8-install-one-ui-android-pie-beta/)。

## 如何在骁龙三星 Galaxy S8 上安装 One UI 封闭的 Android Pie beta

我在下面嵌入的视频将带你完成使用修改后的 Odin 安装一个 UI 的过程；我在视频中使用的是三星 Galaxy Note 9 和三星 Galaxy S9+,它们有官方的 One UI 测试版，但只要你替换正确的文件，同样的过程也适用于 Galaxy S8。

1.  首先你需要下载 [Odin 3.13.1](https://forum.xda-developers.com/attachment.php?attachmentid=4446947&d=1521037501) ，CRK1 到 CRL1 的 [update.zip，CRL1 到 DRL7](https://firmware.science/download?url=48927/1488/SS-G950USQU5CRK1-to-S5CRL1-UP) 的 [update.zip，以及](https://firmware.science/download?url=48927/1488/SS-G950USQS5CRL1-to-U5DRL7-UP) [CRK1](https://updato.com/firmware-archive-select-model?record=56E68A0DFB3F11E89F15FA163EE8F90B) [Odin 文件](https://updato.com/firmware-archive-select-model?record=56E68A0DFB3F11E89F15FA163EE8F90B)。
2.  如果您的三星 Galaxy S8 中有 SD 卡，请将 update.zip 复制到 SD 卡中。如果你没有 SD 卡，跳过这一步。
3.  在名为 SM-G950U _ 1 _ 20181108104414 _ f9mqimhcmz _ fac . zip 的 zip 中包含的 Odin 文件中，您会看到六个文件。奥丁有 5 个类别，但只有 4 个将被使用。
4.  关闭三星 Galaxy S8，然后按住电源+音量降低 Bixby 按钮，让它进入 Odin 模式。
5.  现在打开 Odin，点击 BL、AP、CP、HOME_CSC，然后从之前解压的 ZIP 中选择相应的文件。不要在用户数据中放任何东西。这可能会删除你 Galaxy S8 上的所有数据。
6.  单击开始。
7.  Odin 会把新固件更新到你的三星 Galaxy S8 上。
8.  等待 5 到 10 分钟安装更新。一旦这样做了，关闭你的手机，然后通过保持电源+ Bixby +音量重新启动恢复。
9.  现在使用 CRK1 至 CRL1 OTA 进行更新。
10.  使用音量和电源按钮，选择“应用来自 SD 卡的更新”如果您没有 SD 卡，请跳至步骤 12。
11.  使用音量按钮选择 update.zip 文件，使用电源按钮选择该文件。然后更新将开始。更新可能需要 2 到 10 分钟。完成此步骤后，跳到步骤 13。
12.  如果您没有 SD 卡，请使用音量按钮选择“应用来自 [adb](https://www.xda-developers.com/install-adb-windows-macos-linux/) 的更新”选项。在你的电脑上打开命令提示符，键入:

    ```
     <span >adb sideload </span><span ><</span><span >file location of update</span><span >.</span><span >zip</span><span >></span> 
    ```

    并按回车键。更新将开始，大约需要 2 到 10 分钟。
13.  现在使用 CRL1 至 DRL5 OTA 进行更新。
14.  使用音量按钮和电源来选择“从 SD 卡应用更新”如果您没有 SD 卡，请跳至步骤 12。
15.  再次使用音量按钮选择 update.zip 文件，并使用电源按钮选择它。然后更新将开始。更新可能需要 2 到 10 分钟。完成此步骤后，跳到步骤 13。
16.  如果您没有 SD 卡，请使用音量按钮选择“应用来自 [adb](https://www.xda-developers.com/install-adb-windows-macos-linux/) 的更新”选项。然后在你的电脑上打开一个命令提示符/终端，输入:

    ```
     <span >adb sideload </span><span ><</span><span >file location of update</span><span >.</span><span >zip</span><span >></span> 
    ```

    然后回车。更新将开始，大约需要 2 到 10 分钟。
17.  重启手机，享受 One UI 测试版。

[**三星 Galaxy S8 论坛**](https://forum.xda-developers.com/galaxy-s8)

如果你想了解更多关于三星最新的 One UI 软件，我们建议查看[我们的完整评论](https://www.xda-developers.com/samsung-one-ui-review-android-pie-galaxy-s9-galaxy-note-9/)或者在我们的 XDA 电视 YouTube 频道上观看我们的[视频评论。](https://www.youtube.com/watch?v=tKJkUM18oK4)