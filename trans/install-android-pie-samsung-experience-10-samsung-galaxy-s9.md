# 在 Galaxy S9+上安装带有三星 Experience 10 的早期 Android Pie

> 原文：<https://www.xda-developers.com/install-android-pie-samsung-experience-10-samsung-galaxy-s9/>

# 如何在三星 Galaxy S9+上安装带有三星 Experience 10 的早期 Android Pie Build

基于 Android Pie 的三星 Experience 10 已经泄露为骁龙三星 Galaxy S9+。我们已经设法抓住它，并将向您展示如何安装它。

今天早些时候，我们[发布了](https://www.xda-developers.com/exclusive-this-is-android-pie-with-samsung-experience-10-on-the-samsung-galaxy-s9/)骁龙三星 Galaxy S9+基于 Android 9 Pie 的三星体验 10.0 的第一手操作。我们展示了在快速浏览中可以找到的所有新功能。许多人可能想知道他们如何才能为自己安装这个更新，我们现在有一些说明和文件，你需要在你的三星 Galaxy S9+和高通骁龙 845 上安装 Android Pie。目前，我们只有骁龙三星 Galaxy S9+的版本，但没有骁龙 Galaxy S9 或任何一款 Exynos 型号。我们预计在接下来的几天内会有一个常规的三星 Galaxy S9。然而，没有消息表明三星 Galaxy Note 9 的 Android Pie 版本将于何时推出。

警告:这个版本不稳定。我们不建议安装它，除非你愿意处理一些问题。例如，前置摄像头随着 AR 表情符号一起坏了。新的夜晚主题不能被禁用。更多的功能可能被破坏，我们还没有看到它。除非你对奥丁感到舒服，否则不要安装这个，因为虽然降级到奥利奥是可能的，但这样做并不容易。不要启用最大节电模式。它会让你的手机崩溃，不再开机。

## 如何在骁龙三星 Galaxy S9+上安装三星 Experience 10.0 的 Android Pie

此次更新包括新的 Android Pie 功能，如横向最近应用概述和重新设计的用户界面，重点是圆角。然而，它缺少自适应电池等功能。有一些新的三星体验 10.0 功能，如夜间主题和自定义手势。有些人会喜欢这个更新，而有些人会讨厌它。您可以按照下面的说明在装有高通骁龙 845 的三星 Galaxy S9+上安装第一个 Android Pie 版本。

1.  首先，[下载 Odin 3.13.1](https://forum.xda-developers.com/attachment.php?attachmentid=4446947&d=1521037501) 、 [update.zip](https://firmware.science/download?url=52759/1488/SS-G965USQS3ARI6-to-U3ZRJ9-UP) 、 [Odin 文件](https://androidfilehost.com/?fid=1322778262904016842)。
2.  如果您的手机中有 SD 卡，请将 update.zip 复制到 SD 卡中。如果你没有 SD 卡，跳过这一步。
3.  打开奥丁文件。这个压缩文件将被命名为 G965USQS3ARI6.zip。在奥丁，你会看到 5 个类别，虽然你只会用 4 个。这是一个通用的更新，而不是一个专门为 T-Mobile。不过，它将保留运营商品牌。
4.  通过关闭手机，然后按住电源+音量降低+ Bixby 按钮，将手机置于 Odin 模式。
5.  打开 Odin，放上对应的 BL，AP，CP，HOME_CSC(忽略 CSC)，但是 Userdata 里什么都没有。
6.  点击开始。
7.  你的手机将刷新新的固件，然后重新启动。
8.  在你这样做后，等待大约 5 分钟，然后关闭你的手机，并通过保持电源+音量+ Bixby 重新启动进入恢复状态。
9.  使用音量按钮和电源来选择“从 SD 卡应用更新”如果您没有 SD 卡，请跳至步骤 11。
10.  再次使用音量按钮选择 update.zip 文件，并使用电源按钮选择它。然后更新将开始。更新可能需要 2 到 10 分钟。完成此步骤后，跳到步骤 12。
11.  如果您没有 SD 卡，请使用音量按钮选择“从 adb 应用更新”选项。然后在你的电脑上打开一个命令提示符/终端，输入:

    ```
     adb sideload <file location of update.zip> 
    ```

    然后回车。更新将开始，需要 2 到 10 分钟。
12.  更新完成后，我们建议您恢复出厂设置。这有助于解决稳定性问题。