# Telegram X 月更新带来了改进的通知和帐户管理器

> 原文：<https://www.xda-developers.com/telegram-x-april-update-brings-revamped-notifications-and-account-manager/>

# Telegram X 月更新带来了改进的通知和帐户管理器

Telegram X 是 Android 客户端的一个轻量级版本，他们在这里测试新功能。最新的更新修订了通知和帐户管理器。

Telegram 可能不像 WhatsApp 或 iMessage 那样受欢迎，但它有其公平的用户份额。该应用程序有一个干净直观的界面，以及总是备份的媒体和信息。电报 X 是服务的一个变体，目的是在某个时候取代电报。Telegram X 没有任何旧版应用程序的遗留代码，因此更加稳定，基础设施也更加及时。就在几天前，该应用程序被更新到版本 0.21.7.1151，尽管它更方便地被称为四月更新。变化的清单是巨大的，但我会挑选最重要的。

## 新的通知系统

四月份的更新带有一个完全重写的通知系统，Telegram 称之为通知 2.0。它有很多稳定性改进和一些定制功能。可能最显著的变化是，在收到来自另一个聊天的消息后，被驳回的通知将不会再次出现。有时它们只是随机弹出，所以现在也修复了。通知延迟也变得越来越智能，这样当你的手机放在桌子上时，你可以继续从你的笔记本电脑发送消息。现在也可以对通知进行分组。

## 新客户经理

Telegram 还宣布，4 月份的更新包括多帐户 2.0。你可能已经知道，Telegram X 已经支持多个账户有一段时间了，因此不再需要克隆应用程序或第三方替代品。但是，如果你使用很多账户，设备的内存和电池就很难跟上。Telegram X 的最新更新通过完全重写核心功能来解决这个问题。他们甚至声称“不管你在 Telegram X 中有 3 个还是 3000 个账户都没关系”，这听起来很不错。

## 更大的

上面的特性是从零开始重新构建的，所以我认为它们比其他的更重要。但是，有更多的更新。Telegram X 现在支持在私人聊天中删除两端的消息，创建和参与投票，安装和共享语言包(我相信你会有创造力)，改进的 2FA 过程，等等。变更日志可以在下面看到。四月份的更新现在只对 50%的用户开放，所以你可能还没有收到。你可以从下面的谷歌 Play 商店列表中下载 Telegram X。

### 电报 X 四月更新变更日志

### 通知 2.0

通知已经从头开始重建，带来了改进的行为和可靠性，新的功能和定制，并减少了后台电池的使用。有一些亮点:

*   通知现在工作时，没有连接电报服务器:这并不重要，无论你是试图访问电报从审查地区或选定的代理关闭；
*   每当通知出现明显问题时，你会在“设置”附近的应用菜单中看到警告。跟随它查看如何解决它的完整指南；
*   清理通知托盘。当收到来自另一个聊天的通知时，或由于未知事件，被拒绝的通知将不会再次出现；
*   改进了对三星设备上 Edge 屏幕的支持。要打开:系统设置>显示>边缘屏幕>边缘照明>管理通知>打开电报 X 的切换；
*   当您从其他设备聊天时，智能通知会延迟；
*   通知现在按聊天类型分组。在设置>通知>高级>合并通知类别中切换此行为；
*   选择隐藏秘密聊天通知，当设备屏幕被锁定(你仍然会听到声音和振动)；
*   来自频道的静默广播通知现在静默显示在通知栏中；
*   频道的单独设置；
*   禁用特定聊天的消息预览；
*   系统通知声音选择器，如果可用(允许设置任何自定义通知声音)；
*   当应用程序被密码锁定时，显示只读通知的选项；
*   完全控制提及、回复和锁定消息通知(打开“通知所有成员”)。

    默认情况下，当有人在聊天中提到你时，会应用来自该人的通知设置(比如他们会直接向你发送消息)。当你在一些聊天中变得受欢迎时，这可能会成为一个问题，因为唯一的选择是一个接一个地静音每个成员，或者禁用所有私人聊天的通知。

    为了在不静音所有聊天的情况下停止接收不想要的通知，现在您可以静音该群组&只需在设置>通知>群组>提及和回复/锁定消息中关闭提及、回复&锁定消息通知的通知覆盖，包括每个聊天和全局通知；
*   虽然 Telegram X 通知的可靠性显著提高，但一些设备制造商的系统设置仍然可能会阻止通知可靠地工作(即，当应用程序关闭时，会有很大的延迟或根本不会到达)；

    如果您仍然遇到通知问题，请检查电报 X >设置>通知中是否有任何警告。如果没有显示警告，请查看[故障排除通知问题](https://telegra.ph/Notifications-FIX)。如果这也没有帮助，请联系电报支持。

    我个人也建议在其他应用程序中查看是否有任何针对您设备的通知问题。我个人对全面的 [Slack](https://get.slack.help/hc/en-us/articles/360001562747-Known-issues-with-Android-notifications) 指南印象深刻，它几乎可以应用于任何其他 Android 应用程序。

### 功能和变化

*   Telegram X 现在基于[TD lib 1 . 4 . 0](https://core.telegram.org/tdlib)；
*   [删除私聊中两端的](https://telegram.org/blog/unsend-privacy-emoji)聊天&消息；
*   [投票](https://telegram.org/blog/polls):创建并参与社区投票；
*   [自定义语言](https://telegram.org/blog/translations-iv2):安装&共享语言包链接。在[翻译平台](https://translations.telegram.org/en/android_x/)上帮助将电报 X 翻译成您的语言；
*   多账户 2.0:完全重新设计的内部核心架构，以便在使用多个账户时大幅减少设备内存和电池的使用。现在，不管你在 Telegram X 中有 3 个还是 3000 个账户，它们将占用相似数量的资源，并且通知将对它们都起作用；
*   提高了应用程序的启动速度。请记住，更新 Telegram X 后的首次启动可能需要一段时间，因为它必须为每个帐户优化数据库；
*   应用程序恢复:每当 Telegram X 由于无法解决的错误而无法启动时，下次您启动应用程序时，您将看到恢复屏幕，这将有助于解决问题；
*   在保存的邮件和任何组中锁定邮件；
*   无需等待文件下载即可快速改变音频播放位置；
*   所有群组中的在线成员计数。改进了成员总数计算；
*   新的 2FA 电子邮件恢复设置代码；
*   改进的审查规避；
*   按类型过滤聊天；
*   复制私人组和频道中消息的链接；
*   远程擦除所有下载的媒体。

    当您从另一台设备注销或取消 Telegram X 会话时，所有下载的媒体也将被删除。当安装了 Google Play 服务后，Telegram X 和 TDLib 会尽力删除所有数据，而无需在设备上线后打开应用程序。如果你的设备丢失或被盗，这可能会有所帮助。你永远不知道这什么时候会发生，所以一定要保持 Telegram X 是最新的。

    注意这还不适用于通过“保存到多媒体资料/下载/音乐”按钮复制的媒体文件；
*   在“设置”>“隐私与安全”>“会话”中的准确登录和最后访问时间；
*   擦除所有数据:减少电报 X 磁盘空间使用。始终使用此选项，而不是注销并重新登录，重新安装应用程序或清除其数据。可在设置>数据和存储>存储使用>三点菜单中找到；
*   在存储使用中添加了新字段；
*   高级*点对点通话*设置与其他设备同步；
*   *联系人加入电报*通知设置现已与其他设备同步；
*   Telegram X 现在针对 x86 _ 64 CPUs 进行了优化；
*   会话列表中未完成的登录尝试；
*   向其他应用程序外部共享联系人；
*   从秘密聊天屏幕打开云聊天；
*   在网站会话列表中打开与机器人的聊天；
*   将 libtgvoip 更新至 2 . 4 . 4；
*   更好地处理登录和密码屏幕上的硬件键盘；
*   更好的超级组成员列表排序；
*   *选择表情符号语气时适用于所有*；
*   预览贴纸时，贴纸菜单出现后，您仍然可以移动手指查看其他贴纸；
*   密码即时自动锁定；
*   按住密码按钮以更改密码设置；
*   注销时的替代选项；
*   稍微改进了数据和存储、网络使用和存储使用屏幕的外观。

* * *

[**来源:电报**](https://telegra.ph/Telegram-X-04-25)