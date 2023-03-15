# 谷歌正在为 Chromebooks 添加亮/暗主题切换

> 原文：<https://www.xda-developers.com/google-adding-light-dark-theme-toggle-chromebooks/>

无论你使用的是 iOS 还是 Android，现在你可能已经习惯了在明亮和黑暗的系统主题之间切换。Chrome OS 上的情况有所不同，它混合了两者，在整个系统中使用了一些明暗元素。然而，根据大量报道，这种情况显然将会改变。

*[Chrome Story](https://www.chromestory.com/2020/08/chromebook-dark-mode/)* 首先发现代码变化，表明谷歌正在努力实现一个 UI 改造，允许用户在亮暗主题之间切换。目前，Chrome OS 在文件管理器和设置页面等地方加入了轻量元素。与此同时，书架、快速设置托盘和应用程序抽屉中也有深色元素。

根据 Android policye 的说法，谷歌正在做的是创建一个浅色主题，然后可以作为基线来建立一个合适的深色主题。该网站指出了 [Chromium Gerrit](https://chromium-review.googlesource.com/c/chromium/src/+/2363799) 中的几项提交，其中一项透露了对“login-constants.h”的关键更改。根据代码，当灯光主题打开时，如果 Chrome OS 无法从当前壁纸中提取主要颜色，它将在给锁屏着色时使用白色作为基础。

Chrome OS 中的明暗主题。来源:[9 to 5 Google](https://9to5google.com/2020/09/22/chrome-os-light-theme-demo-gallery/)

多亏了 Chrome OS Canary 的最新版本，谷歌 能够看到这些变化。在新版本中，你会在快速设置面板中找到一个开关，用户可以在他们认为合适的时候关闭和打开它。据我们所知，Chrome OS 的灯光主题仍在进行中，因为一些元素很难看到，例如时钟。

更多灯光主题设置。来源:[9 to 5 Google](https://9to5google.com/2020/09/22/chrome-os-light-theme-demo-gallery/)

虽然有大量证据表明谷歌正在努力为 Chrome OS 带来明暗主题切换，但还不知道这些变化何时能供 Chromebook 用户试用。正如 Android Police 指出的，Chrome OS 以前以黑暗主题为特色，但错误的代码导致一些 Chromebooks 无法使用。希望在最新的变更中，能够更加小心地避免任何这样的问题。

为 Chromebook 用户提供在亮暗主题之间切换的选择应该会提高可用性。像 Chrome 操作系统目前所做的那样，混合使用两者，不仅显示出缺乏一致性，也剥夺了用户的选择。虽然黑暗模式很酷，但有些人很难看到。其他人可能会注意到，在灯光模式下，他们的眼睛会更快疲劳。

目前还不清楚 Chromebook 用户是否只能手动切换模式，或者是否会有一种模式可以根据一天中的时间自动切换明暗主题。目前还不清楚这种切换将如何与能够检测系统主题并相应改变其用户界面的应用程序和网页进行交互。

潜在的明暗主题的到来只是 Chrome OS 众多新功能中的一个。据称，谷歌还在开发一个“ [Holding Space](https://www.xda-developers.com/holding-space-chrome-os-quick-access-screenshots-downloads-shelf/) ”功能，该功能将让用户快速访问截图和下载，以及用于屏幕录制的“[捕捉模式](https://www.xda-developers.com/chrome-os-getting-capture-mode-screen-recording-chromebooks/)。