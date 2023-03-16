# 在 Android 10 的 rooted Pixel 上启用 Google Pay 的快速钱包访问

> 原文：<https://www.xda-developers.com/enable-quick-wallet-access-google-pay-pixel-android-10/>

在早期的 Android Q betas 中，在设置中发现了一个名为“[出示卡片&通过](https://www.xda-developers.com/android-q-google-pay-power-menu/)的新手势。根据它的描述，这个功能允许人们从 Google Pay 访问他们的信用卡、通行证和门票，以及在 power 菜单中的紧急信息卡。当谷歌向公众推出 Android 10 时，他们建立了一个网页，详细介绍了新操作系统的一些新功能。其中一个功能被称为“快速钱包访问”，它的描述与我们在早期 Android Q betas 中看到的相匹配。然而，这段文字被从页面上删除了，而且该功能从未出现在任何 Android 10 版本中——即使是在 10 月份推出 Pixel 4 和 12 月份首次“ [Pixel 功能下降](https://www.xda-developers.com/google-pixel-feature-drop-post-snap-portrait-mode-auto-call-screen/)”的时候。不过，我们知道这个功能仍然存在，因为我们[在九月中旬](https://www.xda-developers.com/android-10-quick-wallet-access-google-pay/)设法激活了它，并且我们已经确认它今天仍然有效。现在，我们正在分享我们的 mod，以便在您自己的根 Pixel 智能手机上实现快速钱包访问。

启用此功能将更改您通过长按电源按钮访问的电源菜单的用户界面。新的电源菜单由一个大的和一个小的卡片组成，水平排列在屏幕底部，而不是一列按钮排列在右侧。在屏幕的顶部，你会发现一排卡片，你可以向左或向右滑动。您的紧急信息和您在 Google Pay 中添加的任何卡片都将出现在此处。这个“快速钱包访问”功能的目的是让你不必打开 Google Pay 应用程序来切换你的活动卡。你所要做的就是长按电源按钮，向左或向右滑动来选择你想要的卡。

为了在更改您的活动卡后进行支付，您仍需要解锁手机。如果你在 Pixel 4 上设置了面部解锁，你就可以立即解锁手机——甚至在快速钱包访问出现在电源菜单之前——进行支付。这就是为什么我预计这项功能会出现在 Pixel 4 的第一个 Pixel 功能下降中，但幸运的是，我们知道这项功能不会是 Pixel 4 独有的。【2019 年 12 月更新的[变更日志](https://support.google.com/pixelphone/thread/21769134)引用了这一功能，暗示它可能会出现在像素 2、像素 2 XL、像素 3、像素 3 XL、像素 3a、像素 3a XL、像素 4 和像素 4 XL。谷歌称这是一个“实验性功能”，所以它可能永远不会正式推出。如果他们真的推出它，它可能会先出现在像素 4，然后再推出旧像素。如果你不想等待，或者你有一部第一代 Pixel 手机，并且想享受乐趣，你可以试试下面链接的我的 mod。

**要求:**

*   内置快速钱包访问功能的系统用户界面。这包括 Android 10 上的谷歌 Pixel、Pixel XL、Pixel 2、Pixel 2 XL、Pixel 3、Pixel 3 XL、Pixel 3a、Pixel 3a XL、Pixel 4 和 Pixel 4 XL。这很可能无法在非 Pixel 智能手机上运行，除非你运行的是 Pixel Experience 等使用谷歌 SystemUI 的定制 ROM。
*   使用 Magisk 进行 Root 访问。

**步骤:**

1.  打开 Magisk Manager 并从下载部分安装“SQLite for ARM aarch64 devices”模块。*注意:如果你已经从 TitaniumBackup 或 Termux 获得了一个 SQLite 二进制文件，那么安装程序脚本会检测到它，所以你不需要安装这个单独的 SQLite 二进制文件。如果是，请继续执行步骤 3。*
2.  重启你的手机。
3.  下载我的 Magisk 模块并安装在 Magisk 管理器中: [GooglePayPowerMenu.zip](https://www.androidfilehost.com/?fid=4349826312261679802)
4.  重启你的手机。
5.  前往“设置”>“系统”>“手势”,查看“卡与通行证”是否出现在列表中。确保该功能已启用。
6.  长按电源按钮，查看新的电源菜单界面是否显示。在顶部，您应该会看到一张紧急信息卡和您在 Google Pay 中添加的任何卡片。

**故障排除:**

您可能需要等待一段时间或再次重启，以便快速钱包访问功能开始工作。对我来说，它出现在我第二次打开电源菜单之后。此外，如果你因为 SafetyNet 而无法将卡添加到 Google Pay，那么一定要安装 [GPay-SQLite-Fix Magisk 模块](https://github.com/stylemessiah/GPay-SQLite-Fix/)。

**卸载:**

最后，如果你想完全卸载这个 mod 并把电源菜单恢复到原来的界面，你必须做以下事情:

1.  卸载 Magisk 管理器中的模块
2.  从/data/adb/service.d 中删除 2 个 quickwalletaccess 脚本
3.  运行以下 shell 命令:

    ```
     adb shell settings put secure global_actions_panel_debug_enabled 0
    adb shell settings put secure global_actions_panel_available 0 
    ```

4.  重新启动

* * *

*我要感谢 XDA 资深成员 [73sydney](https://forum.xda-developers.com/member.php?u=9317193) 、jcmm11、adpoliak 以及所有其他参与 [GPay-SQLite-Fix](https://github.com/stylemessiah/GPay-SQLite-Fix/tree/master/common) Magisk 模块的人，因为我借用了代码来检查 SQLite 二进制文件。*