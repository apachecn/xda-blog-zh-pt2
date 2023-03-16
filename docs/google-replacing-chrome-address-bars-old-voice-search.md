# 谷歌将很快用这款助手取代 Chrome 旧的语音搜索

> 原文：<https://www.xda-developers.com/google-replacing-chrome-address-bars-old-voice-search/>

# 谷歌正致力于用谷歌助手取代 Chrome 地址栏旧的语音搜索

根据我们最近在 Chromium Gerrit 上发现的两次提交，谷歌计划用助手取代 Chrome 中的旧语音搜索。

去年年底，谷歌对 Android 平台的 Chrome 浏览器进行了一些新的改动，包括一些目前正在开发的功能。其中包括 Chrome 新标签页的[新用户界面，一个](https://www.xda-developers.com/google-tests-radically-new-ui-chromes-new-tab-page/)[截图编辑器](https://www.xda-developers.com/google-adding-screenshot-editor-chrome-android/)，一个[自定义分享表](https://www.xda-developers.com/google-chrome-android-testing-custom-share-sheet-canary/)，一个[标签组的二重奏友好用户界面](https://www.xda-developers.com/chrome-android-tests-duet-friendly-ui/)，以及对通知提示的一些[小改动。现在，我们有理由相信谷歌正在致力于用谷歌助手取代 Chrome 地址栏中的旧语音搜索 UI。](https://www.xda-developers.com/google-chrome-annoying-notification-prompts/)

我们在 Chromium Gerrit 中发现了两个新的提交，主题是“助理语音搜索”虽然这些提交的 bug 跟踪器是私有的，但是我们可以从注释和代码更改中收集一些信息。评论和代码更改显示，一旦提交被合并，一个名为“Omnibox 助手语音搜索”的新标志将出现在 chrome://flags # omni box-Assistant-Voice-Search for Android 设备中。根据其描述，新标志将“为 omnibox 语音查询使用助手”。这一变化背后的想法是，每当用户点击 Chrome 地址栏/地址栏/omnibox 中的语音搜索按钮时，都会向谷歌应用发送一个启动谷歌助手的意图。目前，当用户点击 Chrome 中的语音搜索按钮时，会弹出旧的 Android 语音搜索 UI，如下图所示。

谷歌目前正在开发这项功能，使用所谓的深度链接向谷歌应用程序发送意图，尽管负责代码更改的谷歌公司表示，计划是让 Deep Link“去 V1”这项功能。另一位谷歌人也加入了代码更改的行列，他说在合并这些更改之前还有很多工作要做，因为当前的实现没有告诉谷歌网络服务器(GWS)哪台设备正在发送搜索查询，破坏了默认的搜索引擎功能，并且不支持搜索查询提取。谷歌计划在 Chrome 版本 85 中发布该功能，目前计划在 2020 年 9 月 15 日的一周内转移到 stable。

* * *

**来源:Chromium Gerrit ( [1](https://chromium-review.googlesource.com/c/chromium/src/+/1999157/7) ， [2](https://chromium-review.googlesource.com/c/chromium/src/+/1997652) )**