# 如何将 App 自动启动选项插入索尼 Xperia 设置菜单

> 原文：<https://www.xda-developers.com/how-to-insert-app-autostart-option-into-sony-xperia-settings-menu/>

尽管近年来启动时间已经显著减少，并且由于不可恢复的延迟或类似问题，现在只偶尔需要重启，但它仍然*似乎*不能再慢了。这就是为什么许多人求助于禁用启动时运行的不需要的应用程序，以降低启动速度。但是当 Android 平台本身没有这个选项时，你能做什么呢？与其走下载应用程序的捷径，为什么不自己把它添加到你的设置页面呢？嗯，这正是 XDA 公认的贡献者[DaRk-Lord](http://forum.xda-developers.com/member.php?u=4872623)在新教程中向索尼 Xperia 用户展示的内容。

用清晰简单的说明解释，这个过程基本上包括反编译 *Settings.apk，*在众多的 *xml* 和 *smali* 文件中添加和更改代码行，并重新编译 apk。正因为如此，DaRk-L0rD 提供了大量的截图来配合书面说明，以便尽可能地使事情清晰易懂。

如果你拥有一台索尼 Xperia 设备，并希望了解更多，请前往[原始主题](http://forum.xda-developers.com/showthread.php?t=2626333)并开始学习。