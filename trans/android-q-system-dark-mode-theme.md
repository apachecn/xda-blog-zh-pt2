# Android Q 可能最终会带来一个全系统的黑暗模式

> 原文：<https://www.xda-developers.com/android-q-system-dark-mode-theme/>

在 Android 5.0 Lollipop 及其材质设计 UI 发布之前，Android SystemUI、框架和大多数应用程序，无论是第一方还是第三方，都按照赫萝使用了更深的颜色。自从材料设计成为 Android 的指导设计原则，大多数应用程序都改变了用户界面的颜色，使用大量的白色。最近，我们看到谷歌开始在他们的一些应用程序中提供深色主题，因为他们意识到[深色可以提高配备有机发光二极管面板的设备的电池寿命](https://www.xda-developers.com/google-wants-developers-to-add-dark-themes-to-save-battery-life/)。现在，谷歌似乎终于再次拥抱黑暗主题，因为一名谷歌人表示，黑暗模式是一个批准的 Android Q 功能。

在 Chromium Gerrit(被 *AndroidPolice* 发现)中，一名谷歌人为谷歌 Chrome 的新功能创建了一个名为“修改核心 UI 元素并创建设置以启用黑暗模式”的跟踪器。在功能描述中，谷歌称“黑暗模式是一个被认可的[Android] Q 功能。”他继续说，“[Android] Q 团队希望确保所有预装的应用程序都支持原生黑暗模式。”我们很确定，当他们说“所有预装应用”时，他们指的只是 AOSP 应用，所以我们认为谷歌打算让他们所有的第一方预装应用都有黑暗主题。我们已经看到[谷歌手机应用](https://www.xda-developers.com/google-phone-v26-dark-theme/)、[谷歌联系人](https://www.xda-developers.com/google-contacts-adds-dark-theme/)、[消息](https://www.xda-developers.com/android-messages-redesign-dark-mode/)、[谷歌新闻](https://www.xda-developers.com/google-news-5-5-dark-theme/)、[谷歌游戏](https://www.xda-developers.com/google-play-games-dark-theme/)和 [YouTube](https://www.xda-developers.com/youtube-dark-mode-android-roll-out/) 获得了原生黑暗主题，因此已经有很好的证据表明谷歌打算将黑暗主题添加到他们所有的应用中。

由于谷歌 Chrome 没有深色主题(至少，[没有在手机上使用](https://www.xda-developers.com/google-chrome-windows-10-dark-mode/)), Chrome 团队需要在 Chrome 浏览器中实现深色主题元素。该团队表示，Chrome 需要“所有的 UI 元素”，以理想地“在 2019 年 5 月前以黑暗为主题”，这是谷歌 I/O 2019 预计发生的时间。尤其是 Chrome，只有核心的 UI 元素，比如 Omnibox、工具栏、设置/下载/历史页面等等。将是黑暗的主题，所以这意味着网页不会被修改为黑暗。

虽然功能描述多少暗示了 Android Q framework 团队对下一个 Android 版本的全系统黑暗模式计划，但谷歌的后续评论提供了更强有力的证据，表明该公司打算将全系统黑暗主题作为面向用户的设置。评论告知测试人员如何测试谷歌 Chrome 的黑暗模式。在 Android Pie 中，测试人员需要在开发者选项中启用“夜间模式”。在 Android Q 中，测试人员需要在显示设置中启用类似的系统范围的夜间模式功能，这可以为“系统 UI 和应用程序”启用夜间模式

如果你还记得的话，谷歌 Pixel 3 [搭载的安卓派 DR1 版本改变了开发者选项中夜间模式设置的工作方式](https://www.xda-developers.com/google-pixel-3-automatic-dark-theme-option/)。这个设置就像一个全系统黑暗主题的开关，除了只有消息和谷歌地图的闪屏会受到这个变化的影响。再过几个月，谷歌将不再对 Android Q 的核心功能进行修改，因此这种全系统的黑暗模式仍有可能永远不会出现。功能描述和后续评论都是在 2018 年 10 月 31 日做出的，所以有可能谷歌的计划从那时起*已经*改变了。在 Android Q 开发者预览版发布之前，我们不会知道。

第一个 Android Pie 开发者预览版于 2018 年 3 月发布，因此我们预计在 2019 年 3 月的某个时候发布第一个 Android Q 开发者预览版时，会确认或否认黑暗模式功能的存在。然而，今年谷歌可能会允许一些 Project Treble 兼容设备通过 GSI 测试 Android Q，而不是仅限于谷歌 Pixel 智能手机和合作伙伴的少数设备。因此，您可能不必等到 Android Q 源代码发布后再在您的设备上测试下一个版本。

我真的希望谷歌会重新接纳应用程序中的黑暗主题。我非常喜欢一加和三星在系统范围内实现黑暗主题的方式。我希望谷歌能允许更多的用户界面定制，因为安卓奥利奥[允许安装第三方覆盖层](https://www.xda-developers.com/custom-themes-android-oreo-substratum/)。可悲的是，Android Pie [阻止了第三方覆盖](https://www.xda-developers.com/rootless-custom-themes-android-p/)的安装，这并不令人惊讶，但对于那些喜欢传统 Android 体验但不喜欢 UI 有多亮的用户来说，仍然令人失望。请不要玩弄我的情绪，谷歌。

* * *

[**来源:铬 Gerrit**](https://bugs.chromium.org/p/chromium/issues/detail?id=900782&desc=3)[**Via:AndroidPolice**](https://www.androidpolice.com/2019/01/06/googler-seemingly-confirms-that-android-q-will-have-system-wide-dark-mode/)