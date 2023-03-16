# 微软翻译器增加人工智能支持的离线语言包

> 原文：<https://www.xda-developers.com/microsoft-translator-ai-powered-offline-language-packs/>

微软翻译是微软对谷歌翻译的竞争对手。该应用程序具有广泛的功能集，并具有多种语言的翻译功能。用户可以使用它进行多种语言的文本到语音翻译。

现在，微软宣布 Translator 增加了新的功能，允许用户和开发者无论是否连接到互联网，都可以获得人工智能支持的翻译。新功能允许用户和第三方应用程序开发人员从神经翻译技术中受益，无论他们的设备是连接到云还是离线。

最终用户现在可以在微软翻译器中下载免费的人工智能离线包。微软表示，这项开发经过了两年的工作，据说是为了补充其努力，以确保开发人员和用户可以访问人工智能工具来获取数据，无论是在云中还是在设备中。这种能力被专家称为边缘计算。

该公司指出，微软翻译机在 2016 年发布了人工智能在线神经机器翻译(NMT)。由于“运行这些高质量翻译模型所需的计算能力”,这种功能只能在网上使用。2017 年底，该功能针对特定的 Android 手机推出，这些手机都有专用的人工智能芯片-即华为 Mate 10 系列和 Honor View 10，[，因为它们有定制版的 Translator](https://www.xda-developers.com/microsoft-linkedin-huawei-mate-10/) 。这是因为麒麟 970 SoC 有一个专用的神经处理单元(NPU)。据微软称，它允许这些设备的用户获得与在线神经翻译质量相当的离线翻译质量。

微软翻译团队随后能够进一步优化算法，这使得它们可以直接在任何现代设备的 CPU 上运行，而不需要专用的人工智能芯片。因此，新的翻译应用程序现在将所有 Android、iOS 和 Amazon Fire 设备的神经机器翻译“带到了云的边缘”，并很快支持 Windows 设备。

根据微软的说法，新的 NMT 包产生了更高质量的翻译，比以前的非神经离线语言包好 23%，小约 50%。NMT 包以 Translator 最流行的语言提供，该公司表示将定期添加新的 NMT 语言。用户可以在此查看完整的最新列表[。](https://translator.microsoft.com/help/articles/languages)

微软今天宣布的第二个功能是 Translator Android 应用程序中新的本地功能的预览，该功能使 Android 开发者能够“快速而轻松地”将文本翻译添加到任何受益于翻译功能的 Android 应用程序中。此外，由于新的 NMT 离线包，Android 开发者可以首次将离线 NMT 添加到他们的应用程序中，这允许他们的用户在没有互联网连接的情况下访问 NMT 翻译的内容。

为了将翻译集成到他们的应用程序中，开发人员需要添加“一些简单的代码”，这些代码将使用 Android 的绑定服务技术和 AIDL 接口来静默调用 Translator 应用程序，Translator 应用程序将完成剩余的工作。如果用户的设备在线，翻译应用程序将从 Azure 上的微软翻译服务中检索信息。如果没有互联网连接，该应用程序将使用当地的 NMT 离线语言包将翻译发送回开发人员的应用程序。

微软表示，该功能预计将在预览版发布后的 90 天内正式推出。该公司还指出，当用户的设备在线时，翻译也可以利用定制的翻译模型，这些模型与应用程序和公司的独特术语相匹配。

开发人员可以在该公司的 [GitHub 文档和示例应用](https://aka.ms/translatorlocaldocs)中了解更多关于本地功能预览如何工作的信息。

* * *

[**来源:微软**](https://blogs.msdn.microsoft.com/translation/2018/04/18/microsoft-brings-ai-powered-translation-to-end-users-and-developers-whether-youre-online-or-offline/)