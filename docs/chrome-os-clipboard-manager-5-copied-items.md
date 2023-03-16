# Chrome OS 正在为最近复制的 5 个项目获取剪贴板管理器

> 原文：<https://www.xda-developers.com/chrome-os-clipboard-manager-5-copied-items/>

# Chrome OS 获得了一个剪贴板管理器，可以存储最近复制的 5 个项目

根据一项新的承诺，Chrome OS 将获得与 Windows 10 的剪贴板管理器快捷方式几乎相同的功能。

复制和粘贴是我们大多数人每天都在使用的一个基本功能。如果你在电脑上做很多工作，那就更重要了。Windows 10 有一个很方便的功能(Windows key + V)，可以让你看到最后复制的几个东西。Chrome OS 将很快获得一个非常相似的剪贴板管理功能。

根据 Chromium Gerrit 中一项名为“Multipaste”的新承诺，Chrome OS 将获得与 Windows 10 几乎相同的功能。相关标志(chrome://flags/#multipaste)解释道:“按 Search + V 会显示一个菜单，允许你粘贴之前复制的东西。”对于那些不熟悉的人来说，搜索键本质上是 Chrome OS 版本的 Windows 键，因为它被用在许多常见的键盘快捷键中。

进一步观察提交，我们可以看到 Chrome OS 的剪贴板管理器将存储最近复制的五个项目。这些东西可以包括文本、格式化文本、图像、书签格式的链接，以及一个叫做“ [web 智能粘贴](https://chromium-review.googlesource.com/c/chromium/src/+/2240267/10/ash/tote/multipaste_controller.cc#61)的神秘东西。也有可能在快速设置托盘中会有一个[按钮，在没有快捷键的情况下调出剪贴板管理器。](https://chromium-review.googlesource.com/c/chromium/src/+/2188934/6/ash/system/status_area_widget.h#30)

不能保证这个新的剪贴板管理器能够稳定的运行在 Chrome 操作系统上，但是如果可以的话，它会非常有用。Windows 10 的功能非常方便，甚至 [Gboard 也有类似的东西](https://www.xda-developers.com/gboard-clipboard-manager/)。如果你做了大量的复制和粘贴，你就会知道不小心“覆盖”了你最后复制的东西是多么的烦人。这将是一个很大的时间节省，虽然我们希望它将被升级，让你保存不止五个项目。

* * *

**来源:[Chromium Gerrit](https://chromium-review.googlesource.com/c/chromium/src/+/2240267)| Via:[9 to 5 Google](https://9to5google.com/2020/06/25/chrome-os-clipboard-manager/)**