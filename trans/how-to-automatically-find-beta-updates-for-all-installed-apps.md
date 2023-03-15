# 如何自动查找所有已安装应用的测试版更新

> 原文：<https://www.xda-developers.com/how-to-automatically-find-beta-updates-for-all-installed-apps/>

Android 应用的 Beta 测试渠道是用户提前几周或几个月测试最新功能的最佳方式，也是开发者在向所有人推出其功能之前在较小的受众中测试其软件的最佳方式。谷歌曾经让注册测试版更新成为一种极其令人沮丧的体验。你首先要加入一个专门针对该应用的 Google+社区，等待 Google+社区的版主批准(如果是封闭群的话)，最后等待谷歌的服务器将你的账户注册到该应用的测试频道。

虽然这可能是一种确保普通用户不会卷入他们并不真正致力于的测试程序的方法，但 Google+帐户的要求很麻烦。最终，谷歌开始允许用户直接从谷歌 Play 商店注册测试版更新，尽管这个按钮并不是对所有有测试版频道的应用都可用。

此外，尽管测试版的注册过程比过去容易得多，但你怎么知道哪些应用有测试版呢？你可以做的一件事是在 Play Store 中打开你已安装的应用列表，向下滚动到你已安装的每个应用的页面底部，看看是否有测试版，但这很糟糕，原因有两个。首先，正如上面 Whatsapp 的例子所示，并不是每个应用的测试版都可以从 Play Store 界面访问。其次，也是最重要的一点，**手动检查每一个应用程序需要很长时间。**

我安装了 280 个应用程序(包括系统应用程序)，所以我不可能在 Play Store 中手动查找测试程序。我加入的大多数测试程序都是出于需要，例如使用仅在 [AutoApps 测试版](https://joaoapps.com/beta-testing/)中提供的功能，或者当有人在社交媒体上链接测试程序时。我们中的许多人每天都在使用大量的应用程序，测试版可能会有我们现在错过的非常棒的功能。但是，我们没有人愿意费心从我们安装的大量应用程序中筛选出我们有资格进行 beta 测试的应用程序。这就是为什么我想出了一个自动化的脚本来为你做这件事。介绍**寻找测试版**任务脚本！

正如你在上面的截图中看到的，我的脚本创建了一个**应用程序列表**，我已经**在我的设备上安装了**，我是**目前有资格注册测试版更新**。这个列表是以 HTML 文件的形式创建的，这意味着它可以在 Chrome 等浏览器中打开，这样你就可以点击链接并逐个注册测试版。通过使用此列表，您将减少手动查找和注册所有已安装应用的测试版更新所需的时间和精力。此外，您还会发现一些您甚至不知道存在的应用程序的测试渠道，甚至是原始设备制造商预装的系统应用程序！

* * *

## 为所有已安装的应用程序查找合格的测试程序

当我说有资格时，我指的是你的 Google 帐户实际上可以注册的测试程序。不是每个 app 都有测试版程序，也不是每个 app 的测试版程序都允许你加入。你是否能加入一个测试程序取决于开发者，但是如果你有资格加入一个测试程序，这个脚本将帮助你找到它。

我们需要 Tasker 的原因很明显:这个脚本就是用它构建的。我们需要 AutoTools(尤其是 beta 版),因为它提供了一个名为 HTML read 的功能，允许我们从网页中提取原始 HTML 数据。本质上，我们要做的是从 Play Store 测试程序中为我们安装的每个应用程序提取 HTML，并使用一些 HTML 解析魔法来查看页面上的文本是否表明有测试频道可用。如果是，我们记录应用程序名称并将其添加到我们的列表中。

与之前的教程不同，这个脚本不涉及任何类型的概要文件，因为没有什么可以“触发”它。这个脚本只是一个单独的任务，因为它很少由用户手动运行。我将向您展示如何创建任务，但对于那些 Tasker 的专业人员来说，您可以通过展开下面的切换按钮来查看任务描述。

### 查找测试任务任务

```

Find Betas (209)
<<strong><h2>This script was made by XDA-Developers.com</h2></strong>
<h3><font color="red">Before running this script, you need to authenticate AutoTools. Open this Action's configuration and tap on "Authenticate" at the bottom.</font></h3>>
A1: [X] AutoTools HTML Read [ Configuration:URL: https://accounts.google.com/ServiceLogin?service=googleplay&passive=86400&continue=https%3A%2F%2Fplay.google.com%2Fstore#identifier Timeout (Seconds):60 ]
A2: List Apps [ Type:Package Match: Store Result In:%packages ]
A3: Flash [ Text:You have %packages(
A4: For [ Variable:%package Items:%packages() ]
A5: AutoTools HTML Read [ Configuration:URL: https:
CSS Queries: html > body > main > div:nth-child(2) > p:nth-child(1),html body main div h1
Variable Names: invite,name Timeout (Seconds):60 ]
A6: Test App [ Type:Package Name Data:%package Store Result In:%appname ]
A7: AutoTools Text [ Configuration:Text: %invite
Joiner Variable: atjoinedtext
Match Text: has invited you to a testing program for an unreleased version
Separator: π Timeout (Seconds):60 ]
A8: Array Push [ Variable Array:%betas Position:1 Value:%appname---%package Fill Spaces:Off ] If [ %atmatches() ~ true ]
A9: End For
A10: Array Process [ Variable Array:%betas Type:Sort Alpha ]
A11: For [ Variable:%betatest Items:%betas() ]
A12: Variable Split [ Name:%betatest Splitter:--- Delete Base:Off ]
A13: Write File [ File:/sdcard/Tasker/Beta_Test_List.html Text:<a href="https://play.google.com/apps/testing/%betatest2">%betatest1</a>
 Append:On Add Newline:On ]
A14: End For
A15: Open File [ File:Tasker/Beta_Test_List.html Mime Type:text/html ]

```

### 设置

在我们开始列出一步一步的指南之前，您需要完成一个只需要运行一次的简单设置过程(除非您卸载或清除自动工具的数据)。因为检查你是否有资格参加某些 Play Store 测试版程序需要验证你的 Google 帐户来提取信息，所以我们必须验证自动工具。幸运的是，这很容易做到。

打开 Tasker，创建一个名为 **Find Betas** 的新任务(或者随便你怎么称呼它)。创建一个新动作，然后进入**插件- >自动工具- > HTML Read** 。按铅笔图标打开自动工具的配置屏幕。对于**网址**，输入以下地址

```
https://accounts.google.com/ServiceLogin?service=googleplay&passive=86400&continue=https%3A%2F%2Fplay.google.com%2Fstore#identifier
```

完成后，向下滚动到配置屏幕的底部，点击**认证**。你将被引导到一个谷歌登录屏幕，通过你的帐户访问 Play Store。使用您用来下载所有应用程序的 Google 帐户登录。到达 Play Store 登录页面后，点击后退按钮退出配置屏幕。现在，AutoTools 已经通过了正确的身份验证，所以它现在可以在登录到您的帐户时从 beta 测试登录页面中调出。

### 向导

现在，这里有一个逐步的指导来完成这个任务。注意:这里的一些步骤相当高级。我不打算详细解释每件事是如何工作的，但我会给出每个步骤如何工作的概述。

1.  **应用- >列出应用。**类型:**包**。储存结果于:**%套餐**。这将列出所有已安装的软件包，并将它们存储在一个数组中。
2.  **任务- >为。**变量:**%包**。物品:**%包()**。这将一个接一个地遍历所有已安装的包。
3.  **插件- >自动工具- > HTML 读取。【https://play.google.com/apps/testing/%package】网址:**T2**。变量名: **invite，name** 。CSS 查询:`html > body > main > div:nth-child(2) > p:nth-child(1),html body main div h1`。这将读取当前包的测试登录页面，并将页面文本存储在一个变量中。**
4.  **App - >测试 App** 。类型:**包名。**数据:**%套餐**。将结果存储在: **%appname** 中。获取与当前包关联的应用程序名称。
5.  **插件- >自动工具- >文本**。正文:**%邀请**。匹配文本:**邀请你参加一个未发布版本**的测试项目。分隔符: **π** 。检查测试登录页面上显示的文本，看看它是否说有一个我们可以注册的测试频道。
6.  **变量- >数组推送**。变量数组:**% beta**。位置: **1** 。值: **%appname - %package** 。检查 if 并将其设置为 if**% at matches()**~**true**。如果有合格的测试版，将其添加到数组中。
7.  **任务- >结束为**。
8.  **变量- >数组过程。**变量数组:**% beta**。类型:**排序 alpha** 。按字母顺序重新排列名单。
9.  **任务- >为**。变量: **%betatest** 。物品:**% beta()**。
10.  **变量- >变量拆分。**名称: **%betatest** 。分割器: **-**
11.  **文件- >写文件**。文件:**/SD card/Tasker/Beta _ Test _ list . html**。正文:`<a href="https://play.google.com/apps/testing/%betatest2">%betatest1</a><br>`勾选**追加**和**添加换行**。
12.  **任务- >结束为**。
13.  **文件- >打开文件**。文件:**Tasker/Beta _ Test _ list . html**。Mime 类型: **text/html** 。

我被告知您将需要根据您的地区在步骤#5 中修改匹配文本。例如，英语(加拿大/英国)需要将“program”改为“program”。其他语言同样需要打开一个示例 beta 测试页面，并复制您的语言中显示的文本作为匹配文本。

这个剧本到此为止。你需要做的就是按下运行按钮(左下角的播放图标)让脚本运行。根据您安装的应用数量，可能需要 1-2 分钟才能完成。当任务通过 for 循环时，你会看到屏幕上下摆动，但只要你在开始时验证了 AutoTools，它就会结束并要求你使用普通的 HTML 查看器或浏览器应用程序打开 HTML 文件。

* * *

## 下载并导入

和往常一样，如果您想立即尝试一下，我们会提供导入该脚本所需的文件。下载下面的. tsk.xml 文件，并将其保存在内部存储的任何位置。打开 Tasker，在首选项中禁用初学者模式。回到 Tasker 的主菜单，长按顶部的 Tasks 标签，直到你看到一个对话框弹出。按 Import，查找您之前保存的 XML 文件，并选择它进行导入。

[**下载查找 Betas 版任务脚本**](https://www.androidfilehost.com/?fid=817550096634757094)

我被告知您将需要根据您的地区在步骤#5 中修改匹配文本。例如，英语(加拿大/英国)需要将“program”改为“program”。其他语言同样需要打开一个示例 beta 测试页面，并复制您的语言中显示的文本作为匹配文本。

当你导入这个的时候，注意顶部巨大的免责声明。您必须使用您的 Google 帐户验证 AutoTools，然后才能执行此任务。只需打开动作#1(它被禁用，所以它不会自己运行)点击它，并按下铅笔图标打开自动工具配置。滚动到底部并点击认证。您应该会看到登录您的 Google 帐户的提示。这样做，一旦你到达 Play Store 登录页面，点击后退按钮。现在，点击左下角的“播放”图标，返回并运行任务。

我希望这个任务对你有用。我发现了很多我有资格使用的测试频道，很多是我从未想过会有测试频道的应用。这个脚本在为你安装的应用程序寻找测试版更新时确实节省了很多时间，尽管对我个人来说，这个时间被完成这个任务所花费的时间所抵消了！

如果您觉得这个脚本有用，或者您对未来的教程有任何建议，请告诉我们。