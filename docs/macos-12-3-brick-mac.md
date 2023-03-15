# macOS Monterey 12.3 正在用替换下来的逻辑板砌砖一些 MAC 电脑

> 原文：<https://www.xda-developers.com/macos-12-3-brick-mac/>

苹果在 2021 年末发布了 macOS Monterey 12，引入了新的 FaceTime 和 Safari 功能，以及其他改进。自那以后，该公司一直致力于进一步丰富操作系统。本周早些时候，库比蒂诺科技巨头发布了[MAC OS Monterey 12.3](https://www.xda-developers.com/mac-os-monterey-12-3-released/)——这是这个主要版本的最新更新。它带来了期待已久的[通用控制](https://www.xda-developers.com/how-to-use-universal-control/)功能，并支持新的 Unicode 14.0 表情符号。此外，它还带来了一个令人讨厌的惊喜，影响了一些不幸的用户。最近的在线报告表明，在更换了主板的 MAC 电脑上更新到 macOS 12.3 可能会使其崩溃。

苹果开发者论坛上的用户一直在抱怨最新的 macOS 12.3 更新。一些更换了苹果电脑主板的人报告说出现了无限循环和其他问题，导致他们无法使用苹果电脑。他们强调了以下流程的细节:

> 循环是:
> 
> 您尝试升级，升级将失败，但恢复正确处理它，您仍将在 12.2.1 上重新启动，但有一个报告问题对话框通知您 iBoot 死机
> 
> 您将尝试再次升级。这一次，iBoot 固件将会损坏。在看到感叹号符号告诉您需要恢复之前，您会在启动时看到苹果图标闪烁 5-6 次。
> 
> 您可以尝试使用第二台带有 Apple Configurator 2 的 Mac 来恢复。这将会失败，因为它会尝试从 IPSW 加载 12.3 固件，无论是在 DFU 模式还是恢复模式下。
> 
> 让事情再次运行的唯一方法是手动下载 12.2.1 IPSW，并在 Mac 处于 DFU 模式下使用 Apple Configurator 2 来加载 revive 映像。这将更新 iBoot 的固件，并将恢复映像更新到工作版本。然后，Mac 将恢复 12.2.1 的操作系统，并在完成后保留您的数据。

目前还不清楚苹果是否意识到了这个问题。然而，可以肯定的是，该公司最终会修补这个严重的缺陷。与此同时——如果你已经更换了 Mac 的主板——不要升级到 macOS 12.3。

*升级到 macOS Monterey 12.3 会对你的 Mac 造成影响吗？请在下面的评论区告诉我们。*

* * *

**来源:** [*苹果开发者论坛*](https://developer.apple.com/forums/thread/701681)

**Via:**[MAC rumors](https://www.macrumors.com/2022/03/17/macos-monterey-bricking-macs-logic-boards/)