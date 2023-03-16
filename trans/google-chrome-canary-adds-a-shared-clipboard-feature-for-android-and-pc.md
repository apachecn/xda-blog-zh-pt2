# 谷歌 Chrome Canary 的共享剪贴板将文本从 PC 复制到 Android

> 原文：<https://www.xda-developers.com/google-chrome-canary-adds-a-shared-clipboard-feature-for-android-and-pc/>

# 谷歌 Chrome Canary 为 Android 和 PC 增加了共享剪贴板功能

使用谷歌 Chrome Canary，你现在可以使用新的共享剪贴板功能将文本从一个运行 Canary 的设备复制到另一个设备。

如果您在便携式设备和台式机上使用相同的浏览器，不同设备之间的同步是理想的。我的日常使用依赖于[谷歌 Chrome](https://www.xda-developers.com/google-chrome-for-android-new-shortcut-tab-switcher-menu/) ,并享受 Android 和桌面版本之间的无缝同步。在 Chrome 77 中，谷歌还增加了“[发送到你的设备](https://www.xda-developers.com/chrome-android-self-share-tabs/)”功能，让你可以将网页从桌面版本发送到其他移动设备，反之亦然。另一个有意义的功能正在开发中——“共享剪贴板”,它将允许用户跨设备复制内容。该功能最近被添加到 Chrome 的金丝雀频道，下面是你如何使用它。

首先，确保你的台式机和智能手机上都安装了 Chrome Canary 79。在桌面版上，在地址栏输入 **`chrome://flags/`** 。在页面的搜索栏中查找“clipboard ”,你会看到下面列出的 Chrome 标志:

*   使接收器设备能够处理共享剪贴板功能
*   允许处理共享剪贴板特征信号
*   同步剪贴板服务

单击下拉菜单，将“默认”作为预设选项，并为所有三个标志选择“启用”。之后，系统会提示你点击“重启”按钮重启 Chrome Canary。没有必要在智能手机上单独启用这些标志。

现在，你可以在 Canary 中选择任何网页上的任何文本，然后右键单击以显示选项，“将文本发送到<*设备名称* >”请注意，您还必须在 Android 设备上安装金丝雀频道，以便向该设备发送文本。你的智能手机会弹出一个通知，告诉你文本已经被添加到你的剪贴板。复制的文本将与您的 Android 智能手机上的剪贴板同步，并可以普遍粘贴。

你只需在任何文本栏内长按并点击粘贴，就可以使用复制的文本，就像我在谷歌的信息应用程序中使用它一样。同样，如果你在 Android 版本的 Chrome Canary 上启用了标志，你将能够共享文本。一旦你选择了文本，并从出现的菜单中选择“分享”，你会在 Android 的分享表中看到一个选项，将它分享给其他运行 Canary 的设备。

* * *

**Via:[Chrome Story](https://www.chromestory.com/2019/09/how-to-use-chromes-shared-clipboard/)**