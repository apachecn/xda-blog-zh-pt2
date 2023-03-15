# 在 Tasker 中创建一个上下文感知指纹读取器

> 原文：<https://www.xda-developers.com/create-a-context-aware-fingerprint-reader-in-tasker/>

指纹读取器在默认状态下相当有限。除了解锁手机或授权一些支付的明显功能外，大多数 Android 手机上的指纹识别器没有太多其他功能。直到现在，这个特性总是让人觉得错过了一个机会！

* * *

## 基于 Tasker 的上下文感知指纹识别器

在 Tasker 中创建一个定制的指纹读取器是一个相当简单的项目。Tasker 将根据您正在做的事情或您所在的位置，为指纹识别器分配多种功能。在本例中，我将向您展示如何将当前网站即时投射到大屏幕上(在本例中，是我的 PC)。通过这种方式，您可以根据打开的窗口或您的位置为阅读器添加额外的功能。你的想象力是你唯一的极限。

### *工作原理*

请记住，[指纹扫描仪工具应用程序](https://play.google.com/store/apps/details?id=com.flextrick.fringerprintscannertools)是新的，正在积极开发中。Tasker 支持目前仅限于执行任务，但是，这是我们需要的。我们将使用 Tasker 中的变量为指纹扫描仪分配**多个配置文件**。当指纹被激活，Tasker 将检查你还做了什么(或你在哪里)，并相应地执行正确的配置文件。

### *指纹扫描*

我们需要让读者成为我们条件的通用触发器。我们将需要创建一个任务，**扫描手指**，这将为我们触发其他配置文件。我们可以将此与变量**% fingerscaned**联系起来。当指纹扫描仪工具应用程序识别到指纹时，它将启动我们的扫描手指任务，临时设置从 **0** 到 **1** 的%FingerScanned 值，持续 2 秒钟。2 秒钟的时间应该足够让我们的其他 Tasker 配置文件对变量变化做出反应。如果 Tasker 对变量更改的响应有任何问题，请尝试将等待时间增加到 3 秒或更长。打开指纹扫描仪工具并分配此任务。接下来，我们将创建不同的配置文件，这些文件将根据当前的环境启动——某个应用程序是否打开，您的当前位置等。

### *投射当前的 Chrome 窗口*

在这个例子中，我们将演示如何在 Chrome 中**转换当前打开的标签页。当值%FingerScanned 设置为 1(根据之前创建的任务)**并且** Tasker 检测到当前打开的应用程序是 Chrome 浏览器时，将触发此配置文件。这需要你为 Tasker 启用辅助功能服务，否则 Tasker 将无法检测到 Chrome 何时打开。此外，由于与 Tasker 的广泛集成，我们将使用 XDA 初级成员 [joaomgcd](http://forum.xda-developers.com/member.php?u=4805489) 的 **[自动输入](https://play.google.com/store/apps/details?id=com.joaomgcd.autoinput)** 以及 **[加入](https://play.google.com/store/apps/details?id=com.joaomgcd.join)** 。**

首先，您需要创建一个带有两个上下文的概要文件:第一，当%FingerScanned = 1 时激活的状态上下文；二是 Chrome 打开时激活的一个 App 上下文。接下来，您需要复制上面截图中显示的任务，或者复制如下。一旦你完成了，这个任务将会查询 Chrome 中当前打开的 URL，并使用 Join 将它推送到你的 PC 上。如果你愿意，你可以提示选择一个设备，但是对于超快速共享，我指定了一个设备来完成。

我使用 AutoInput UI 查询来获取浏览器中 URL 的值。在大多数情况下，网址将以 www/http(s)或其组合开头。要获取 URL，我们需要以下正则表达式:

```
 ((?<=http:\/\/|https:\/\/|https:\/\/www.|http:\/\/www.|www.))?.* 
```

如果您在配置查询时有任何问题，请使用变量 Setup 返回 Chrome 并选择地址栏。AutoInput 将帮助自动设置 URL 捕获。我已经设置了一个自定义变量 **%address** ，它将包含当前打开的 Chrome 标签中的 URL 地址。

最近对 Join app 的更新已经修复了该问题，不再需要 A2-A4 操作。您可以正确推送与前缀无关的 URL。

在将页面推送到计算机之前，我们需要检查 URL 的格式是否正确。推送以 www 开头的 URL 不会在您的桌面浏览器中自动打开该网站。确保我们发送格式正确的 URL 的最简单方法是运行**搜索/替换**操作。**%前缀**变量的默认值将是“ **http://”。如果一个网站不支持 https 协议，我们需要这个。我们将在 URL 中查找 http 或 https，如果找到了**%前缀**，它将在加入 URL 推送中设置。查找 **https://** 并选择替换。不要在**替换为**字段中输入任何内容，因为我们只是希望将其从我们的地址中删除。对 **http://** 执行同样的操作。**

最后一个动作是加入推送。转到网址，输入**%地址**。这样，URL 将被正确地推送到 PC，并自动打开网站。

如果你担心安全性，许多网站会自动将你重定向到它们的安全版本，如果存在的话，但如果没有，你可以使用 [HTTPS Everywhere](https://chrome.google.com/webstore/detail/https-everywhere/gcbommkclmclpchllfjekcdonpmejbdp?hl=en) 扩展来为你处理。

* * *

## 结论

如您所见，通过将指纹扫描仪工具的 Tasker 操作分配给变化的变量，我们可以分配多个操作，尽管单个 Tasker 任务存在局限性。我联系了指纹扫描工具的开发者 Daniel Huber，他说未来会有更多的 Tasker 功能。现在，您已经知道如何使用指纹识别器，而不必将其绑定到单个任务，您可以自定义在识别指纹时应该启动的上下文和操作。

也许你只需轻轻一点就可以播放 YouTube 视频(不需要 Chromecast)。我可能会在下一个教程中展示这一点？如果你想看这个和其他任务脚本，请在下面告诉我们你的想法！

* * *

## **下载/导入**

一如既往，我们将提供下载或手动导入我们在这些 Tasker 教程中展示的作品的方法。您将有两个选项将这些脚本添加到 Tasker 设置中。

首先，您可以通过下面的下载链接下载整个项目。下载完项目 XML 文件后，您可以打开 Tasker，然后长按左下角的 Home 图标来导入它。这将打开 Tasker 项目菜单，允许您导入位于内部存储器上的项目。

[**下载上下文感知指纹识别器项目**](https://www.androidfilehost.com/?fid=385035244224400253)

或者，您可以使用下面两个选项卡中包含的概要文件/任务的描述来指导您自己重新创建该脚本。如果您想学习如何在 Tasker 上做得更好，我们推荐这条路线，这样您就可以自己对脚本进行定制或改进。

[选项卡][选项卡 title ="Cast Chrome"]

```
Profile: Cast Chrome

应用:铬合金

状态:变量值[ %FingerScanned eq 1 ]

回车:Chrome

A1:自动输入 UI 查询[配置:仅可见:真

仅可点击:假

App 包:com.android.chrome

检查屏幕状态:假

正文:((？< = http:\/\/| https:\/\/| https:\/\/www。|http:\/\/www。|www。))?。*

对

变量:地址超时(秒):20 ]

 ~~A2:变量集【名称:% prefix To:http://Do Maths:Off Append:Off】~~

 ~~A3:变量搜索替换[变量:%地址搜索:https://忽略大小写:在多行上:仅提供一个匹配:在存储中匹配:%前缀替换匹配:在替换为:]~~ 

 ~~A4:变量搜索替换[变量:%地址搜索:http://忽略大小写:在多行上:仅提供一个匹配:在存储中匹配:%前缀替换匹配:在替换为:]~~ 

A5:加入发送推送[配置:设备:Chrome@Home

URL:%前缀%地址超时(秒):60 ]
```

[/tab][tab title = "阅读手指"]

```
Scanned Finger 

A1:变量集[名称:% finger scanned To:1 Do Maths:Off Append:Off]

A2:等待[毫秒:0 秒:2 分钟:0 小时:0 天:0 ]

A3:变量集[名称:% finger scanned To:0 Do Maths:Off Append:Off][/tab]
```

[/tabs]