# 从 Pixelbook 开始，Chrome 操作系统将支持 Linux 应用程序

> 原文：<https://www.xda-developers.com/chrome-os-linux-app-support-google-pixelbook/>

在 Chrome OS 早期历史的大部分时间里，这个操作系统被视为一个美化了的网络浏览器。随着操作系统的成熟，这种观点已经变得毫无根据:Chrome 操作系统后来增加了离线功能和 Android 应用支持，以显著扩展其功能集。谷歌的下一个重大举措是通过引入 Linux 应用支持来吸引开发者，该应用支持在谷歌 Pixelbook 上以预览形式提供。

对于预算有限的人来说，Chromebooks 是非常好的机器，由于 Android 应用程序和[渐进式网络应用程序](https://www.xda-developers.com/tag/progressive-web-apps/)的不断增长的应用程序支持，这意味着大多数用户在从可比的[微软 Windows](https://www.xda-developers.com/tag/windows/) 或 macOS 笔记本电脑转移时几乎没有牺牲。然而，对于开发者来说， [Chrome OS](http://xda-developers.com/tag/chromebooks) 不提供像 Visual Studio、 [Firebase](https://www.xda-developers.com/tag/firebase/) 、Google Cloud SDK 或 [Android Studio](https://www.xda-developers.com/tag/android-studio/) 这样的工具，这使得 [Chromebook](https://www.xda-developers.com/tag/chromebook/) 很难销售。像[谷歌 Pixelbook](https://www.xda-developers.com/high-end-google-pixelbook-launch/) 这样的高端 Chromebooks 当然能够在移动中处理开发，但软件支持还没有到位。

有进取心的开发人员已经使用了面包丁安装了 T2 的 GNU/Linux 发行版，但是这需要一定程度的技术知识，这让很多人感到不快。此外，油炸面包丁并不是一个完美的解决方案，因为您可能会遇到令人讨厌的错误，需要同样令人讨厌的解决方法。最后，启用油炸面包丁需要切换到开发者模式，这意味着失去安全措施，如[验证启动](https://www.chromium.org/chromium-os/chromiumos-design-docs/verified-boot)。但由于谷歌在容器方面的工作，这种情况在未来将会改变。

 <picture>![Screenshot of Crouton installation](img/78edd3558c80e4432cc0c41a08a11376.png)</picture> 

Installing Crouton, an open-source toolkit for accessing Linux apps on Chrome OS 

## Chrome 操作系统上的 Linux 应用

由于容器化，Linux 应用程序支持将成为可能。这种集成将比通过 chroot 运行 GNU/Linux 发行版更加无缝:你可以通过鼠标点击从启动器启动 Linux 应用程序，移动窗口，直接从应用程序打开文件。应用程序窗口主题甚至将基于 [Adapta Gtk 主题](https://www.xda-developers.com/chrome-os-native-linux-apps-material-design-theme/)的修改版本，一个美丽的[材质设计](https://www.xda-developers.com/tag/material-design/)启发的主题。你将可以使用大多数 GNU/Linux 发行版上可用的各种流行开发工具，谷歌希望这些工具能够说服开发人员开始在 Chromebook 上开发，而不是在苹果 MacBook 或微软 Surface 上开发。对于那些熟悉桌面 Linux 的人来说，你不必改变安装新应用的方式:通过命令行中的 apt-get 安装或下载 tarballs 都可以。

Chrome OS 上的 Linux 应用程序支持被谷歌内部称为“Crostini ”,在过去的几周内[我们对它进行了广泛的跟踪](https://www.xda-developers.com/linux-apps-chrome-os-overview-crostini/)。在最新的 Dev 或 Canary 频道上，一些 Chromebook 用户可能已经注意到了设置中 Linux 应用程序的一个新菜单项:这是针对 Crostini 的，虽然它只在谷歌 Pixelbook 上运行，但谷歌承诺未来将为其他 chrome book 提供支持。谷歌希望确保 Crostini 在更大范围的推广之前足够好，并首先在较小的用户群中进行测试(即敢于在 Dev 或 Canary 频道上运行他们的机器的 Pixelbook 所有者)他们将能够尽可能多地消灭 bug。

 <picture>![Linux app Chrome OS](img/2723172d6e84544ac1cf5cd62e7a5e57.png)</picture> 

Linux app settings in Chrome OS. Source: [AboutChromebooks](https://www.aboutchromebooks.com/news/linux-apps-project-crostini-option-appears-in-chrome-os-settings-on-dev-channel/).

但不要指望 Crostini 会推广到市场上的每一款 Chromebook。Chrome OS 产品管理总监刘戡表示，由于 Crostini 利用的底层技术，Linux 应用支持**需要 Linux 内核 4.4 及以上版本**。目前，GPU 加速不可用，所以那些希望在 Chromebook 上玩游戏的人运气不好。正如[发现](https://www.reddit.com/r/chromeos/comments/8g6vxp/gpu_acceleration_coming_to_linux_apps_on_chrome/)我们自己的[基兰宫本](https://www.xda-developers.com/author/kieranmiyamoto/)和确认刘先生，但是， **GPU 加速支持将在今年晚些时候**。

目前，该团队希望专注于开发人员的需求。如果你最近看了一本 Pixelbook，那么现在是一个加入的好时机。你也可以等一等，因为其他 Chromebook 制造商正在开发高端 Pixelbook 竞争对手。鉴于近年来 Chrome OS 的快速扩张，无论现在还是未来投资一台 Pixelbook 或其他 Chromebook 都是一个好主意。

## 为快速增长的 Chromebook 用户群开发

谷歌的 Chrome 操作系统是教育领域的巨头。据 [NPD](https://www.npd.com/wps/portal/npd/us/home/) 称，Chromebooks 在 2017 年黑色星期五周期间推动了近四分之一的笔记本销量。此外，2017 年 Chromebooks 的销量是 2016 年的两倍。[运行操作系统](https://www.xda-developers.com/acer-chromebook-tab-chrome-os-tablet/)的平板电脑即将问世，这要归功于学校对外形的兴趣。随着操作系统[变得更加触摸友好](https://www.xda-developers.com/google-chrome-material-design-2-android-p/)，为触摸屏 Chrome 操作系统设备设计的应用需求不断增长。

以现在流行的 [Evernote](https://evernote.com/) 笔记 app 为例。在一项案例研究中，该公司声称，在为触摸屏手写实现低延迟手写笔 API 后，Pixelbook 用户在该应用上花费的时间是普通用户的 4 倍。另一款名为 [Squid](https://play.google.com/store/apps/details?id=com.steadfastinnovation.android.projectpapyrus&hl=en) 的笔记应用也因[针对 Chrome 操作系统](https://www.youtube.com/watch?v=Oc66T_e7xwU)的优化而取得了巨大成功:Chromebooks 在过去 30 天里占其整体用户群的 7%，但占其收入的 21%。

 <picture>![Evernote Pixelbook](img/342e355370ba2d45f6c5c12b65f293e8.png)</picture> 

Virtual stylus input in the Evernote app on the Google Pixelbook. Source: [Evernote](https://blog.evernote.com/blog/2017/10/31/whats-new-evernote-pixelbook/).

## 结论

Chrome 操作系统因其速度、简单性和安全性而备受推崇。这是一个操作系统，开发者经常推荐他们不懂技术的朋友和家人使用，以使他们的生活更轻松。但是操作系统并不能说服开发者真正迁移到生态系统。向操作系统添加 Linux 应用程序支持是实现这一目标的重要一步。