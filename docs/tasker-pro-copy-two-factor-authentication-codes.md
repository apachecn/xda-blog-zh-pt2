# Tasker Pro:复制双因素认证码，无需更换应用程序！

> 原文：<https://www.xda-developers.com/tasker-pro-copy-two-factor-authentication-codes/>

自动化应该是简化日常任务，让你有更多宝贵的时间做自己喜欢的事情。在 XDA，我们已经向你展示了如何使用 Tasker 来[保护你的设备](http://forum.xda-developers.com/u/tasker-tips-tricks/guide-send-sms-address-speed-url-map-pin-t3330371)、[提高生产力](http://forum.xda-developers.com/u/tasker-tips-tricks/guide-read-google-calendar-events-day-t3332783)或[让驾驶更安全](http://forum.xda-developers.com/u/tasker-tips-tricks/guide-driving-mode-answer-calls-texts-t3332004)，这些都是我们系列的一部分，叫做“ **[Tasker Week](http://www.xda-developers.com/xda-tasker-week-in-review/)** 。”

但是乐趣并没有就此结束。如果你一直渴望**一些非常棒的 Tasker 任务**(并且厌倦了*无聊的*东西，比如告诉你如何重启手机或者摇动手机来唤醒显示屏)，那么我们新的 [Tasker Pro 系列](http://xda-developers.com/tag/tasker-pro)就是为你准备的。

我们将发布一系列**高度先进的** Tasker 简介，向你展示 Tasker 有多强大，如果你愿意跳出框框思考的话。虽然我们已经为您做了大部分艰苦的工作，您当然可以自由地导入我的个人资料并按原样使用它们，但如果您想自己定制这些任务，我强烈建议您尝试一下如何使用 Tasker。在我们的 [Tasker Tips & Tricks](http://forum.xda-developers.com/u/tasker-tips-tricks/guide-automatically-check-md5-sum-t3365590/post66531924#post66531924) 论坛上或者在 Reddit 的/r/Tasker subredit 上，你可以与他人分享和合作如何实现你可能有的想法(正如[我已经做了很多次](http://forum.xda-developers.com/u/tasker-tips-tricks/guide-automatically-check-md5-sum-t3365590/post66531924#post66531924))。

这是 Tasker pro 的第**周第 4** 。[上周](http://www.xda-developers.com/tasker-pro-tag-new-photos-with-the-current-calendar-event/)，我们向您展示了如何使用 Tasker 自动为所有拍摄的新照片添加正在进行的日历事件的标题。本周，我们将向您展示如何在不离开您的应用程序的情况下**复制通过短信发送的双因素认证码！**

* * *

**Tasker Pro #4:复制双因素认证码**

如今，随着如此多的密码数据库被攻破，许多想让自己的在线账户更加安全的人选择在其服务中启用双因素身份认证。服务如何实现向您发送双因素认证码因服务而异(短信、电子邮件、认证应用等)。所以很不幸，你只能依靠你注册的服务所允许的任何方法。对于许多许多通过短信发送 2FA 代码的服务来说，必须打开你的短信应用程序来复制代码可能会有点麻烦(在糟糕的编码应用程序中，应用程序甚至可能在你可以粘贴 2FA 代码之前就关闭了！)

在这种情况下，我们可以使用 Tasker 来**拦截短信**并在你当前使用的任何应用程序上显示一个**短吐司或小吃条**的代码！你可以按一个按钮让**复制到你的剪贴板**，在 **15 秒**后你的剪贴板会自动清空。

* * *

**要求**

以下是可选的，但是，如果您想要完全复制我的设置(或者只是导入我的脚本)，那么您需要安装这两个插件:

* * *

**指令**

在我们开始之前，此脚本需要对您的联系人列表进行一些更改。为了让此脚本检测某些机构何时发送短信，您需要事先将他们命名为联系人。例如，如果你收到来自 PayPal 的 2FA 短信，那么你会想给那个联系人起个名字，这样 Tasker 就能识别出信息来自哪里。但是最重要的部分是:**你需要在每个联系人的名字前加上同一个单词，这样对于 Tasker 来说就简单多了。**在我的例子中，我将我的每个联系人命名为“**验证*”**，其中*是 PayPal、LinkedIn 等。这样，Tasker 可以解析出名称的“验证”部分，以获得发送 2FA SMS 的实际机构。

这是您将要制作的个人资料的概述。这实际上很简单，但是我们将为您更详细地分解它。你需要做的第一件事是创建一个新的**事件配置文件**，它在收到**短信时触发。**对于联系人姓名，将其设为**验证*** ，这意味着任何包含“验证”一词的联系人都将触发此配置文件，因此这意味着任何您明确命名为“验证”的联系人。将正文部分留空，因为每个机构发送不同的正文，我们无法立即在档案中找到。

现在，让我们来看看您需要为此档案采取的措施:

1.  **可选**:插件- >自动通知- >自动通知查询。将其设置为查询短信应用程序发送的通知。这并不是真正需要的，但它可以帮助我们拦截并自动取消您的短信应用程序发送的通知，从而节省您的一些时间，因为我们已经在与它进行交互了。
2.  变量->变量集。将**%剪辑**设置为**%剪辑。**将当前消息保存在剪贴板中，以防我们选择复制 2FA 代码。
3.  变量->变量集。将 **%text** 设置为 **%SMSRB。**将文本消息正文保存在变量中。
4.  变量->变量集。将中的**%设置为 **%SMSRN。**将联系人姓名设置为变量。**
5.  变量->变量搜索替换。变量: **%text** 。搜索: **\d{3，}** 点击“**多线**”、“**一次只匹配**”，将匹配结果存储在**%代码中。**这将在文本消息正文中搜索长度为 3 个字符或更长的任何数字字符串，应该是 2FA 代码。它会将所有结果存储在一个变量中，该变量应该只有一个匹配项。
6.  **可选:**插件- >自动通知- >自动通知取消。其他 Id: **%anid。**包装:**% an 包装。**标签: **%antag。**这将关闭来自你的短信应用程序的通知。
7.  **可选:**插件- > Snackbar Tasker 插件- >带按钮的 Snackbar。消息:**%发件人:%code1** 。按钮:**复制。**命令:**复制。**检查是否设置了 **%code1。仅当找到 2FA 代码时，这将显示一个带有您的代码的 snackbar，并给你一个复制文本的按钮。**
8.  **可选:**系统- >设置剪贴板。正文: **%code1** 。检查是否并使其 **%sb_command ~副本**。如果您愿意，这将把代码复制到您的剪贴板。
9.  **可选:**插件- > Snackbar Tasker 插件- >无按钮 Snackbar。消息:**复制到剪贴板，15 秒后清除...**
10.  **可选:**任务- >等待。等待 15 秒钟。等到你清空剪贴板的时间。
11.  **可选:**系统- >设置剪贴板。正文:**%剪辑。**这将恢复您的剪贴板。
12.  **可选:**插件- > Snackbar Tasker 插件- >无按钮 Snackbar。消息:**剪贴板恢复。**

如果您不想使用 Snackbar Tasker 插件，那么您可以复制第 7 步中的消息，并使用 Alert - > Flash 显示一条 toast 消息。

* * *

瞧，瞧！如果你能理解这一点，那么恭喜你，你已经是一个任务大师了！迷茫于一个步骤，只想导入脚本，继续自己的生活？我不能责怪你，这一次我花了很多时间才把它写好。

**如果你想导入这个档案，你可以[在这里](https://www.androidfilehost.com/?fid=24572369242685927)从 Android 文件主机下载。**为了导入任务，您需要首先在 Tasker 中禁用初学者模式，进入菜单- >偏好设置。在 UI 选项卡下，取消选中“初学者模式”然后回到主任务菜单，点击“任务”标签。然后长按“任务”标签并按“导入”导航到下载 my .prf.xml 文件的位置，并选择要导入的文件。一旦你导入了它，你就可以随意使用它了。

在下周的 Tasker Pro 中，我将向你展示如何**确保你在早上总是准备好闹钟，并禁用任何你不小心设置的闹钟，从而避免职场尴尬！**

[**Check out all Tasker Pro scripts!**](http://www.xda-developers.com/tag/tasker-pro/)

* * *

你想看我和 Tasker 一起做什么？请在下面告诉我们，我们可能会在未来的文章中重点介绍您的想法！