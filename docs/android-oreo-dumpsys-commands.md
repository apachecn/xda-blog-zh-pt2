# OEM 厂商不得修改 Android Oreo 中的 Dumpsys 命令

> 原文：<https://www.xda-developers.com/android-oreo-dumpsys-commands/>

# OEM 厂商不得修改 Android Oreo 中的 Dumpsys 命令

谷歌声明，原始设备制造商不允许修改某些 dumpsys 命令的格式或内容，这些命令对新的 Android Oreo 更新的开发者很有用。

每年，Google 都会发布他们兼容性定义文档的更新版本。这些是每个原始设备制造商必须遵守的规则，如果他们想要发布自己的内置 Google Play 服务的 Android 版本。这意味着[新的限制可以到位](https://www.xda-developers.com/android-oreo-oem-background-app-limitations/)但也意味着[以前的限制可以放松](https://www.xda-developers.com/google-daydream-vr-6-3-display/)。我们在 Android Oreo 中发现的另一个新变化是要求 OEM 厂商**不能修改 Dumpsys 命令的格式或内容**。

Dumpsys 是 ADB 执行的一个命令，它输出与智能手机硬件和软件相关的各种信息。大多数 Android 的普通用户可能不知道 Dumpsys 的好处是什么，但有些人可能知道什么是电池历史记录。谷歌过去在电池统计方面更慷慨，但 KitKat 的发布使他们对第三方应用程序增加了一些限制。然而，随着 Android 5.0 Lollipop 的发布，该公司宣布了一项名为电池历史学家的功能，这在一定程度上有助于填补这一空白。

我们能够通过 ADB 使用 Dumpsys 命令获得这种新型电池数据。对于那些好奇的人来说，这样做的命令是`adb shell dumpsys batterystats > batterystats.txt`，然后你可以获取该文本文件并创建一个更容易阅读的 HTML 版本[，这要感谢谷歌](https://developer.android.com/studio/profile/battery-historian.html)提供的 python 脚本。这些数据需要以特定的方式进行格式化，这样脚本才能正常工作，谷歌现在禁止原始设备制造商在 Android Oreo 中修改这样的命令。

开发人员可以通过 ADB 访问许多其他有用的 Dumpsys 命令。Google 要求 OEM 厂商不要修改的 Dumpsys 命令的完整列表是 batterystats、diskstats、fingerprint、graphicsstats、netstats、notification 和 procstats。在 ADB shell 中输入`dumpsys -l`可以找到任何 Android 设备上可用的 dumpsys 命令的完整列表。

这些命令提供的数据在调试和优化代码时对一些应用程序开发人员来说至关重要，谷歌希望这些命令的输出在任何设备上都保持一致。有些 dumpsys 命令是特定设备独有的，但至少 Google 确保了不管在什么设备上都可以使用这些有用的命令。