# tasker 5 . 9 . 3 . beta 4 增加了“通过应用程序联系”来自动化 WhatsApp 呼叫、WireGuard 集成等

> 原文：<https://www.xda-developers.com/tasker-5-9-3-beta-4-contact-via-app-wireguard-integration/>

就 Android 上的自动化应用而言，Tasker 被广泛认为是最佳选择之一。该应用程序允许你创建基于特定条件自动触发的配置文件来执行任务，它提供了大量的插件，可以帮助你在 Android 设备上自动化几乎任何事情。例如，该应用程序最近的测试版引入了完整的[勿扰定制和传感器操作](https://www.xda-developers.com/tasker-5-9-3-beta-do-not-disturb-customization-sensor-actions/)，让你可以完全个性化手机的勿扰模式，并启动由手机传感器收集的值触发的任务。现在，该应用程序在测试频道又有了重大更新，带来了更多的东西。

**[XDA Tasker 提示&招数论坛](https://forum.xda-developers.com/u/tasker-tips-tricks)**

根据最近在 Reddit 上的一篇帖子，Tasker v 5 . 9 . 3 beta 4 现在向用户推出，它包括了大量有趣的新功能。以下是最新 Tasker 测试版中一些最值得注意的特性:

如果你曾经想要自动开始 WhatsApp 聊天、视频通话或在谷歌地图中导航到联系人的地址，现在你可以使用新的“通过应用程序联系”操作来实现这一点。该操作可让您在设备上选择任何联系人，然后根据您安装的应用程序，选择要执行的操作。正如您在视频演示中看到的，您可以使用这一新操作启动 Google Maps 导航，导航到特定联系人的地址，与该联系人进行 Skype 通话，在 WhatsApp 中查看他们的个人资料信息，或者在 WhatsApp 上与他们进行音频/视频通话。虽然从技术上讲，您可以通过发送意向来完成所有这些工作，但新功能现在消除了一些跑腿工作，使整个过程更容易。

### WireGuard 集成

对于不知道的人来说，WireGuard 是一个全新的现代 VPN 协议[，刚刚进入 Linux 内核](https://www.xda-developers.com/wireguard-vpn-linux-kernel-5-6/)。如果你在你的设备上运行一个支持 WireGuard 的定制内核，你可以使用 [WireGuard Android 应用](https://play.google.com/store/apps/details?id=com.wireguard.android)来控制 WireGuard VPN 隧道。然而，打开/关闭 WireGuard VPN 隧道是一个手动过程，如果您经常这样做，可能会变得很麻烦。如果您希望根据您的当前位置自动启用/禁用 VPN 隧道，您现在可以使用 Tasker 来实现。查看下面的演示视频，了解如何在您的设备上进行配置。

除了这两个特性，最新的 Tasker beta 更新还包括其他几个变化，您可以在下面的 changelog 部分看到。如果您有兴趣亲自尝试这些功能，您可以通过点击[此链接](https://joaoapps.com/beta-testing/)注册 Tasker 测试版，然后从下面的 Play Store 链接下载最新版本。

 **### 完整变更日志

*   通过应用程序操作添加新联系人，允许您通过第三方应用程序与联系人交流(例如通过 Whatsapp 进行视频通话，通过 skype 进行音频通话等)
*   在 Tasker 函数动作中增加了控制 WireGuard 隧道的动作
*   允许 Tasker 二级 app 被 tasker://secondary 这样的网址触发？text=hello&other=hi 其中每个参数都将作为触发任务中的 Tasker 变量
*   添加了“请勿打扰”操作的查询选项
*   在测试网络中添加选项以获取您手机的 Wifi IP 地址
*   修复了各种情况下的文件修改事件
*   在文件修改事件中增加了事件过滤器，这样你可以只对一个事件而不是所有事件做出反应
*   已将文件修改事件的%evtprm(1)从受监视的路径更改为已更改的实际文件的路径
*   允许文件修改事件处理文件修改字段中的变量
*   将%evtprm()添加到具有事件条件的配置文件中的操作的变量列表中
*   增加了等待文件事件函数到 Tasker 函数动作，这样你就可以等待一个文件写完
*   通过询问您想要移动项目多少个位置，而不是一个位置一个位置地移动，使左右移动项目变得更加容易
*   修正了在后台获取剪贴板的问题
*   修正了在 Android 10 上截图，不应该再在截图上显示提示
*   修复了获得 gzipped 响应时的 HTTP 请求操作。现在自动解压它
*   修正了某些情况下 HTTP 请求动作的自动重定向
*   在列表对话框动作中添加了行分隔符
*   在 Tasker 函数动作中取得 Sims 动作请求 READ_PHONE_STATE 权限
*   如果需要，为儿童应用程序添加生物识别权限
*   添加了使用菜单动作时关于列表对话框动作的提示
*   试图让 Tasker 只检查根用户的访问权限，如果使用了根用户操作

 *** * *

**来源:[Reddit](https://www.reddit.com/r/tasker/comments/g1to35/dev_tasker_593beta4_contact_via_app_wireguard/)******