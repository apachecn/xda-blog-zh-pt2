# 任务周:利用 NFC 触发器！

> 原文：<https://www.xda-developers.com/tasker-week-everything-nfc/>

所以，你拿起了一些 NFC 标签或正在考虑这样做，但接下来呢？当然，你可以把它们设置为无聊的事情，比如存储你的 WiFi 密码或者用可信设备登录你的手机。或者你可以通过 Tasker 设置它们触发任何事情！

> 这里只是一些最好的和最有用的日常任务，您可以使用 Tasker 和 NFC 标签自动完成。

## 内容

[设置](#SU)

[唤醒局域网](#WOL)

[驾驶模式](#DM)

[显示自定义应用菜单](#DAD)

## 建立

[段落 _ 左侧]

以下所有 Tasker 配置文件都需要 NFC Tasker 插件；我使用并推荐 [Locale NFC 插件](https://play.google.com/store/apps/details?id=se.badaccess.locale.nfc&hl=en_GB)以方便使用。当然，每个配置文件还需要一个 NFC 标签。所有这些的第一步都是一样的，所以我现在只介绍一次。如果你正在使用 Locale，你可以通过写 **bad://access/development** 作为它的自定义 URL 来停止手机询问你想使用哪个应用程序来读取标签，这将确保只有 Locale 插件可以访问该应用程序。为此，我推荐使用 [NFC 工具](https://play.google.com/store/apps/details?id=com.wakdev.wdnfc&hl=en_GB)应用，整个过程只需几秒钟(见右图)。一旦你准备好你的标签，点击页面底部的+建立一个新的档案，然后点击状态>插件>区域 NFC 插件。最后，在新的屏幕上点击笔的配置和扫描您的标签，勾选“允许重复扫描”，你就可以开始了！

[/paragraph_left]

* * *

## 局域网唤醒

你回到家，很清楚要做的第一件事就是打开你的电脑，你必须等待它启动，但是如果你一进门电脑就打开了，准备好等你进去的时候再打开呢？以下是方法。

你需要一个网络唤醒任务插件，我再次使用并推荐[网络唤醒](https://play.google.com/store/apps/details?id=co.uk.mrwebb.wakeonlan&hl=en_GB)应用，它遵循材料设计，非常容易设置。安装完成后，打开应用程序并点击浮动操作按钮，这应该会开始显示与您相同网络上的所有设备，当您看到您想要唤醒的 PC 的 MAC 或 IP(可以在 Windows 中使用“ipconfig”命令在终端中找到)时，点击并命名它。回到 Tasker 添加一个新任务到你之前创建的配置文件，并添加一个新动作:插件>局域网唤醒，再次点击笔图标，选择你之前在应用程序中命名的 PC。您需要确保您的电脑在 bios 中启用了局域网唤醒功能，并最终将 NFC 标签放在门边。在我的情况下，它坐在我的钥匙碗旁边，这是我进屋后第一个去的地方。

* * *

## 驾驶模式

如果你的汽车上有手机支架或底座，你可以将 NFC 标签贴在它的背面，只要你将手机放在里面，它就会运行，只是要确保在设置标签时取消重复扫描。这个简介会因人而异，取决于他们的媒体和导航应用偏好，甚至取决于你的汽车是否内置蓝牙，但我会在这里分享我的，你可以根据需要进行调整。添加一个标签到一个新的配置文件，并选择新的任务，你会想要添加下面的，我已经分成三个部分在这里，使它更容易跟随:

**打开蓝牙和 GPS，关闭 WiFi** (这将需要[安全设置](https://play.google.com/store/apps/details?id=com.intangibleobject.securesettings.plugin&hl=en_GB)插件)

1.  Net > BlueTooth，然后在下拉列表中设置为 On，
2.  Net > WiFi，然后在下拉列表中设置为 Off，
3.  插件>安全设置>配置>系统+操作> GPS >打开>保存

**调高媒体音量**

1.  音频>媒体音量>选择您满意的音量

**选择目的地后，打开导航并选择媒体**

1.  应用程序>启动应用程序>地图(或您首选的导航应用程序)
2.  位置>获取位置
3.  插件>安全设置>配置>操作>启动活动>谷歌应用>[语音搜索]。语音搜索活动>保存

在新屏幕中，点击变量框中的+IF 和 type 4.4，然后选择~并将其更改为“Maths: Less Than”，最后选择 value 框并键入“%LOCSPD”。

这最后一个命令将等到你驾驶速度超过 4.4 米/秒(10 英里/小时)，然后启动 Google Now 活动，允许你说“Play <insert band="" playlist="" or="" song="" of="" your="" choice="" here="">”你可以将 4.4 变量更改为你选择的速度(单位是米/秒)，但请确保驾驶时保持安全。</insert>

* * *

[paragraph _ left]这将在屏幕上显示一个菜单，其中包含最适合您的应用程序，并且在充满电时会一直显示，将分配的标签放在您的桌子上，放在充电器够得着的地方，坐下时只需将手机插上电源，放在标签上。

**设置菜单覆盖图**

1.  提醒>菜单>向右滑动超时，直到显示“永不”
2.  布局>图标网格菜单
3.  项目>网格>应用程序图标>选择您选择的应用程序
4.  对所有需要的应用程序重复上述步骤

**充满电时保持显示屏打开**

1.  显示>显示超时>设置一个想要的时间，我用 4 小时
2.  如果> 100% = %电池

我发现这有助于我战胜拖延症，让我专注于工作所需的应用程序，选择一个应用程序将关闭菜单，直到你再次将手机放在标签上。

[/paragraph_left]

* * *

当然，你可以设置任何任务配置文件从 NFC 标签触发，这里只是我每天使用的几个。

请务必查看[XDA/安卓播客第 15 集:“轻扫一下，你就有了两个应用”](http://www.xda-developers.com/podcast-leeco-one-pro-giveaway/)有机会赢得 5 个 LeEco One Pro (SD810)中的一个！！！

**你和 Tasker 一起使用 NFC 标签吗？在**下方留下评论