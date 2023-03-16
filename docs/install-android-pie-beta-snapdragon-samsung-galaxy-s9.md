# 如何在骁龙三星 Galaxy S9 上安装 Android Pie beta

> 原文：<https://www.xda-developers.com/install-android-pie-beta-snapdragon-samsung-galaxy-s9/>

# 骁龙三星 Galaxy S9 现已推出早期 Android Pie 测试版

在三星 Galaxy S9+泄露之后，骁龙三星 Galaxy S9 的早期 Android Pie 测试版已经泄露。下面是手动安装的方法。

昨天，我们公布了三星 Galaxy S9+的三星 Experience 10 的[第一手资料。在发布了关于](https://www.xda-developers.com/exclusive-this-is-android-pie-with-samsung-experience-10-on-the-samsung-galaxy-s9/)[如何在骁龙三星 Galaxy S9+](https://www.xda-developers.com/install-android-pie-samsung-experience-10-samsung-galaxy-s9/) 上安装早期 Android Pie 测试版的细节后，我们现在有了这个相同的版本，但适用于较小的骁龙三星 Galaxy S9。如果你对更新中的新内容感兴趣，[看看我们之前的文章](https://www.xda-developers.com/exclusive-this-is-android-pie-with-samsung-experience-10-on-the-samsung-galaxy-s9/)。如果你想在装有高通骁龙 845 的三星 Galaxy S9 上安装早期的 Android Pie 测试版，请查看下面的教程。目前，我们只有骁龙三星 Galaxy S9 和 Galaxy S9+的版本，但没有 Exynos 型号或三星 Galaxy Note 9 的版本。

与骁龙三星 Galaxy S9+ build 不同，我们对骁龙三星 Galaxy S9 的测试人员报告说，前置摄像头和 AR 表情符号都可以工作。然而，由于这是一个早期的测试版本，您的里程可能会有所不同。

警告:这个版本不稳定。我们不建议安装它，除非你愿意处理一些问题。新的夜晚主题不能被禁用。更多的功能可能被破坏，我们还没有看到它。除非你对奥丁感到舒服，否则不要安装这个，因为虽然降级到奥利奥是可能的，但这样做并不容易。不要启用最大节电模式。这将导致你的手机崩溃，无法启动。

## 为骁龙三星 Galaxy S9 安装基于 Android Pie 的三星 Experience 10

1.  首先下载 [Odin 3.13.1](https://forum.xda-developers.com/attachment.php?attachmentid=4431749&d=1519672710) 、[ARI6 到 CRJB update.zip](https://firmware.science/download?url=52758/1488/SS-G960USQS3ARI6-to-U3CRJB-UP) 和 [Odin 文件](https://androidfilehost.com/?fid=1322778262904019664)。
2.  如果您的 Galaxy S9 中有 SD 卡，请将 update.zip 复制到 SD 卡中。如果您的 Galaxy S9 中没有 SD 卡，请跳过这一步。
3.  打开奥丁文件。这个压缩文件将被命名为 G960USQS3ARI6.zip。在奥丁，你会看到 5 个类别，虽然你只会用 4 个。这是一个通用的更新，而不是一个专门为 T-Mobile。不过，它将保留运营商品牌。
4.  关闭你的 Galaxy S9 进入 Odin 模式，然后按住电源+音量降低+ Bixby 按钮。
5.  打开 Odin，放上对应的 BL，AP，CP，HOME_CSC(忽略 CSC)，但是 Userdata 里什么都没有。
6.  点击开始。
7.  你的手机将刷新新的固件，然后重新启动。
8.  这样做之后，等待大约 5 分钟，然后关闭 Galaxy S9，按住电源+音量增大+ Bixby 按钮重新启动进入恢复模式。
9.  使用音量按钮和电源来选择“从 SD 卡应用更新”如果您没有 SD 卡，请跳至步骤 11。
10.  再次使用音量按钮选择 ARI6 至 BRJ5 update.zip 文件，并使用电源按钮选择它。更新将开始，可能需要 2 到 10 分钟。完成这一步后，跳到第 11 步。
11.  如果您没有 SD 卡，请使用音量按钮选择“从 adb 应用更新”选项。然后在你的电脑上打开一个命令提示符或终端，输入:

    ```
     <span >adb sideload </span><span ><</span><span >file location of update</span><span >.</span><span >zip</span><span >></span> 
    ```

12.  更新完成后，我们建议您恢复出厂设置。这有助于解决稳定性问题。