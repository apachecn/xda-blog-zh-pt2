# Google Duo 的新机器学习模型提高了通话中的音频质量

> 原文：<https://www.xda-developers.com/google-duo-ai-waveneteq-machine-learning-model-audio-call-quality/>

谷歌有一段不愉快的历史，它杀死了通讯应用程序，而支持更新的通讯应用程序，这些应用程序最终也会被杀死。到目前为止，Google Duo 是一个例外，因为它是与现已倒闭的信息服务 Allo 一起推出的。Duo 不断受到谷歌的关注，并频繁添加新功能，如 5G 三星 S20 手机上的 [1080p 支持](https://www.xda-developers.com/google-duo-galaxy-s20-1080p-video-5g/)、【即将推出】、[直播字幕](https://www.xda-developers.com/google-duo-prepares-to-add-captions-to-video-and-audio-messages/)、[涂鸦](http://xda-developers.com/google-duo-update-adds-notes-doodles/)，以及多达 [12 名参与者的群组通话](https://www.xda-developers.com/google-duo-group-video-calling-live/)。现在，谷歌正在应用机器学习来消除抖动的主要问题，以获得更流畅和不间断的音频体验。

在新冠肺炎隔离期间，视频通话已经成为一种重要的官方沟通方式，紧张的音频会让你或你的公司付出经济代价。谷歌承认，Duo 上 99%的通话因网络延迟而中断。大约五分之一的通话会丢失 3%的音频，而十分之一的通话会丢失近 8%的音频，其中大部分可能是非常重要的信息，你最终会错过这些信息。当数据包在传输中被延迟或丢失时，就会发生这种情况，这些数据包的缺失会导致音频中的毛刺，使许多内容无法理解。

谷歌新的 WaveNetEQ 机器学习算法基于一种叫做“丢包隐藏”(PLC)的技术。WaveNet EQ 是一个基于 [DeepMind 的](https://deepmind.com/) [WaveRNN](https://arxiv.org/abs/1802.08435) 的生成模型，它创建大量音频，用逼真的填充物填补空白。人工智能模型已经通过输入大量语音相关数据进行了训练。由于 Google Duo 中的端到端加密，该模型在接收者的设备上运行。但谷歌声称，它的速度足够在手机上运行，同时仍能提供最先进的音频质量。

WaveRRN 依赖于文本到语音的模型，除了接受“说什么”的训练外，它还接受了“如何说”的训练。它以很强的语音理解能力分析输入，以预测不久的将来的声音。除了填充间隙之外，该模型还在原始波形中产生多余的音频，以覆盖抖动之后的部分。该信号与实际音频重叠，带有一点交叉衰落，导致更平滑的过渡。

Google Duo 的 WaveNetEQ 模型已经由 100 个人用 48 种语言进行了训练，因此它可以学习人类声音的一般特征，而不仅仅是一种语言。该模型经过训练，主要产生音节，可以填补长达 120 毫秒的空白。

该功能已经在谷歌 Pixel 4 上提供，现在正在推广到其他 Android 设备。

* * *

**来源:[谷歌 AI 博客](https://ai.googleblog.com/2020/04/improving-audio-quality-in-duo-with.html)**