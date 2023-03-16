# 【更新:未泄露】商业反盗版软件 DexGuard 的源代码在网上泄露

> 原文：<https://www.xda-developers.com/source-code-dexguard-anti-piracy-software-leaks/>

# 【更新:未泄露】商业反盗版软件 DexGuard 的源代码在网上泄露

Android 应用程序混淆器 DexGuard 的源代码在 GitHub 上被泄露。那到底是什么意思？

DexGuard 是一个由 Guardsquare 编写的流行的商业反盗版软件，它可以帮助混淆 APK 文件。反编译 Android 应用程序并查看其内部工作方式非常容易，但 DexGuard 等混淆程序使这变得非常困难。该软件还保护应用程序免受逆向工程攻击，以防止用户弄清楚应用程序到底是如何做的。这反过来防止了盗版，因为它使攻击者更难找到绕过反盗版检查的方法。然而，DexGuard 的一个旧版本在 GitHub 上泄露了源代码。

该代码已被证实是真实的，这在很大程度上要归功于 Guardsquare 自己在最初的 GitHub 知识库上提交了一份 DMCA 撤销请求，理由是侵犯了版权。

> #### “列出的文件夹(见下文)包含我们用于 Android 应用程序的商业混淆软件(DexGuard)的旧版本。该文件夹是一个更大的代码库的一部分，是从我们以前的一个客户那里偷来的。”

如果你从未听说过 DexGuard，你可能听说过 ProGuard。ProGuard 是一个通用的 Java 混淆器，而 DexGuard 专门适用于 Android 应用程序。ProGuard 也是完全免费和开源的。两者都能在 Android 应用上完美运行。

该公司的源代码被盗的后果目前还不清楚。源代码已经出现在互联网上的许多不同地方，所以它似乎不会很快消失。Guardsquare 发现了超过 200 个包含侵权代码的分叉库，当时 DMCA 已经删除了原始版本。它可能会让那些试图反编译和修改受该软件保护的 Android 应用程序的人了解其模糊方法的内部工作原理，尽管还不知道源代码可能会带来多大的优势。对于依赖 DexGuard 安全性的开发人员来说，现在还没有理由恐慌。

## 更新:DexGuard 源代码没有泄露

DexGuard 的源代码似乎没有泄露，而是泄露了配置文件和其他工具，以帮助开发人员开始使用它。

* * *

[**来源:TorrentFreak**](https://torrentfreak.com/stolen-android-anti-piracy-software-dumped-on-github-180818/)

[**Via:AndroidPolice**](https://www.androidpolice.com/2018/08/18/oops-dexguard-tool-protect-android-apps-hacking-code-leaked-online/)