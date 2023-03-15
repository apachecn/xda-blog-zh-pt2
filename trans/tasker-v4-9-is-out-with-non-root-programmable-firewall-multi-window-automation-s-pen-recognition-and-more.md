# Tasker v4.9 推出了非根可编程防火墙、多窗口自动化、S-Pen 识别等功能

> 原文：<https://www.xda-developers.com/tasker-v4-9-is-out-with-non-root-programmable-firewall-multi-window-automation-s-pen-recognition-and-more/>

众所周知，我们 XDA 是 Tasker 的忠实粉丝。在过去的中，我们已经多次介绍了该应用程序及其功能[，并展示了由于其广泛的插件框架，Tasker 的潜在用途是无限的。Tasker 在过去的几年里变得如此强大，以至于在过去的一年左右，应用程序的开发速度明显放缓。这并不意味着在 Tasker 上的开发是不必要的或死亡的，因为新版本的 Android 引入了自动化成熟的新功能。](https://www.xda-developers.com/tag/tasker/)

早在 7 月，Tasker 的开发者开玩笑说，Tasker 的下一个重大更新将利用 Android 的 VPN 集成，允许[非根、每个应用程序、可编程防火墙](https://www.xda-developers.com/upcoming-tasker-update-to-bring-non-root-per-app-firewall/)。在这一发现近 5 个月后，Tasker 终于收到了 4.9 版本的更新，带来了这一特性以及大量的额外变化。

* * *

## **Tasker 的新功能**

开发者已经在他的网站上发布了一个完整的变更日志，但是有太多的变更需要列出来。以下是本次更新中 Tasker 最重要的变化:

*   新增**网络访问控制。**这个新动作位于净动作类别下。您有 4 个不同的选项来控制设备上的网络访问:全部允许、允许、全部拒绝或拒绝。如果您选择“允许”或“拒绝”，您可以选择允许或拒绝哪些特定应用程序的网络访问。由于这是一个操作，您必须将它与相关的上下文结合起来触发它，或者您可以设置一个启动器快捷方式来手动运行包含此操作的任务。
*   新增**切换分屏**动作。此操作位于应用程序操作类别下。此操作没有配置选项。和以前一样，这个动作包含在任务中，因此必须与触发任务的上下文相结合。不幸的是，你似乎不能使用这个操作直接打开你选择的两个应用程序，因为 Tasker 只切换多窗口，所以你必须手动选择另一个应用程序在多窗口中启动，或者使用 AutoInput 选择第二个应用程序。
*   新的**笔出**和**笔菜单**状态。这些是新的状态上下文(只要满足条件，它就是活动的)，Tasker 现在可以对用户从设备支架上取下 Samsung S Pen 或显示 S Pen Air 按钮菜单做出反应。
*   支持**外置 SD 卡**。以前，Tasker 不能很好地处理位于外部 SD 卡上的文件。现在，该应用程序已更新为使用新的外部 SD 访问 API。当您在文件类别中选择任何操作时，您现在会在 Tasker 的内部文件浏览器的右下角看到一个小的 SD 卡图标，这将允许您选择 SD 卡上的文件。
*   增加了对原生**返回按钮和最近按钮的支持。**您将不再需要依赖第三方插件来满足您的用户界面导航需求，因为您可以使用 Tasker 创建自己的导航应用。
*   增加了在设备上显示**电源菜单**的支持。使用这个和 AutoInput 插件，如果你的设备在电源菜单中有重启功能(比如新的谷歌 Pixel 手机)，你现在可以自动重启你的设备。
*   使用 Android 7.0+中的新媒体按钮 API，这应该可以修复用户从 Tasker 输入媒体按钮时遇到的任何问题。
*   场景生成器的大量 UI 和 UX 改进——对于新用户来说，这是 Tasker 最令人沮丧的部分之一。

正如我之前提到的，本次更新中添加了大量的错误修复、更改和功能。如果您是 Tasker 的粉丝，那么您应该阅读完整的变更日志，以了解新内容。此外，由于我不想让 Tasker 的任何新用户蒙在鼓里，这里有一些我想出的利用这些新特性的快速想法。您可以根据以下描述轻松实现这些功能，并根据您的需要进行修改。

在下面的第一个选项卡中，您将看到新的网络访问功能的快速简单的使用。我创建了一个配置文件，当我不在家庭网络上时，它会禁用 Mint 应用程序的网络访问。在第二个选项卡中，我使用新的切换分屏功能设置了快速驾驶模式配置文件。在这里，连接到我的蓝牙设备后，Tasker 将在多窗口模式下启动地图和 Google Play 音乐。这需要借助[自动输入](https://play.google.com/store/apps/details?id=com.joaomgcd.autoinput)从最近的应用程序屏幕中选择第二个应用程序。

[tabs][tab title =" **防火墙** "]

```
 Profile: Firewall (78)
State: Not Wifi Connected [ SSID:Rahman MAC:* IP:* ]
Enter: Anon (81)
A1: Network Access [ Mode:Deny App:Mint ] 
```

[/tab][tab title =" **驾驶模式多窗口** "]

```
 Profile: Driving Mode (82)
 State: BT Connected [ Name:FLEXSMART X3 MINI Address:* ]
Enter: Anon (86)
 A1: Launch App [ App:Maps Data: Exclude From Recent Apps:Off Always Start New Copy:Off ] 
 A2: Launch App [ App:Play Music Data: Exclude From Recent Apps:Off Always Start New Copy:Off ] 
 A3: Toggle Split Screen 
 A4: Wait [ MS:0 Seconds:2 Minutes:0 Hours:0 Days:0 ] 
 A5: AutoInput Action [ Configuration:Type: Point
Value: 540,1465
Action : Click
Is Tasker Action: false
Check Screen State: false Timeout (Seconds):20 ] 
```

[/tab]

[/tabs]

请注意，这些只是对两个相当简单的概要文件的描述。如果您重新创建这些，请确保在“防火墙”配置文件中将 SSID 更改为指向您自己的家庭网络，并在“驾驶模式多窗口”配置文件中将蓝牙设备更改为您的汽车蓝牙。

如果我们将来想出了任何伟大的 Tasker 脚本，我们一定会在 XDA 门户上分享它们。如果你自己想出了一个很棒的 Tasker 点子，欢迎在下面发表评论，或者点击下面的链接访问我们的 Tasker 技巧论坛。

* * *

[**访问我们的 Tasker Tips &招数论坛**](http://forum.xda-developers.com/u/tasker-tips-tricks)

[**从谷歌 Play 商店**下载 Tasker](https://play.google.com/store/apps/details?id=net.dinglisch.android.taskerm&hl=en)