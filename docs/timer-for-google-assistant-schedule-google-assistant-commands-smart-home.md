# 这位开发者制作了一个工具来安排谷歌助手的命令

> 原文：<https://www.xda-developers.com/timer-for-google-assistant-schedule-google-assistant-commands-smart-home/>

谷歌助理作为数字助理提供了许多功能，其中相当一部分扩展到了智能家居和自动化领域。谷歌通过[例程](https://www.xda-developers.com/google-home-scheduled-routines/)为智能家居提供了一些日程安排功能，允许用户在满足特定条件的任何时候例行启动特定任务。多年来，[例程下的功能已经扩展了](https://www.xda-developers.com/google-assistant-clock-routines-broadcast-replies/)，但在智能家居自动化的背景下，谷歌助手到底能实现什么，仍有很大的改进空间。现在，一名开发者开发了一款开源工具，可以让你安排谷歌助手的命令，为智能家居和其他领域开辟了一系列功能和用例。

wiseindy 的 Google Assistant 计时器允许你向 Google Assistant 发送命令，这些命令将在特定时间后执行，或者延长特定的持续时间。该项目利用 IFTTT 和一个面向互联网的网络服务器与谷歌助手和你的智能设备进行通信。一旦设置好，你可以发送类似“*嘿谷歌，10 分钟后关灯*”的命令，在特定的持续时间后执行一个动作。该项目已经扩展了这个指令集，使其可以使用持续时间命令，如*“嘿，谷歌，打开风扇 25 分钟”*，这将立即发送一个命令，并在持续时间后发送最后一个命令。

该应用程序不直接与您的本地设备通信，而是使用 IFTTT 作为这种通信的连接媒介。当您要求 Google Assistant“在 5 分钟后关闭设备”时，它会将该命令发送给 IFTTT，if TTT 又会使用设备名称和参数“5 分钟”向您的服务器发出 HTTP 请求。服务器打开设备并等待指定的时间。一旦时间过去，服务器将向 IFTTT 发出 web 请求，该请求将告诉 Google Assistant 关闭设备。因此，您需要一个始终运行的 Node.js 服务器，IFTTT 可以与之对话，尽管它不需要运行在同一个网络上。

**[谷歌助手的计时器——Github](https://github.com/wiseindy/timer-for-google-assistant)**

设置项目需要几个步骤，但是附带的 readme 很方便，将为您提供足够的指导。该项目也是开源的，因此您可以自己检查代码并做出贡献。目前的应用和用例是在智能家居的背景下设想的，但也许社区可以将其扩展到其他新颖的用途。