# Tasker Pro:使用您的指纹解锁您的 Windows PC！

> 原文：<https://www.xda-developers.com/unlock-windows-pc-using-fingerprint/>

自动化应该是简化日常任务，让你有更多宝贵的时间做自己喜欢的事情。在 XDA，我们已经向您展示了如何使用 Tasker 来[保护您的设备](http://forum.xda-developers.com/u/tasker-tips-tricks/guide-send-sms-address-speed-url-map-pin-t3330371)、[提高生产力](http://forum.xda-developers.com/u/tasker-tips-tricks/guide-read-google-calendar-events-day-t3332783)或[让驾驶更安全](http://forum.xda-developers.com/u/tasker-tips-tricks/guide-driving-mode-answer-calls-texts-t3332004)，这些都是我们名为“ **[Tasker Week](http://www.xda-developers.com/xda-tasker-week-in-review/)** ”系列的一部分

但是乐趣并没有就此结束。如果你一直渴望**一些非常棒的 Tasker 任务**(并且厌倦了*无聊的*东西，比如告诉你如何重启手机或者摇动手机来唤醒显示屏)，那么我们新的 [Tasker Pro 系列](http://xda-developers.com/tag/tasker-pro)就是为你准备的。

我们将发布一系列**高度先进的** Tasker 简介，向你展示 Tasker 有多强大，如果你愿意跳出框框思考的话。虽然我们已经为您做了大部分艰苦的工作，您当然可以自由地导入我的个人资料并按原样使用它们，但如果您想自己定制这些任务，我强烈建议您尝试一下如何使用 Tasker。在我们的 [Tasker Tips & Tricks](http://forum.xda-developers.com/u/tasker-tips-tricks/guide-automatically-check-md5-sum-t3365590/post66531924#post66531924) 论坛上或者在 Reddit 的/r/Tasker subredit 上，你可以与他人分享和合作如何实现你可能有的想法(正如[我已经做了很多次](http://forum.xda-developers.com/u/tasker-tips-tricks/guide-automatically-check-md5-sum-t3365590/post66531924#post66531924))。

这是 Tasker pro 的第**周第 6** 周。[上周](http://www.xda-developers.com/tasker-pro-calendar-based-alarm/)，我们向你展示了如何使用 Tasker 创建一个基于日历的闹钟，让你永远不会错过工作。本周，我们将向您展示如何使用从 Android 手机读取的指纹来**解锁您的 Windows PC(包括您的桌面)!**

* * *

**Tasker Pro #6: Windows 指纹解锁**

假设您坐在楼下的沙发前，想要开始观看存储在 Plex 服务器上的电影。除了，糟糕，你忘了打开电源。没问题，你只需要去手动打开它，但是谁愿意离开一个舒适的沙发去做这件事呢？或者，对于那些设置了局域网唤醒功能的用户来说，虽然他们可以通过唤醒电脑来达到他们的目的，但是仍然需要你坐下来手动登录。谁想这么做？对于我们当中的懒人来说，这里有一个简洁的 Tasker 脚本，可以让你只使用指纹解锁你的 Windows PC。见鬼，你甚至可以修改这个脚本来解锁你的电脑，而不需要你的指纹，如果这是你想要的。

现在我意识到，我们当中更有安全意识的人可能会对这个想法感到恼火。这肯定不太安全，对吧？我已经考虑了这里可能存在的安全漏洞，归根结底，您的 Windows 密码可能被泄露的唯一方式是:

*   你的家庭 WiFi 网络被破坏了(在这种情况下，你有*许多其他事情*要担心)。
*   你的手机在物理上受到了损害，攻击者可以接触到手机(在这种情况下，你有*许多其他事情*要担心)。

所以，是的，这种方法确实可以通过你的家庭网络以纯文本的形式发送你的密码。然而，这将需要一些非常特殊的情况下，你的 Windows 密码被这个设置所破坏。为了防止用户在共享他们的 Tasker 设置时意外地共享他们的 Windows 密码，我把它设置成你的实际 Windows 密码以加密状态存储在 Tasker 变量中。因此，唯一的方法，有人可以提取你的 Windows 密码再次是，如果他们有物理上完全进入你的手机。

无论如何，让我们继续 Tasker 脚本，好吗？下面是自动工具对话框，每当您启动任务时都会出现。成功扫描您存储的指纹后，Unified Remote 将触发必要的操作来解锁您的电脑。这实际上很简单 Unified Remote 所做的就是打开密码框并粘贴密码。

* * *

**要求**

* * *

**指令**

您需要做的前两件事是在您的设备上设置指纹(如果您还没有这样做的话)(AutoTools 使用 Android 上的原生指纹认证 API)并在您的 Windows PC 上安装统一远程服务器应用程序。然后，打开手机上的统一远程应用程序，找到您的计算机的名称/IP 地址，并保存服务器(它将显示在服务器菜单中的**保存的服务器**下)。一旦你完成了，我们将需要做一个快速的 3 个动作的任务，在 Tasker 中加密你的 Windows 密码，这样你就不会意外地分享它。

创建一个新任务，并给它起一个任意的名字。我们不会保留该任务，我们只会运行一次，然后立即删除该任务。这个任务所要做的就是设置您的加密密码，并将其存储在一个全局变量中。

1.  变量->变量集。名称: **%pass** 到 **YOURWINDOWSPCPASSWORD** 。这是你的密码，你应该知道它是什么。如果你用的是大头针，把它放进去。
2.  插件->自动工具->自动工具文本。正文:**%通过。**转到 Encryption，将它设置为加密通行证，并为加密密码设置一些任意短语。你将需要**记住**这个短语或者把它设置为一个全局变量，因为当你在主任务中解密密码时你将需要这个密码。
3.  变量->变量集。名称: **%EncryptedPass** 到 **%attextresult()** 。这将把加密的密码存储在一个全局变量中。

设置后运行一次该任务，然后将其删除。你将不再需要这个任务，除非你清除 Tasker 的数据/重新安装应用程序，在这种情况下，你的全局变量被清除。如果发生这种情况，您可以很容易地创建这个任务并再次运行它来创建一个新的加密密码。无论如何，我们接下来将深入到主要任务本身。

创建一个任务，将其命名为类似于**指纹解锁**的名称。

1.  插件->自动工具->自动工具对话框。选择**指纹对话框**。标题: **PC 指纹解锁。**尝试次数: **1。**失败消息:**错误:无法识别指纹。你可以根据自己的喜好定制其他任何东西。**
2.  插件->自动工具->自动工具文本。Text: **%EncryptedPass。**变量名: **%pass。**进入加密，选择**解密。**对于密码，使用您之前设置的加密密码。
3.  Net ->浏览 URL。URL:**ur://intent/remote:Core。键盘/操作:按/extra:space/destination:yourpcname here**
4.  任务->等待 1 秒钟。
5.  Net ->浏览 URL。URL:**ur://intent/remote:Core。键盘/操作:text/extra:% pass/destination:yourpcname here**
6.  任务->等待 1 秒钟。
7.  Net ->浏览 URL。URL:**ur://intent/remote:Core。键盘/操作:按/extra:enter/destination:yourpcname here**

基本上，这个任务所做的就是解密你存储的密码(动作 2)，然后按空格键，Windows 8/10*锁屏被关闭，最后在动作 7 中粘贴密码。在每个统一远程步骤之间有 1 秒钟的等待操作，以便有时间清除 Windows 动画并准备好文本框。现在，你可能已经注意到 Unified Remote 有一个 Tasker 插件，所以你可能想知道为什么我们不直接使用它。不幸的是，统一远程 Tasker 集成(我相信这是一个付费功能)不允许您传递 Tasker 变量，所以我们无法发送密码。至少，它对我不起作用。

**Windows 7 用户，您将需要更改此设置，使其按 CTRL+ALT+DEL，您可以通过打开应用程序并转到键盘遥控器，然后单击右下角的电话图标，在 Unified Remote 中捕捉 URI。点击“创建 URI 字符串”,并按照指示，直到你看到一个 URI 字符串，你可以放在这里。*

* * *

瞧，瞧！如果你能理解这一点，那么恭喜你，你已经是一个任务大师了！迷茫于一个步骤，只想导入脚本，继续自己的生活？我不能责怪你，这一次我花了很多时间才把它写好。**但是，请记住，你将需要设置如上所述的加密密码，因为这是一个任务，你创建然后立即删除。**

**如果你想导入这个 Tasker 脚本，可以从 [Android 文件主机](https://www.androidfilehost.com/?fid=24572369242687714)下载。**为了导入任务，您需要首先进入菜单- >偏好设置，禁用 Tasker 中的初学者模式。在 UI 选项卡下，取消选中“初学者模式”然后回到主任务菜单，点击“任务”标签。然后长按“任务”标签并按“导入”导航到下载 my .prf.xml 文件的位置，并选择要导入的文件。一旦你导入了它，你就可以随意使用它了。你可以通过创建一个启动器快捷方式来启动这个任务，你可以创建一个 Zooper 小部件，或者，如果你想将这个任务导出为一个应用程序，你可以安装 [Tasker 应用程序工厂](https://play.google.com/store/apps/details?id=net.dinglisch.android.appfactory&hl=en)。

下周我将向你展示如何**改变你的音量摇杆行为，只控制媒体音量而不是铃声音量！**

[**Check out all Tasker Pro scripts!**](http://www.xda-developers.com/tag/tasker-pro/)

* * *

你想看我和 Tasker 一起做什么？请在下面告诉我们，我们可能会在未来的文章中重点介绍您的想法！