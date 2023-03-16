# 在 Galaxy Note 9 上安装测试版三星 Experience 10 (Android Pie)

> 原文：<https://www.xda-developers.com/install-early-android-pie-samsung-experience-10-snapdragon-samsung-galaxy-note-9/>

# 如何在骁龙三星 Galaxy Note 9 上安装带有三星 Experience 10 的早期 Android Pie build

这是三星 Galaxy Note 9 的三星 Experience 10(基于 Android Pie)的早期测试版，以及如何将其安装在骁龙 Galaxy Note 9 上。

基于 Android Pie 的三星 Experience 10 早期预发布版本现已适用于骁龙三星 Galaxy Note 9。我们已经展示了我们在 Galaxy S9 的[快速浏览](https://www.xda-developers.com/early-samsung-experience-10-android-pie-samsung-galaxy-note-9/)和[早期视频中可以找到的所有新功能。如果你想在你自己的 Galaxy Note 9 上安装这个早期的 Android Pie 版本，我们现在有你需要为三星 Galaxy Note 9 安装早期三星 Experience 10 的说明和文件，前提是你有高通骁龙 845 的型号。不幸的是，我们只有骁龙三星 Galaxy Note 9 型号的版本，所以如果你有 Exynos Galaxy Note 9，你必须等到你的手放在 Android Pie 上。](https://www.xda-developers.com/exclusive-this-is-android-pie-with-samsung-experience-10-on-the-samsung-galaxy-s9/)

如果您有骁龙三星 Galaxy S9 或三星 Galaxy S9+，您已经可以在您的设备上安装 Android Pie:

## 如何在骁龙三星 Galaxy Note 9 上安装三星 Experience 10.0 的 Android Pie

警告:这个版本可能不稳定。我们不建议安装它，除非你愿意处理一些 bug。例如，可能会不断崩溃，一些应用程序可能无法使用。更多的功能可能会被破坏，我们还没有看到。除非你熟悉 Odin，否则不要安装这个，因为如果你打算降级回 Android 奥利奥，你需要知道如何使用这个工具。最后，不要启用最大省电模式，因为这可能会导致启动循环。

此次更新包括新的 Android Pie 功能，如横向最近应用概述和重新设计的 UI，强调黑色背景和白色圆角卡片。三星 Experience 10.0 有一些新功能，如系统范围的夜间主题，尽管一些新功能不完整，如手势。按照下面的说明为您的三星 Galaxy Note 9 和高通骁龙 845 安装第一个可用的 Android Pie build。

1.  首先，[下载 Odin 3.13.1](https://forum.xda-developers.com/attachment.php?attachmentid=4446947&d=1521037501) ，【ARI5 到 ARJA 的 update.zip， [Odin 文件](https://drive.google.com/file/d/1exO5oTf8FS3odOUMI_ffvugxjCZrgUAw/view)。
2.  如果你的 Galaxy Note 9 中有 SD 卡，请将 update.zip 复制到 SD 卡中。如果你没有 SD 卡，跳过这一步。
3.  打开奥丁文件。这个压缩文件将被命名为美国电话电报公司 _N960USQU1ARJ7.zip。在这个文件中，你会看到六个文件。在奥丁，你会看到 5 个类别，虽然你只会用 4 个。这是一个通用更新，不是专门针对美国电话电报公司的，因此它将保留运营商品牌。
4.  通过关闭 Galaxy Note 9，然后按住电源+音量降低+ Bixby 按钮，将您的 Galaxy Note 9 置于 Odin 模式。
5.  打开 Odin，放上对应的 BL，AP，CP，CSC，但是 Userdata 里什么都没有。这将删除你手机上的所有数据。
6.  点击开始。
7.  你的 Galaxy Note 9 会刷新新固件，然后重启。
8.  在你这样做之后，等待大约 5 分钟，然后关闭你的 Galaxy Note 9，并通过按住电源+音量+ Bixby 重新启动进入恢复状态。
9.  现在使用 ARJ7 来更新 OTA。
10.  使用音量按钮和电源来选择“从 SD 卡应用更新”如果您没有 SD 卡，请跳至步骤 12。
11.  再次使用音量按钮选择 update.zip 文件，并使用电源按钮选择它。然后更新将开始。更新可能需要 2 到 10 分钟。完成此步骤后，跳到步骤 13。
12.  如果您没有 SD 卡，请使用音量按钮选择“从 adb 应用更新”选项。然后在你的电脑上打开一个命令提示符/终端，输入:

    ```
     adb sideload <file location of update.zip> 
    ```

    然后回车。更新将开始，需要 2 到 10 分钟。
13.  你的手机现在应该运行一个用户界面。

你应该为三星 Galaxy Note 9 启动基于 Android Pie 的三星 Experience 10。关注 XDA 门户网站，了解三星 Experience 10 更新的最新消息。如果 Galaxy Note 9 Android Pie build 有任何新的更新，我们会让您知道，并在有新文件可用时用新文件更新本文。