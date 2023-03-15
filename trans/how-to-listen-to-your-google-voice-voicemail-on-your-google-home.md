# 如何在 Google Home 上收听您的 Google Voice 语音邮件

> 原文：<https://www.xda-developers.com/how-to-listen-to-your-google-voice-voicemail-on-your-google-home/>

当 Google Home 第一次发布时，它(现在仍然)缺乏许多功能。你仍然无法设置日历事件、阅读短信、创建待办事项列表等等。然而，如果你有勇气，你可以自己实现几乎所有这些功能，这要归功于 [AutoVoice](https://play.google.com/store/apps/details?id=com.joaomgcd.autovoice&hl=en) 和 [Tasker](https://play.google.com/store/apps/details?id=net.dinglisch.android.taskerm&hl=en) 的强大功能。为了展示你使用 Google Home 和 AutoVoice 的创造力，我将向你展示如何让你的 Google Home **阅读你最新的 Google Voice 语音邮件。现在这看起来像是巫术，但希望在本教程结束时，一切都会变得有意义。**

通过 AutoVoice，你可以从 Google Home 设备向手机发送语音命令，然后手机会解释这些命令并通过 Tasker 执行一些操作。最好的部分是，由于 [API.ai](https://api.ai/) 的力量，你可以向你的手机发送自然语言命令，前提是你向 AutoVoice 注册 0.99 美元/月的订阅服务，以抵消托管 API.ai 服务器的成本。这意味着当你对着你的 Google Home 说话时，你不必说得那么机器人化/精确，AutoVoice 仍然会识别你试图发送的命令。

一段时间以来，AutoVoice 与 Google Home 的集成一直处于测试阶段，但 AutoVoice 3.0 的[版本允许 Tasker 插件的所有用户享受 Google Home 集成。现在，AutoVoice 已经被用户广泛使用，并且它的大多数问题都已经解决，我将开始展示我用 AutoVoice 和 Tasker 做的一些东西。我的第一个谷歌主页教程，阅读你最新的谷歌语音邮件，是我最复杂的分享，但它是一个很好的候选人，表明你可以用 Tasker 做什么，只受你的想象力限制。](https://www.xda-developers.com/autovoice-3-0-brings-google-home-amazon-echo-ifttt-integration-and-natural-language-support-to-stable-channel/)

在我的谷歌主页上听我最新的语音邮件。

***推荐阅读:查看我们的[以前的教程](https://www.xda-developers.com/category/tutorials/)，在那里我们向你展示如何解决很少有人接触过的常见问题。***

* * *

### 要求

AutoVoice 是这个项目工作的软要求。您可以使用 IFTTT 来触发任务，但这将需要您使用一种变通方法，涉及另一个应用程序，如 [Join](https://play.google.com/store/apps/details?id=com.joaomgcd.join&hl=en) 或[push pullet](https://play.google.com/store/apps/details?id=com.pushbullet.android&hl=en)向 Tasker 发送命令，因为 IFTTT 不直接与 Tasker 集成。此外，不使用 AutoVoice 的最重要的警告是，如果使用 IFTTT，语音命令将是不灵活的。这意味着你必须每次都完全准确地说出你的命令，否则命令不会被触发。如果你开始创建大量的 Tasker/Google Home 集成(我目前有 28 个)，这在未来可能是一个问题，这意味着你每次都必须记住并准确再现你想要的命令。

* * *

## 准备

在我们开始讨论这个很酷的集成之前，我们必须为它的正常工作做一些准备。我将分几个部分来介绍这个设置。

### 第 1 部分-设置 AutoVoice

关于如何用 Google Home 设置 AutoVoice，我已经写了很长时间，所以请[在这里](https://www.xda-developers.com/autovoice-integration-finally-makes-its-way-to-google-home-heres-how-to-use-it/)参考我以前的文章。唯一值得注意的变化是，你不再需要 AutoVoice 测试版，因为集成现在与 AutoVoice 稳定更新一起工作。我还建议您通读关于使 Tasker 配置文件对 AutoVoice 命令做出反应的简短教程，因为我们将在这里做同样的事情。要点是，在这个设置过程中，您将做四件主要的事情:

1.  在 Google Home 应用中启用 AutoVoice 服务。
2.  设置一个 API.ai 帐户并获取您的 API 密钥
3.  将这些 API 键添加到 AutoVoice 的自然语言设置中
4.  订阅 AutoVoice 自然语言订阅服务

同样，这些步骤在我之前的文章中有更详细的描述，所以我建议您通读一遍。

### 第 2 部分-设置 Google Voice

我们需要一种方法来访问您的 Google Voice 语音邮件，以便 Tasker 可以提取语音邮件内容。我们将通过将我们所有的语音邮件转发到您关联的 Gmail 帐户来实现这一点。这是谷歌语音的原生功能，你需要做的只是在谷歌语音应用程序中切换一个按钮。

完成后，您将开始在电子邮件中接收所有新的语音邮件。如您所见，这封电子邮件既包含语音邮件的副本，也包含语音邮件实际音频的链接。我们将出于我们的目的使用此电子邮件。

### 第 3 部分-设置 AutoWeb

为了提取这封邮件的内容，我们需要使用 [Gmail API](https://developers.google.com/gmail/api/) 来访问邮件内容。我们将使用开头附近链接的 AutoWeb 应用程序来完成这项工作。打开 AutoWeb 并点击“浏览 Web 服务”向下滚动到 Gmail API，点击它进行导入。导入后，AutoWeb 会要求您对要使用 API 的 Gmail 帐户进行身份验证。选择将语音邮件转发到 的同一个 Gmail 帐户 **。**

现在，您已经通过使用 Gmail API 将您的手机链接到您的 Gmail 帐户！

### 第 4 部分-设置自动成本核算

在我们可以将语音邮件音频发送到我们的 Google Home 之前，我们需要设置 AutoCast，以便它可以连接到 Google Home。打开 AutoCast 并选择“管理演职人员设备”。点击顶部栏中的“ **+** ”图标，选择您的 Google Home 设备。

最后，我们已经准备好进行实际设置。

* * *

## 在谷歌主页上阅读您最新的谷歌语音邮件

### AutoVoice

我们需要做的第一件事是创建一个 AutoVoice 自然语言命令。这很容易做到。

1.  打开自动语音
2.  利用自然语言
3.  点击命令
4.  点击 **+** 图标添加新命令
5.  输入语音命令列表，用逗号分隔，包含您认为触发此命令时可以说出的语音命令的各种变体。
6.  对于响应，您可以输入尽可能多的响应，或者不输入任何响应，以便 Google Home 在您发出该命令时向您朗读。
7.  完成后，给这个命令命名。这里什么都行。

即使您正在输入一堆不同的命令和响应，您也不必担心要记住准确地说出这些命令。API.ai 将自动解析您所说的任何内容，并使用其自然语言算法将您所说的命令与您在此列出的命令进行匹配。

或者，如果你只是想下载我自己的设置，你可以在下面的链接。我相信，就目前而言，为了导入它，您必须登录 API.ai 并在那里导入它。

[**下载 AutoVoice 自然语言意图**](https://www.androidfilehost.com/?fid=529152257862710887)

老实说，这个设置的实际自动语音部分相当简单，因为我们不处理口头命令中的变量/参数或上下文。真正复杂的部分来自下一部分，我们让 Tasker 对这个 AutoVoice 自然语言命令做出反应。

### 包包包包包包包包包包包包包包包包包包包包包包包包包包包包包包包包包包包包包包包

这是我们制作这份简介的一步一步的指南。

1.  打开 Tasker，按下 **+** 图标，创建一个新的个人资料。
2.  进入事件->插件->自动语音->自然语言。
3.  点击铅笔图标打开 AutoVoice 的配置屏幕。
4.  按“命令”并选择您之前创建的命令的名称。
5.  按上面的勾号图标，然后按返回键返回到 Tasker 的主屏幕。
6.  Tasker 将要求您创建一个新任务。如果你愿意，你可以给它一个名字，但是不管怎样，点击勾号图标来创建一个新的任务。

进入任务编辑屏幕后，我们将创建如下所示的任务。要创建新动作，请点击底部中间的 **+** 图标。对于这里的任何 Tasker 专业人员，您可以展开下面的切换，以显示您自己可以关注的个人资料和任务描述。

### 家庭阅读语音邮件

```
  Profile: Home - Read Voicemail (165)
 Event: AutoVoice Natural Language [ Configuration:Commands: read my last voicemail ]
Enter: Read Voicemail (164)
 A1: AutoCast Speak [ Configuration:Device: Bedroom Home Timeout (Seconds):60 ] 
 A2: AutoWeb Web Service [ Configuration:API: Gmail
API Action: List messages
Include spam trash: false
User ID: me
Search: from:voice-noreply@google.com
Max Results: 5 Timeout (Seconds):120 ] 
 A3: Wait [ MS:0 Seconds:1 Minutes:0 Hours:0 Days:0 ] 
 A4: AutoWeb Web Service [ Configuration:API: Gmail
API Action: Get Message
Format: full
User ID: me Timeout (Seconds):120 ] 
 A5: For [ Variable:%headers Items:1:%payload_headers_name(
 A6: Variable Set [ Name:%reference To:%headers Recurse Variables:Off Do Maths:Off Append:Off ] If [ %payload_headers_name(%headers) ~ Subject ]
 A7: End For 
 A8: Java Function [ Return:decodedbody Class Or Object:Base64 Function:decode
{byte[]} (String, int) Param:%bodydata(1) Param:8 Param: Param: Param: Param: Param: ] 
 A9: Java Function [ Return:%body Class Or Object:String Function:new
{String} (byte[], String) Param:decodedbody Param:UTF-8 Param: Param: Param: Param: Param: ] 
 A10: Variable Split [ Name:%body Splitter:https://www.google.com/voice/fm/ Delete Base:Off ] 
 A11: Variable Split [ Name:%body2 Splitter:> Delete Base:Off ] 
 A12: HTTP Get [ Server:Port:https:
 A13: Variable Set [ Name:%voicemail To:%payload_headers_value(%reference) Recurse Variables:Off Do Maths:Off Append:Off ] 
 A14: Variable Split [ Name:%voicemail Splitter:from Delete Base:Off ] 
 A15: Variable Split [ Name:%voicemail2 Splitter:at Delete Base:Off ] 
 A16: Test Phone [ Type:Contact Name Data:%voicemail21 Store Result In:%name Continue Task After Error:On ] 
 A17: Variable Set [ Name:%voicemail To:%voicemail1 from %name at %voicemail22 Recurse Variables:Off Do Maths:Off Append:Off ] If [ %name Set ]
 A18: Variable Set [ Name:%voicemail To:%voicemail1 from %voicemail21 at %voicemail22 Recurse Variables:Off Do Maths:Off Append:Off ] If [ %name !Set ]
 A19: AutoCast Speak [ Configuration:Device: Bedroom Home
Text: %voicemail Timeout (Seconds):60 ] 
 A20: Wait [ MS:0 Seconds:5 Minutes:0 Hours:0 Days:0 ] 
 A21: AutoCast [ Configuration:
Starting Casting Screen
Persistent Notification: true
Cast Device: Bedroom Home
Screen: Full Screen Media
Audio: /storage/emulated/0/Tasker/voicemail.mp3
Audio Volume: 100
Audio Position: 0
Audio AutoPlay: true Timeout (Seconds):3000 ] 
```

下面的分步指南将向您展示如何复制右侧屏幕截图中显示的任务。这个任务是这个设置的核心，相当复杂。它的工作原理是，一旦激活该配置文件，最初的几个操作(A2-A4)会从您的 Gmail 帐户中搜索并提取来自 voice-noreply@google.com 的邮件，这是 Google Voice 使用的自动电子邮件服务。然后我们寻找主题头(A5-A7 ),这样我们就可以得到谁在何时发送了语音邮件的信息。接下来，我们提取 Gmail 邮件的邮件正文，邮件正文以 base 64 编码，因此我们必须使用 Java 函数(A8-A9)。在我们检索到解码后的消息后，我们接着寻找将我们链接到语音邮件音频文件(A10-A11)的 URL，并最终将该文件下载为 mp3 (A12)。A13-A18 简单地查找留下语音邮件的号码的联系信息(如果存在的话)。最后，A19-A21 将读出语音邮件是在什么时间由谁发送的，以及记录的语音邮件音频。

1.  插件->自动发布->自动发布语音。设备:**选择你的谷歌主页。**(这里不需要任何文字，这只是为了连接到 Google Home。)
2.  插件- > AutoWeb。API: Gmail。API 操作:列出消息。用户 ID:我。搜索:**from:voice-noreply@google.com**。最大结果:5。输出: **Id。**
3.  任务->等待。等待 1 秒钟。
4.  插件- > AutoWeb。API: Gmail。API 操作:获取消息。格式:全。用户 ID:我。消息 ID: **%aid(1)** 。输出:**主体数据，有效载荷头名称，**和**有效载荷头值。**
5.  任务->用于。变量:**%头**。项目:**1:%有效负载标题名称(#)**
6.  变量->变量集。名称:**%引用**。致: **%headers** 。检查 If 并将其设置为 If**% payload _ headers _ name(% headers)~ Subject。**
7.  任务->结束。
8.  代码- > Java 函数。对于类/对象，选择 **Base64。**功能:**解码{byte[]} (String，int)** 。Param (string): **%bodydata(1)。** Param (int): **8。**返回: **decodedbody。**
9.  代码- > Java 函数。对于类/对象，选择**字符串。**函数: **new {String} (byte[]，String)** 。param(byte[]):**decode body。** Param (string): **UTF-8。**返回:**%体。**
10.  变量->变量拆分。名称:**%体。**拆分器:【https://www.google.com/voice/fm/】T2
11.  变量->变量拆分。名称: **%body2** 。拆分器: **>**
12.  Net - > HTTP Get。服务器:端口:**https://www.google.com**路径: **/voice/fm/%body21** Mime 类型: **audio/*** 输出文件:**/SD card/Tasker/voice mail . MP3**
13.  变量->变量集。姓名:**%语音邮件**。收件人:**%有效负载标题值(%参考)**
14.  变量->变量拆分。姓名:**%语音信箱。**拆分器:中的
***   变量->变量拆分。姓名: **%voicemail2** 。分割器:**在***   电话->测试电话。类型:**联系人姓名。**数据: **%voicemail21** 。将结果存储在: **%name。**出错后，确保检查**继续任务。***   变量->变量集。姓名:**%语音邮件**。收件人: **%voicemail1 发自%name 于%voicemail22** 。检查底部的 if，并将其设置为是否设置了 **%name。***   变量->变量集。姓名:**%语音邮件**。收件人: **%voicemail1 发自%voicemail21，时间为%voicemail22** 。在底部检查是否，如果没有设置 **%name，将其设置为。***   插件->自动发布->朗读。设备:**选择你的 Google Home** 。正文:**%语音信箱***   任务->等待。等待 **5 秒钟。**这是一个**可配置的延迟**，以确保在宣布新语音邮件和播放语音邮件音频之间总是有足够的时间。如果这个太短，可以增加这个时间。不过，可以试验一下这个值，看看怎样将延迟降低到可接受的水平。*   插件->自动发布->自动发布。Cast Device: **再次挑选你的 Google Home。**选择**全屏媒体**作为屏幕。转到全屏媒体元素，然后音频，对于音频(“要播放的歌曲”)，将**/SD card/Tasker/voice mail . MP3**。选择**自动播放**。**

 **就是这样！现在，你需要做的就是发送命令到你的 Google Home 设备来触发这个任务。你可以说“ ***”嘿/好的谷歌，让我和 AutoVoice*** ”然后当 AutoVoice 告诉你说你的命令时，说出你的命令的一个变体。或者你可以说“ ***嘿/OK 谷歌，问 AutoVoice 到【命令】*** ”就像我在开头展示的视频中做的那样，一口气说出你的命令。

* * *

## 下载个人资料

你可以从下面的链接下载我制作的任务简介/任务。如果您选择这样做，请确保您进入并修改两个“自动发布”操作，以便它们引用您的特定 Google Home 设备。此外，检查以确保在我的个人资料中命名的 AutoVoice 自然语言命令与您创建的命令相同。如果没有，只需更改配置文件以指向您的命令。应该只需要几秒钟。

[**下载首页阅读语音邮件任务者简介**](https://www.androidfilehost.com/?fid=817550096634754127)

下载上述 XML 文件后，将其保存在设备上的任何地方。打开 Tasker，在首选项中禁用初学者模式。然后返回主屏幕，长按 Profiles 选项卡，直到您看到一个弹出框，其中有一个“导入”选项。按下该按钮，导航到保存. prf.xml 文件的位置，并选择要导入的文件。

我希望这个教程对你有用。我喜欢摆弄 API 和 Tasker，直到我能够让事情正常工作。我知道这不是超级优雅，但这主要是一个展示，你可以如何有力地将你的谷歌主页与各种网络服务和你的手机集成。希望这能激发你创造一些你以前认为不可能的东西！**