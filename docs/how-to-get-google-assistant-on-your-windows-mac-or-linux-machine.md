# 如何在你的 Windows、Mac 或 Linux 机器上安装谷歌助手

> 原文：<https://www.xda-developers.com/how-to-get-google-assistant-on-your-windows-mac-or-linux-machine/>

谷歌助手是谷歌对亚马逊的 Alexa 智能家居助手的回答。最初，谷歌助手仅在谷歌 Allo 应用程序中提供有限的功能，后来随着谷歌 Home 和 Pixel 智能手机的推出，为消费者带来了谷歌助手的全部功能。

经过几个月的等待，[运行 Android 6.0+](https://www.xda-developers.com/google-assistant-now-available-for-all-android-6-0-devices/) 的智能手机也获得了谷歌助手，就在几天前谷歌推出了[谷歌助手 SDK](https://www.xda-developers.com/google-launches-the-google-assistant-sdk-for-3rd-party-companies/) ，它允许助手基本上在任何平台上运行。今天，我们将向你展示如何使用 Python 在你的 Windows、Mac 或 Linux 机器[上安装谷歌助手。](https://github.com/googlesamples/assistant-sdk-python)

**注意:此时此刻，这纯粹是出于教育目的。没有花哨的 GUI 供您使用，安装 Assistant 需要您使用命令行。**

* * *

## 在 Windows/Mac/Linux 机器上获取谷歌助手

无论您使用的是 Windows、macOS 还是 GNU/Linux 发行版，您都需要安装 Python。安装相当简单，并且已经由 Python wiki 很好地记录了[，所以我们不会详细讨论如何在您的机器上安装和运行 Python。](https://wiki.python.org/moin/BeginnersGuide/Download)

一旦让 Python 在您的机器上运行(您可以通过打开终端/命令提示符，然后简单地键入`python`来确认它正在运行。)如果您看到终端/命令提示符返回您计算机上的当前 Python 版本，那么您就成功了。

接下来，在我们可以安装必要的文件来让谷歌助手工作之前，我们需要在谷歌云平台控制台中启用对谷歌助手 API 的访问。

* * *

### 配置谷歌助手 API

接下来是一步一步的指导，带你完成在云平台控制台中启用谷歌助手 API 的过程，这样你就可以通过 Python 程序访问谷歌助手了。所有这些步骤都是独立于平台的，这意味着这些步骤对于 Windows、macOS 和 GNU/Linux 用户来说是相同的。

1.  进入谷歌云平台控制台的[项目页面](https://console.cloud.google.com/project)。
2.  点击顶部的**创建项目**。
3.  将项目命名为“我的谷歌助手”，然后点击“创建”
4.  等待几秒钟，让控制台创建您的新项目。您应该会在右上角看到一个旋转的进度图标。创建完项目后，您将进入项目的配置页面。
5.  **[点击此链接](https://console.developers.google.com/apis/api/embeddedassistant.googleapis.com/overview)** 直接进入谷歌助手 API 页面。在顶部，点击“启用”
6.  Google 会警告你需要创建凭证来使用这个 API。点击右上角的**创建凭证**。这将把你带到一个设置向导页面，在这里 Google 会帮助你确定使用这个 API 需要什么样的凭证。
7.  在“您将从哪里调用 API”下，选择“**其他用户界面(如 Windows、CLI 工具)**”。对于“您将访问哪些数据”，请选择“**用户数据**”圆圈。现在点击“我需要什么凭证？”
8.  Google 应该推荐你创建一个 **OAuth 2.0 客户端 ID** 。将客户端 ID 命名为您想要的任何名称，例如，您的姓名+桌面。选择好名称后，点击“创建客户 ID”
9.  在“向用户显示的产品名称”下，输入“我的谷歌助手”单击继续。
10.  点击“完成”没有必要点击这里的下载，因为我们只需要客户端密码，我们将下载下一步。
11.  现在，在 OAuth 2.0 客户端 ID 列表下，您应该可以看到刚刚创建的客户端 ID。一路向右，点击下载图标，下载 **client_secret_XXX.json** 文件，其中‘XXX’是你的客户端 ID。把这个文件保存在你电脑上的任何地方，最好保存在一个名为“googleassistant”的新文件夹中
12.  转到您的 Google 帐户的[活动控制页面](https://myaccount.google.com/activitycontrols)，确保“Web &应用活动”、“位置历史记录”、“设备信息”和“语音&音频活动”已启用。这是为了让 Google Assistant 实际上可以为你读取个性化信息。

我们现在已经为一个客户端创建了一个机制，在这个例子中是我们的 Windows/Mac/Linux 机器，它在我们的 Google 帐户下访问 Google Assistant API。接下来，我们需要设置将访问 Google Assistant API 的客户端。

### 安装 Google Assistant 示例 Python 项目

**尽管谷歌建议您设置 [Python 虚拟环境](https://docs.python.org/3/library/venv.html)来将谷歌助手 SDK 及其依赖项与其他 Python 系统包隔离，但我们将跳过这一步，因为您不太可能花几分钟时间来玩这个。如果你担心其他程序访问你的谷歌账户的可能性，你可以很容易地回到云平台控制台并禁用 API。**

打开终端/命令提示符窗口，并执行以下步骤。首先，输入以下命令:

```
 py -m pip install google-assistant-sdk[samples] 
```

当您输入这个命令时，应该会看到下载并安装了一大堆依赖项。这些是示例 Python 项目运行所必需的。等待它结束。

完成后，接下来输入以下命令(确保调整路径):

```
 py -m googlesamples.assistant.auth_helpers --client-secrets path\to\your\client_secret_XXX.apps.googleusercontent.com.json 
```

在命令提示符下，您会看到一个响应，告诉您访问一个 URL 以便对应用程序进行授权。

将此 URL 复制并粘贴到浏览器中。选择您用来配置 Google Assistant API 的同一个 Google 帐户。在下一页上，您将看到一个包含客户端访问令牌的文本框。

复制该访问令牌并将其粘贴到命令提示符中，在命令提示符处，它会要求您输入授权码。如果操作正确，您将看到一个响应，提示您的凭据已保存。

* * *

### 测试谷歌助手

你要测试的第一件事是谷歌助手是否能够从你的麦克风录音。在命令提示符下输入以下命令，它将录制 5 秒钟的音频并向您播放:

```
 python -m googlesamples.assistant.audio_helpers 
```

如果您听到向您播放的音频，请输入以下命令开始与 Google Assistant 对话:

```
 python -m googlesamples.assistant 
```

等待命令提示符说“按 Enter 发送新请求”，然后按 Enter 开始与 Google Assistant 对话。在您说完之后，命令提示符将显示您刚才所说内容的文字记录，然后回放响应。如果之后看到警告，就忽略它。

在您的 Windows、macOS 或 GNU/Linux 机器上玩 Google Assistant 玩得开心！我只玩了几分钟就厌倦了。它在这种格式下并不特别有用，但它非常快速地展示了新的 Google Assistant SDK 所代表的可能性。或许在不久的将来，我们会看到桌面应用程序或浏览器扩展利用这一功能。