# 如何在 Android 上禁用 Facebook Messenger Day 功能

> 原文：<https://www.xda-developers.com/disable-facebook-messenger-day-android/>

在脸书与 Snapchat 永无休止的斗争中，该公司推出了一项名为 Facebook Messenger Day 的功能。虽然 Snapchat Stories 功能是一种让你向人们展示你当天做了什么的方式，但 Facebook Messenger Day 的过滤器和 Active Now 指示器可以快速找到要做的事情或要聊天的人。问题是，它已经变成了那些被推到你面前的特征之一。如果你讨厌脸书的每日功能，并希望它不再要求你“增加你的一天”，幸运的是有一种方法可以禁用 Facebook Messenger Day。你将不再被 Messenger Day Snapchat 克隆和 My Day 功能所困扰，因为我们将在应用程序中完全禁用它。

虽然一些用户可能会发现[新的 Messenger 功能](https://www.xda-developers.com/facebook-messenger-platform-2-1-natural-language-processing/)很有用，但其他人[讨厌强加给他们的功能](https://www.xda-developers.com/facebook-to-roll-out-ads-in-facebook-messenger-globally/)。脸书《我的一天》就是这样一部讨厌的电影，至少对某些人来说是这样。目前，Facebook Messenger Day 可以显示在您聊天列表中的任何位置。有些人发现它就在屏幕的最上方(即使他们不在乎使用它)，而其他人在滚动聊天时会发现它藏在两个聊天记录之间。许多人希望脸书能让最终用户选择是否使用 My Day 功能，而不是强迫他们使用。

有两种不同的方法来禁用 Facebook Messenger Day，一种需要您拥有 root 访问权限，另一种不需要 root 访问权限。根方法将主动禁用您自己现有的 Facebook Messenger 应用程序中的 My Day 功能，而非根方法则是可能的，这要归功于我们自己社区中的某个人对 Facebook Messenger 的修改版本。

* * *

## 禁用 Facebook Messenger Day(根方法)

1.  下载并启动[终端模拟器应用](https://forum.xda-developers.com/android/apps-games/3-0-material-terminal-emulator-t3041056)
2.  在提示符下执行以下命令:`su`
3.  然后在提示符下执行以下命令:`am start -n "com.facebook.orca/com.facebook.messaging.internalprefs.MessengerInternalPreferenceActivity"`
4.  一旦您执行第二个命令，它应该会在 Facebook Messenger 中启动一个隐藏的设置页面
5.  点击门覆盖选项
6.  点击搜索网关守护设备选项
7.  搜索以下文本:内部
8.  然后将 messenger _ internal _ prefs _ Android 选项设置为 YES
9.  点击导航栏中的后退按钮
10.  现在，查找并点击 MobileConfig 选项
11.  搜索以下文本:wave2
12.  将“启用 wave2 蒙太奇”选项设为假
13.  然后点击底部的“立即重启”选项来重启 Messenger

## 禁用 Facebook Messenger Day(无根用户)

如前所述，前面的方法需要 root 用户，但是没有 root 用户访问权限的用户可以使用另一种方法。XDA 成员[邪恶袋熊](https://forum.xda-developers.com/member.php?u=5029215)已经[创造了一个脸书和信使应用](https://forum.xda-developers.com/android/apps-games/bullshified-version-facebook-okay-to-t3586318)的修改版本。这些修改后的版本减少了广告，删除了无用的功能，等等。此外，这个修改版本还允许访问内部设置选项，而不必使用 shell 命令。

通常情况下，内部设置菜单需要 root 访问权限才能用股票信使应用程序打开它，因为内部设置菜单是一个未导出的活动，但 evilwombat 已经进入并修改了 Facebook 信使应用程序，以便在安装他们的版本时可以自由访问。由于 Messenger 的这个修改版本可以简单地加载到任何支持的 Android 智能手机或平板电脑上，这意味着如果你选择使用这个修改的应用程序，你可以绕过上面指南的步骤 1 至 9。

但是，脸书使用基于密钥的身份验证来实现其应用程序系列之间的数据共享。所以为了使用这种不需要 root 权限的方法，**你需要卸载脸书**开发的所有其他应用程序。这包括脸书本身，Facebook Messenger，Facebook Messenger Lite，Page Manager 等。由于 evilwombat 必须用自己的密钥签署修改后的 APK，这导致了与脸书家族中其他应用程序的冲突。

因此，一旦您卸载了这些应用程序，然后从 evilwombat 下载了修改后的应用程序，我们就可以按照下面的步骤操作了。

1.  启动 Messenger 应用
2.  深入设置
3.  点击内部菜单选项
4.  查找并点击 MobileConfig 选项
5.  搜索以下文本:wave2
6.  将 wave2 蒙太奇启用功能更改为 false
7.  然后点击底部的“立即重启”选项来重启 Facebook Messenger

因此，再次，步骤实际上禁用脸书我的一天，从修改版本是相同的根方法。我们可以跳过很多教程，因为 Facebook Messenger 应用程序设置中的内部菜单选项已经启用。我们所做的就是从这个隐藏的内部菜单中进入并关闭这个新功能，这将防止脸书我的一天功能堵塞你的应用程序。

* * *

### 说明

因此，我们在本指南中所做的是在 Facebook Messenger 应用程序中显示一个隐藏菜单。我们可以用一个终端模拟器来实现，这个终端模拟器有根用户权限，或者用一个修改过的 APK 来实现，它有一个暴露给用户的菜单。在隐藏菜单中，我们可以开始切换大多数用户通常无法使用的几个选项。

要真正禁用 Facebook Messenger Day，我们需要在 Facebook Messenger 内部设置部分查找并点击 MobileConfig 选项。一旦你去那里，你将能够搜索一些东西，所以只需输入 wave2，你会看到我们需要改变的 wave2 蒙太奇功能。该页面上将有一个值部分，默认情况下设置为 True，但我们只需要点击 False 选项(对我来说就在 True 上面)。

当您将其从 True 更改为 False 时，您应该会看到页面底部出现一条消息，说明您的覆盖已经设置好，并告诉您重新启动应用程序以使您的更改生效。继续点击立即重启蓝色文本，Facebook Messenger 将关闭，然后再次打开。这个方法是由于 [/u/jagotu](https://www.reddit.com/user/jagotu) 在 [/r/Android 线程中被发现的，他们创建了关于它的](https://www.reddit.com/r/Android/comments/6gsn5m/turn_off_messenger_my_day_on_latest_version_root/)。