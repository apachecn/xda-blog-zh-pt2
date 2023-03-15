# 如何将你的桌面 Chrome 书签与 Android 上的第三方 Chrome 浏览器同步

> 原文：<https://www.xda-developers.com/how-to-sync-your-desktop-chrome-bookmarks-with-third-party-chrome-browsers-on-android/>

过去一年，基于谷歌 Chrome 的第三方浏览器大受欢迎。这一趋势始于 Code Aurora Forum (CAF)于 2015 年 10 月开始发布针对骁龙设备优化的 [Chromium 版本。对制作终极、功能丰富的浏览器感兴趣的开发人员开始分叉该项目，并通过 Chrome Sync API 在支持 Chrome 书签的基础上添加了一些功能，如夜间模式、内容拦截器、省电模式、手势支持等。](https://www.xda-developers.com/chromium-optimized-for-snapdragon-devices/)

用户蜂拥至我们论坛上流行的 TugaBrowser 等项目，因为这些浏览器在谷歌现有 Chrome sync 功能的基础上提供了许多非 Chrome 浏览器所没有的增强功能。不幸的是，谷歌[在一月份关闭了第三方对 Chrome Sync API](https://bugs.chromium.org/p/chromium/issues/detail?id=677887) 的访问，称是出于安全考虑。谷歌表示，此举并非有意阻碍第三方 Chrome 浏览器，甚至连[开源 Chrome](https://www.xda-developers.com/xda-spotlight-living-on-the-bleeding-edge-with-chromium-auto-updater/)也被归为第三方 Chrome 浏览器，但这个安全补丁无意中终结了第三方 Chrome 浏览器的书签同步。

此时，TugaBrowser 等浏览器仍然没有办法将书签更改与 Chrome Sync 同步。但是有一种方法可以让你的桌面书签与第三方 Chrome 浏览器同步，前提是你有 root 权限。我们在之前已经在[上发布过的方法，基本上可以总结为以下几个步骤:](https://www.xda-developers.com/xda-external-link/how-to-copy-desktop-chrome-bookmarks-to-caf-based-chromium-browsers/)

1.  打开第三方 Chrome 浏览器的书签文件，复制校验和值
2.  将书签文件从 Chrome 的目录下推到你的第三方 Chrome 浏览器的目录下，覆盖它。
3.  打开新的书签文件，用第一次复制的值覆盖校验和值
4.  强制关闭/终止第三方 Chrome 浏览器，这样它就会重新加载书签

这种编辑书签的方法已经存在很多年了，作为一种在桌面上恢复书签的方法，以防出现问题，但是使用这些步骤在 TugaBrowser 等浏览器上获取书签是这种老技巧的巧妙应用。虽然这种方法确实允许你在你最喜欢的第三方 Chrome 浏览器上获得你的 Chrome 书签，但它要求你每次在 Chrome 中添加新书签时都要做这些步骤。这当然一点也不方便，这就是为什么我试图**自动化这个过程。**

在上面的视频中，请注意当我打开 TugaBrowser 展示我的书签时，显示了 3 个书签。当我离开并重新打开 TugaBrowser 时，会显示一个 [snackbar](https://material.io/guidelines/components/snackbars-toasts.html) 告诉我已经检测到一个新的书签，还有一个重启 TugaBrowser 的按钮。当我按下按钮重新启动浏览器时，我打开了书签页面，现在看到添加了一个新的第四个书签。本质上，我已经自动完成了上述 4 个步骤，在后台安静地工作，我在这里发布了一个教程，告诉你如何做到这一点！

在我开始本教程之前，我需要提到几件事:

*   这个方法**需要 root 访问权限**。这个要求绝对没有办法，抱歉！我们正在处理/data/data 中的文件，没有 root 用户就无法访问这些文件。
*   这个方法是**单向同步**，意味着你添加到第三方 Chrome 浏览器的任何书签都不会被保存(实际上是被覆盖)。你必须在启用了 Chrome Sync 的 Chrome 浏览器中添加新的书签。我已经研究了强制 Chrome Sync 接受我的书签更改的方法，但不幸的是，我认为这是不可能的，因为谷歌服务器上存储的书签版本似乎总是会覆盖你手动做出的任何更改。
*   这个方法**安全**。你的书签不会被删除，因为我们不会(也不可能)篡改谷歌储存在服务器上的书签副本。

如果你正在你的第三方 Chrome 浏览器上寻找一种双向同步方法，那么对不起，**你永远也得不到这样的方法**。这要怪谷歌。*如果你在问自己“这有什么意义”，那么这个教程不适合你*。如果你想在某种程度上减轻谷歌移除 Chrome Sync 的痛苦，那么希望这篇教程对你有用。

* * *

## 第三方 Chrome 浏览器的单向 Chrome 书签同步

虽然我说 Tasker 是必需的，但你也许可以在 Play Store 上使用其他自动化应用。如果你选择这样做，你只能靠自己，因为我没有使用它们的经验，所以你必须自己改编我的剧本。Synker 是必要的，因为我们用它来强制手动刷新你的书签。snackbar Tasker 插件在技术上是不必要的，但它提供了整洁的 snackbar，让我知道有新的书签和重新启动应用程序的按钮。最后，你必须在你的设备上安装(而不是禁用)谷歌浏览器(任何频道都可以)，因为它将为我们提供我们要复制的书签文件。

还有一点要提的是:虽然我的教程是基于 TugaBrowser 的，但你可以通过修改一些步骤，很容易地让它与任何其他基于 Chrome 的浏览器一起工作，我将在下面的结尾概述这一点。

### 辅导的

我使用的脚本相当复杂，总共有 29 个动作，所以我不会过多地讨论每个步骤是如何工作的，只需知道这个脚本基本上自动完成了本文开头概述的 4 个手动步骤。

这是对那些已经是 Tasker 专家并想自己复制它的人的简介描述。

### CAF 书签同步

```
 Profile: CAF Bookmark Sync (28)应用:TugaBrowser回车:检查 Chrome 书签(27)A1: Synker - Force sync [配置:Force sync 2 提供程序超时(秒):0 ]A2:等待[毫秒:0 秒:5 分钟:0 小时:0 天:0 ]A3:运行 Shell[Command:CP/data/data/com . Android . chrome/app _ chrome/Default/Bookmarks/SD card/Tasker/Bookmarks 超时(秒):0 Use Root:On Store Output In:Store Errors In:Store Result In:]A4:读取文件[File:/SD card/Tasker/Bookmarks To Var:% JSON]A5:变量 Split[Name:% JSON Splitter:" checksum ":Delete Base:Off]A6:变量搜索替换[变量:%json2 搜索:(？<=")[^"]+(?= ")忽略大小写:关闭多行:仅关闭一个匹配项:存储中的匹配项:%校验和替换匹配项:关闭替换为:]A7:如果[ %ChromeChecksum！设置]A8:变量集[名称:%ChromeChecksum To:%checksum(1)递归变量:Off Do Maths:Off Append:Off ]A9:其他A10:如果[ %ChromeChecksum！~ %校验和(1) ]A11:变量集[名称:%ChromeChecksum To:%checksum(1)递归变量:Off 做数学:Off 追加:Off ]A12:运行 Shell [命令:CP/data/data/tuga power . code aurora . browser/app _ chrome/Default/Bookmarks/SD card/Tasker/TugaBookmarks 超时(秒):0 使用 Root:在存储输出中:存储错误中:存储结果中:]A13:读取文件[File:/SD card/Tasker/TugaBookmarks To Var:% tugajson]A14:变量 Split[Name:% tugajson Splitter:" checksum ":Delete Base:Off]A15:变量搜索替换[变量:%tugajson2 搜索:(？<=")[^"]+(?= ")忽略大小写:关闭多行:仅关闭一个匹配项:存储中的匹配项:%校验和替换匹配项:关闭替换为:]A16:变量搜索替换[变量:%json2 搜索:(？<=")[^"]+(?= ")忽略大小写:关闭多行:仅关闭一个匹配项:存储匹配项:替换匹配项:替换为:%checksum(1) ]A17:写入文件[File:/SD card/Tasker/Bookmarks Text:% JSON 1 " checksum ":% JSON 2 Append:Off Add Newline:Off]a18:Run Shell[Command:CP/SD card/Tasker/Bookmarks/data/data/tuga power . code aurora . browser/app _ chrome/Default/Bookmarks time out(Seconds):0 Use Root:On Store Output In:Store Errors In:Store Result In:]A19: Snackbar [配置:消息:检测到新书签。按钮:重新启动命令:超时(秒):15 ]A20:如果[ %sb_button ~ Button 按下]A21:回家[ Page:0 ]A22:等待[毫秒:0 秒:2 分钟:0 小时:0 天:0 ]A23: Kill App [ App:TugaBrowser 使用 Root:Off ]A24:等待[毫秒:0 秒:2 分钟:0 小时:0 天:0 ]A25:启动应用程序[应用程序:TugaBrowser 数据:从最近的应用程序中排除:关闭总是启动新副本:关闭]A26:结束 IfA27:删除文件[File:/SD card/Tasker/TugaBookmarks 粉碎级别:0 使用 Root:Off ]A28:结束 IfA29:结束 IfA30:删除文件[文件:/SD card/Tasker/书签粉碎级别:0 使用 Root:Off ]
```

每当 Tasker 检测到你进入了你选择的第三方 Chrome 浏览器，这个脚本就会被激活。您将需要启用 Tasker 的辅助功能服务，以便 Tasker 可以检测到您何时进入您选择的浏览器。这一部分可以很容易地修改，以与其他基于 Chrome 的浏览器一起工作，你需要做的就是在 Tasker 的应用程序上下文中选择你希望这个脚本运行的浏览器。

现在，这里简要描述一下该任务中的每组操作要完成的内容。

*   **A1-A2** :从谷歌的服务器手动同步 Chrome 书签，以便安装的 Chrome 应用程序的书签文件得到更新。等待 5 秒钟，以确保有足够的时间来完成同步
*   **A3-A6** :将 Chrome 的书签文件复制到一个临时位置，将文件中的 JSON 提取到一个变量中，然后使用 regex 过滤器将校验和值提取到另一个变量中
*   **A7-A10** :如果 Tasker 没有设置全局变量%ChromeChecksum(即。第一次运行脚本)，将其设置为当前值。如果它有一个值集，接下来检查存储在 Tasker 变量中的值是否与书签文件中的当前校验和相匹配。如果是这样，继续走 A11-A26 公路
*   **A11** :将保存 Chrome 校验和的 Tasker 变量设置为从书签文件中提取的当前校验和
*   **A12-A15:** 将 TugaBrowser 的书签文件复制到一个临时位置，从文件中提取 JSON，然后使用 regex 过滤器提取校验和值
*   **A16:** 使用从 TugaBrowser 获取的校验和值，并用它替换来自 Chrome 书签文件的校验和值
*   **A17** - **A18:** 将从 Chrome 获取的带有 TugaBrowser 校验和值的更新书签文件推送到 TugaBrowser 的数据目录中
*   A19-A26: 显示一个 snackbar，告诉我们已经添加了新的书签。如果按下 snackbar 上的按钮，重启 TugaBrowser，否则继续。
*   A27-A30 :删除我们正在处理的临时书签文件，并结束任务

为什么这涉及这么多步骤？不幸的是，这是因为我们没有一种简单的方法可以通过 Tasker 或它的一个插件(比如 AutoTools)直接访问书签文件中的(可能很大的)JSON 数据结构，而不需要复制文件并将其内容提取到一个变量中。如果我们可以的话，这项工作将会更加简洁，但现在这是我想出来的。我和 AutoTools 的开发人员讨论过这个问题，虽然他能够更新 AutoTools，使之能够从文件中读取 JSON 数据，但是不能通过 Tasker 插件将 JSON 直接写入文件。

在任何情况下，这个脚本本身运行非常快，尽管有些步骤似乎是不必要的，因为我想得到它，而不需要你在 Tasker 上安装任何不必要的附加插件。唯一让这个脚本变慢的，也是你为什么会在视频中看到一些延迟的原因，是 Tasker 需要等待一段时间，以确保你的 Chrome 书签已经从谷歌的服务器上同步，然后再继续脚本的其余部分。如果你愿意，你当然可以在 Tasker 任务中使用“等待”命令来降低延迟，但这最终取决于你自己。

* * *

## 下载、导入和设置

和往常一样，我们将提供 Tasker Profile XML 文件，您可以快速地为自己设置。从 AndroidFileHost 下载下面的. prf.xml 文件，并将其保存到您的内部存储。打开 Tasker，在首选项中禁用初学者模式。回到 Tasker 的主屏幕，长按顶部操作栏中的“个人资料”选项卡，直到你看到一个“导入”选项弹出。按下该按钮，然后导航到您保存 XML 文件的位置，选择它以导入它。

[**从 AndroidFileHost** 下载“Chrome 书签同步”配置文件](https://www.androidfilehost.com/?fid=529152257862717245)

在这个概要文件为您工作之前，有 3 个非常非常重要的步骤(如果您没有运行 TugaBrowser，还有 1 个可选但必要的步骤)需要您执行。

1.  启用**任务者的** **无障碍服务**。您可以通过打开“设置”并搜索“辅助功能”来完成此操作点击 Tasker，然后启用其辅助功能服务。这是必要的，因为否则 Tasker 无法检测您何时使用 TugaBrowser(或任何其他浏览器)。
2.  在 Synker 中选择您的 **Chrome 同步提供商。你可以打开“检查 Chrome 书签”任务，然后点击标有“Synker - Force sync”的动作#1 按铅笔图标调出 Synker 的配置屏幕。向下滚动，为你的谷歌账户选择“Chrome Sync”。**
3.  **授予 Tasker 超级用户权限**。最快的方法是让任务者尝试执行一个需要*苏*的动作。再次进入“检查 Chrome 书签”任务配置屏幕，这次长按标有“运行 Shell”的动作#3 按下左下角弹出的“播放”图标，让 Tasker 运行这个动作，而且只运行这一个。Tasker 会要求你授予它超级用户权限。*使用 MagiskSU 的用户请注意:Tasker 目前并不自己检测 MagiskSU，因此它可能会抛出一个错误，说明您的设备不是根设备。这将在下一次 Tasker 更新中被修复，但是如果你正在寻找一个临时的解决方法，XDA 资深成员 [RandomPooka](https://forum.xda-developers.com/member.php?u=3053466) 有一个针对那个的[简短指南。](https://forum.xda-developers.com/apps/magisk/mod-magisk-v1-universal-systemless-t3432382/post70912646#post70912646)*

在你做了这三件事之后，这个档案应该开始工作了。在你第一次启动 TugaBrowser/你选择的浏览器时，Tasker 会保存 Chrome 书签文件的校验和值。当校验和值在 TugaBrowser/您选择的浏览器的后续启动中发生变化时，Tasker 会用 Chrome 的书签文件替换您浏览器的书签文件。

**注意，第一次启动你的浏览器**时，我故意没有设置它，所以 Tasker 会复制 Chrome 的书签值，直到它检测到变化。这意味着你选择的 TugaBrowser/browser 的书签不会改变，除非你对 Chrome 的书签进行了更改。我这样做是为了让你能够访问 TugaBrowser/你选择的浏览器来保存你没有存储在谷歌服务器上的未同步/离线书签，这样我的 Tasker 个人资料就不会在你没有机会保存它们的情况下将它们清除掉。

* * *

### 如何在 TugaBrowser 以外的浏览器上同步书签

如果你没有使用 TugaBrowser，你需要修改一些步骤，以便在你选择的基于 Chrome 的浏览器上运行。幸运的是，这非常非常容易做到。我将以开源的 Chromium 为例向您展示如何做到这一点。以下是你需要改变的事情:

1.  **改变应用上下文**。不要将“TugaBrowser”设置为应用程序上下文，而是将应用程序上下文更改为在使用选择的浏览器时触发。只需点击上下文，在列表中查找您的应用程序。
2.  修改**动作#12** (运行 Shell 命令)指向你特定浏览器的书签文件。该目录应该类似于/data/data/PACKAGE。名称/app _ chrome/Default/书签。(注意:保存它/将其称为“TugaBookmarks”的变量和文件名可以安全地忽略，您只需要更改 Tasker 从何处提取书签文件)之前:

    ```
     cp /data/data/tugapower.codeaurora.browser/app_chrome/Default/Bookmarks /sdcard/Tasker/TugaBookmarks 
    ```

    之后:

    ```
     cp /data/data/org.chromium.chrome/app_chrome/Default/Bookmarks /sdcard/Tasker/TugaBookmarks 
    ```

3.  修改**动作#18** (另一个运行 Shell 命令)将更新的书签文件保存在您特定浏览器的数据目录中。同样，目录看起来应该和上面一样。之前:

    ```
     cp /sdcard/Tasker/Bookmarks /data/data/tugapower.codeaurora.browser/app_chrome/Default/Bookmarks 
    ```

    之后:

    ```
     cp /sdcard/Tasker/Bookmarks /data/data/org.chromium.chrome/app_chrome/Default/Bookmarks  
    ```

4.  修改**动作#23** 关闭你选择的浏览器。这就是为什么当你按下 snackbar 中的重启按钮时，Tasker 会终止正确的应用程序。
5.  修改**动作#25** 重新启动你选择的同一个浏览器。这将在用户关闭浏览器后重新启动浏览器，以便它可以加载新的书签。

其他一切都可以安全地保持原样，即使创建的变量/文件名对您的特定浏览器没有意义。如果它们打扰了你，你可以选择改变它们，但是在尝试这样做之前，确保你知道你在做什么。熟悉一些 Tasker 肯定会有所帮助。

* * *

## 结论

我希望你觉得这个简介有用。我知道这里有很多东西需要理解，但仔细阅读这篇文章对你来说真的很重要，这样你就能理解它的作用、工作原理以及何时工作。这花费了我很多的尝试和错误，但是我对结果很满意，即使它最终看起来过于复杂。

自动化这一过程有助于减轻一些用 Chrome Sync 同步书签的负担，尽管不幸的是，这将永远只是单向同步，并将始终需要 root 访问权限，直到谷歌放松对第三方 Chrome 浏览器访问 Chrome Sync 的限制。

***如果您有任何问题、意见或担忧，请在下面的评论中告诉我们！***