# [更新:“精选手机”上的直播字幕]谷歌致力于 Android Q 上的直播字幕、直播转播和直播转录

> 原文：<https://www.xda-developers.com/google-accessibility-live-caption-android-q-live-relay-live-transcribe/>

**更新 1(美国东部时间 2019 年 5 月 10 日晚上 11 点 53 分):**据 *VentureBeat* 报道，直播字幕将不会在所有运行 Android Q 的设备上提供。下面是更多细节。

作为消费者，我们常常认为我们周围的世界是理所当然的。我们所经历的，我们假设我们周围的每个人都以相似的方式经历着同样的事情，如果不是一样的话。这个假设延伸到我们生活的每一个部分，包括技术。但是残疾是真实存在的，由于这些假设，与残疾一起生活成为一项具有挑战性的任务。因此，无障碍成为一个重要的话题，谷歌正在尽自己的努力，确保残疾人有平等的机会享受这些体验。Android Q 整合了谷歌的几项可访问性工作，使 Android 成为一个更具凝聚力的体验，尽管下面提到的所有功能目前在 Android 中都不可用。

## 实时字幕

我们中的很多人从来懒得看一眼字幕设置，我们也消费了很多媒体，甚至没有注意到字幕的缺失。但是对于世界上 4.66 亿失聪和重听的人来说，文字说明的作用大于方便——它们是体验的媒介。Android Q 集成了实时字幕，让聋人社区的用户能够更轻松、更普遍地获得体验。

启用该设置后，只需轻轻一点，实时字幕就会自动为正在设备上播放音频的媒体添加字幕。实时字幕可以处理视频、播客、音频信息和任何其他应用程序，甚至可以处理设备上正在录制的内容。一旦检测到语音在设备上播放，字幕就会出现。由于所有这一切都是通过设备上的语音识别进行的，音频和字幕都不会离开你的手机，你可以在不需要 WiFi 或蜂窝数据的情况下使用该功能。

**2019 年 5 月 10 日更新:**谷歌已经与 [*VentureBeat*](https://venturebeat.com/2019/05/10/how-android-qs-live-caption-works-select-phones/) 确认，直播字幕将是“今年晚些时候选择运行 Android Q 的手机”具体来说，“选择更高端的设备，”Android 辅助功能产品经理 Brian Kemler 说。原因显然是由于内存和空间的限制。最初的推出将是有限的，但随着时间的推移将会扩大，谷歌计划在我们接近第一次公开 Android Q 发布时发布一系列支持直播字幕的设备。

此外，谷歌证实，保存转录对于直播字幕将是不可能的(由于 AudioPlaybackCaptureConfiguration API 中的有意限制)，它将不适用于电话呼叫、语音呼叫或视频呼叫(因为 API 不支持)，并且它将只支持发布时的英语字幕。一旦该功能启动，将会下载一个离线模型，并通过 Google Play 服务提供该模型的更新。

## 现场转播

Live Relay 基于 Live Caption 提出的理念，允许人们在不说话或听不到的情况下拨打和接听电话。

Live Relay 使用设备上的语音识别和文本到语音的转换，允许电话收听音频呼叫，然后代表键入响应的用户说出响应。该功能与预测性写作建议功能协同工作，如[智能撰写](https://www.xda-developers.com/smart-compose-gmail-android-more-users/)和[智能回复](https://www.xda-developers.com/google-ml-kit-sdk-adds-smart-reply-language-identification-api/)，通过帮助快速响应，更容易保持通话。直播中继完全在设备上运行，因此通话仍然是私密的。由于 Live Relay 通过常规电话与另一端进行交互，因此它也可以与另一端的座机一起工作。

虽然实时转播肯定会对聋人群体和哑巴群体有所帮助，但它的使用案例会扩展到某些人可能无法说话或听到电话呼叫，但仍希望与之互动的情况。谷歌还对在 Live Relay 中集成实时翻译功能持乐观态度，这反过来又有可能让任何人打电话给世界上的任何人，不分语言障碍地进行交流。

谷歌表示，直播转播仍处于研究阶段。目前还不清楚该功能是否已经集成到当前的 Android Q 版本中——我们猜测它将在未来进入 Android 设备。

## 为有语言障碍的用户提供实时转录扩展

Google 今年早些时候展示了 Live Transcribe，这是一款为失聪用户提供的工具，帮助他们实时转录周围的语音。该应用旨在通过手机麦克风将现实世界的语音转换为实时字幕，从而使日常对话更容易理解。Live Transcribe 是[已经可以通过 Play Store](https://play.google.com/store/apps/details?id=com.google.audio.hearing.visualization.accessibility.scribe) 作为早期访问限制测试版，支持超过 70 种语言和方言。Pixel 3 设备上也预装了该应用程序。

谷歌在改善可访问性方面的最新努力不仅将实时转录扩展到了聋人用户，还通过 Euphonia 项目扩展到了有语言障碍的用户。

Euphonia 项目下的团队正在使用人工智能来提高计算机理解不同语音模式的能力，包括受损的语音。谷歌已经与 ALS Therapy Development Institute 和 ALS Residence Initiative 等非营利组织合作，记录受 ALS 影响的人的声音，然后使用这些记录来训练人工智能模型，以更可靠地转录有这种语言困难的人所说的话。当前的一套人工智能算法与英语一起工作，以适应患有 als 相关障碍的个人，但谷歌对这项研究应用于更大的群体和不同的语言障碍持乐观态度。

此外，谷歌还在此基础上训练个性化的人工智能算法来检测声音和手势，然后采取行动，如向谷歌主页发出口头命令或发送文本消息。这个用例对严重残疾、不能说话、只能用非语音声音和面部手势进行交互的人特别有帮助。

这些新功能似乎还没有出现在 Live Transcribe 中。谷歌正在请求那些说话含糊不清或难以理解的志愿者提供帮助，如果他们愿意记录一组短语，以帮助进一步训练系统更好地工作。如果您符合条件并希望成为志愿者，请[填写同一](http://bit.ly/AudioData)的表格。

谷歌在提高技术可及性方面的努力当然值得称赞。我们希望更多的软件公司致力于为不同能力的个人提供公平的世界体验。

* * *

[**来源 1:谷歌**](https://www.blog.google/products/android/android-q-io/) [**来源 2:谷歌**](https://www.blog.google/outreach-initiatives/accessibility/live-relay-phone-calls-io/) [**来源 3:谷歌**](https://www.blog.google/outreach-initiatives/accessibility/live-relay-phone-calls-io/)