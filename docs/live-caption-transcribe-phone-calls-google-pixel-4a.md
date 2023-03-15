# 直播字幕可以在谷歌 Pixel 4a 上转录电话

> 原文：<https://www.xda-developers.com/live-caption-transcribe-phone-calls-google-pixel-4a/>

在去年的谷歌 I/O 大会上，[谷歌推出了直播字幕](https://www.xda-developers.com/google-accessibility-live-caption-android-q-live-relay-live-transcribe/)，这是一项可在设备上转录回放音频的辅助功能。使用 Android 的 AudioPlaybackCaptureConfiguration API，实时字幕从设备中捕捉音频，并通过三个设备上的机器学习模型运行它，以从任何识别的英语语音中生成字幕。第一批获得直播字幕支持的设备是 [Pixel 4](https://forum.xda-developers.com/pixel-4) 和 [Pixel 4 XL](https://forum.xda-developers.com/pixel-4-xl) ，但谷歌后来将支持扩展到了 [Pixel 2 和 2 XL](https://www.xda-developers.com/live-caption-pixel-2-update/) 、 [Pixel 3 和 3a 系列](https://www.xda-developers.com/december-2019-android-security-patches/)、[三星 Galaxy S20 系列](https://www.xda-developers.com/samsung-galaxy-s20-google-live-caption/)、[一加 7T 系列](https://www.xda-developers.com/oneplus-7t-pro-open-beta-1-build-live-caption-support/)、[一加 8 系列](https://www.xda-developers.com/oneplus-8-series-update-adds-live-caption-bullets-wireless-z-integration-dolby-atmos/)、[一加诺德](https://www.xda-developers.com/oneplus-nord-review/)，以及现在的[新像素然而，随着谷歌 Pixel 4a 的推出，直播字幕得到了第一次功能升级:通过电话检测和转录语音的能力。](https://www.xda-developers.com/google-pixel-4a-specs-features-pricing-availability/)

我们第一次发现这个新功能的线索是在 4 月份，当时负责直播字幕的应用程序 Device Personalization Services 被拆除。这些字符串表明，用户将能够在电话通话中选择录制音频，如果他们选择这样做，他们对该功能的使用将被告知通话中的其他人。一旦启用该功能，通话中的其他方将听到以下内容:“嗨，您要与之通话的人已打开通话字幕。他们会看到你所说内容的字幕，以帮助他们听下去。”这将适用于语音和视频通话，并支持 Telegram、Facebook Messenger、WhatsApp 等应用程序。

**[谷歌像素 4a 论坛](https://forum.xda-developers.com/pixel-4a)**

除了引入转录电话的功能，谷歌还没有宣布对直播字幕的任何其他改进。它仍然只适用于英语语言的语音，仍然不适用于所有类型的媒体。然而，谷歌有可能会继续增加新功能，并且很可能在未来继续扩展对其他设备的支持。谷歌表示，转录电话将首先适用于其他带有实时字幕的 Pixel 设备(具体来说，Pixel 2、Pixel 3、Pixel 3a 和 Pixel 4)，但它很可能会推广到上述具有该功能的非谷歌设备，但我们没有确切的可用性或时间表。一旦我们找到答案，我们会更新这篇文章。