# Live Transcribe 2.1 准备添加紧急警报检测、智能片段和扬声器 ID

> 原文：<https://www.xda-developers.com/live-transcribe-2-1-prepares-to-add-emergency-siren-detection-smart-segments-and-speaker-id/>

今年早些时候，在谷歌 I/O 大会上，该公司[推出了两款新的安卓应用](https://www.xda-developers.com/live-transcribe-sound-amplifier-google-hearing-impaired/)来帮助有听力障碍的人——实时转录和声音放大器。虽然这两个应用最初都是针对听力受损者的，但谷歌后来[更新了实时转录应用](https://www.xda-developers.com/google-live-transcribe-sound-events-save-transcripts/)，以帮助学生和记者。更新后，该应用程序允许用户在本地设备上保存转录，甚至能够在转录过程中检测声音事件。现在，谷歌似乎正在为这款应用做准备，以引入另外三个功能。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些特性目前还没有在实时构建中实现，并且可能会被开发人员在未来的构建中随时引入。

Live Transcribe 的最新更新(版本 2.1.276871059)的拆解揭示了暗示即将到来的功能的代码字符串，包括显示紧急警报、智能片段和扬声器 ID。显示紧急警报功能将允许应用程序识别紧急警报并提醒用户。这些字符串还包括一个功能对话框，说明“当报告警报时，请谨慎操作。请记住，并非所有的警笛都需要行动或指示相关的紧急情况(例如，电视上的警笛)。此外，我们的警报器检测偶尔会出错。”

```
 <string name="show_emergency_siren_dialog_message">Please exercise caution when sirens are reported. Remember that not all sirens require action or indicate a relevant emergency (sirens on TV, for example). Furthermore, our siren detection will occasionally make mistakes.</string>
<string name="show_emergency_siren_title">Show Emergency Sirens</string>
<string name="smart_segment">Smart segment</string>
<string name="smart_segment_summary">Segment transcript based on performance (rather than text length)</string>
<string name="speaker_id_title">Enable speaker ID</string> 
```

智能段功能将根据表现而不是文本长度来划分抄本，发言者 ID 功能将帮助应用程序识别和标记正在进行的对话中的发言者。我们的主编米沙·拉赫曼(Mishaal Rahman)也看了一下[Live transcript GitHub 知识库](https://github.com/google/live-transcribe-speech-engine)，其中[包含用于与谷歌的云语音 API](https://www.xda-developers.com/google-io-2019-app-live-transcribe-speech-engine-open-source/) 通信的 Android 客户端库，并发现自动语音识别(ASR)模块支持内置的说话人识别。然而，没有提供扬声器 ID 实现，看起来应用程序目前没有它，但在不久的将来可能会改变。

* * *

*感谢 PNF 软件为我们提供了使用许可 [JEB Decompiler](https://www.pnfsoftware.com/?aid=xdadev) ，这是一款针对 Android 应用的专业级逆向工程工具。*