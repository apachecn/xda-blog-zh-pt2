# 如何为骁龙三星 Galaxy Note 8 安装一个 UI beta

> 原文：<https://www.xda-developers.com/samsung-galaxy-note-8-install-one-ui-android-pie-beta/>

# 如何为骁龙三星 Galaxy Note 8 安装 One UI 封闭测试版

Android Pie 上面有一个分层的 UI 可供下载，我们将向您展示如何在骁龙三星 Galaxy Note 8 上安装它。

如果你碰巧拥有三星 Galaxy Note 8，并且觉得自己错过了最新的功能，我们有一些好消息。昨天，我们[发布了](https://www.xda-developers.com/samsung-galaxy-note-8-one-ui-beta-android-pie-leak/)关于 Android Pie 的封闭测试版，其中一个 UI 层叠在 Galaxy Note 8 的 Snapdragon 835 型号之上。我们现在将向您展示如何在骁龙三星 Galaxy Note 8 上安装它。这一更新已经适用于 Galaxy S9、Galaxy S9+和 Galaxy Note 9。

2019 年 1 月 3 日更新:这篇文章增加了一个新版本。build，DRL7，自带 2019 年 1 月的安全补丁级别。还有一个新的 AT & T 启动动画和相机应用中的场景优化开关。锁屏下拉延迟似乎也被修复了。

## 如何在三星 Galaxy Note 8 上安装封闭 beta One UI (Android Pie)

下面的视频将引导您完成安装一个用户界面的过程。我在视频中使用的是 Galaxy Note 9 和 Galaxy S9+,但只要你用下面链接的文件替换骁龙 Galaxy Note 8，这个过程就可以工作。

1.  首先，[下载 Odin 3.13.1](https://forum.xda-developers.com/attachment.php?attachmentid=4446947&d=1521037501) ，CRK1 到 DRL7 的 [update.zip，](https://firmware.science/download?url=48993/1488/SS-N950USQS5CRK1-to-U5DRL7-UP) [CRK1](https://updato.com/firmware-archive-select-model?record=8BBD7C25032511E99F15FA163EE8F90B) [Odin 文件](https://updato.com/firmware-archive-select-model?record=8BBD7C25032511E99F15FA163EE8F90B)。
2.  如果你的 Galaxy Note 8 中有 SD 卡，请将 update.zip 复制到 SD 卡中。如果你没有 SD 卡，跳过这一步。
3.  打开奥丁文件。该压缩文件将被命名为 SM-N950U _ 1 _ 20181126150901 _ oux wmh 265 r _ fac . zip，在其中，您将看到六个文件。在奥丁，你会看到 5 个类别，虽然你只会用 4 个。
4.  关闭三星 Galaxy Note 8，然后按住电源+音量降低+ Bixby 按钮，将它置于 Odin 模式。
5.  打开 Odin，选择对应的 BL，AP，CP，HOME_CSC，但是 Userdata 里什么都没有。这可能会清除你手机上的所有数据。
6.  点击开始。
7.  你的手机将刷新新的固件，然后重新启动。
8.  在你这样做后，等待大约 5 分钟，然后关闭你的手机，并通过保持电源+音量+ Bixby 重新启动进入恢复状态。
9.  现在使用 CRK1 至 DRL6 OTA 进行更新。
10.  使用音量按钮和电源来选择“从 SD 卡应用更新”如果您没有 SD 卡，请跳至步骤 12。
11.  再次使用音量按钮选择 update.zip 文件，并使用电源按钮选择它。然后更新将开始。更新可能需要 2 到 10 分钟。完成此步骤后，跳到步骤 13。
12.  如果您没有 SD 卡，请使用音量按钮选择“应用来自 [adb](https://www.xda-developers.com/install-adb-windows-macos-linux/) 的更新”选项。然后在你的电脑上打开一个命令提示符/终端，输入:

    ```
     <span >adb sideload </span><span ><</span><span >file location of update</span><span >.</span><span >zip</span><span >></span> 
    ```

    然后回车。更新将开始，需要 2 到 10 分钟。
13.  重启手机，享受 One UI 测试版。

[**三星 Galaxy Note 8 XDA 论坛**](https://forum.xda-developers.com/galaxy-note-8)

如果你想了解更多关于一个 UI 的信息，你可以[阅读我们的完整评论](https://www.xda-developers.com/samsung-one-ui-review-android-pie-galaxy-s9-galaxy-note-9/)或者在 XDA 电视台观看[的视频。](https://www.youtube.com/watch?v=tKJkUM18oK4)