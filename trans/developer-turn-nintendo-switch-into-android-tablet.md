# 开发者正在将 Android 移植到任天堂 Switch

> 原文：<https://www.xda-developers.com/developer-turn-nintendo-switch-into-android-tablet/>

**更新 2(美国东部时间 2019 年 6 月 15 日晚上 8 点 15 分):**自从我们上一次发布这个项目以来，致力于任天堂 Switch Android 移植的开发人员已经取得了重大进展。详情分享如下。

**更新 1(美国东部时间 2019 年 2 月 24 日上午 11 点 28 分)**:一名参与该项目的开发人员在 Twitter 上发布了一段视频，显示任天堂 Switch 号正在启动 AOSP 的新版本。更多细节见下文。

任天堂 Switch 是任天堂最新的游戏机/掌上电脑，它在销售和吸引力方面做得非常好。这也标志着任天堂态度的转变，因为该设备不仅由 Nvidia Tegra 片上系统驱动，而且据报道该公司甚至[希望雇佣](https://www.xda-developers.com/nintendo-approached-cyanogen-to-partner-for-the-switch-cyanogen-refused/)现已解散的 Cyanogen Inc .开发他们的操作系统。自从发现 [Fusée Gelée 漏洞](https://www.xda-developers.com/nvidia-tegra-x1-google-pixel-c-nvidia-shield/)后，Switch modding 在社区中真正流行起来。用户长期以来一直在理论上探讨是否有可能将 Android 移植到交换机上。毕竟，Linux [已经被移植到它](https://github.com/fail0verflow/switch-linux)上，该设备使用 Tegra X1 SoC，有文档可以参考。剩下的就是对移植 Android 足够感兴趣的开发人员的血汗和眼泪。一个名叫[章程](https://gitlab.com/ByLaws/android_device_nintendo_switch)的开发者正在接受将任天堂 Switch 变成安卓平板电脑的挑战。

然而，在我们看到任何远程功能之前，仍然有很大的障碍。开发者[声明](https://www.reddit.com/r/SwitchHaxing/comments/apx8pw/someone_is_working_on_android_no_more_information/egd8z8p/)他们目前正在编写驱动程序以使其工作，因为目前，该软件不会启动超过 Android 标志。即使它进入了可启动阶段，也不能保证它能以任何可预测的方式工作，因为这些都是自制的驱动程序。虽然可能会利用交换机操作系统中的一些驱动程序(或者甚至是 Tegra 芯片组中的 Nvidia Shield)，但不知道它最终会有多稳定。

开发人员试图让 Android 在交换机上运行并不奇怪。任天堂设备对 Linux 内核并不陌生，因为自制软件开发人员总是试图在其上运行某种形式的 Linux。DSLinux 和 Wii-Linux 浮现在脑海中，它们分别将 Linux 带到了任天堂 DS 和任天堂 Wii 上。将 Android 引入像任天堂 Switch 这样的便携式控制台设备将是一个巨大的壮举。虽然在交换机上安装 Android 不会给你带来与直接购买 Android 平板电脑相同的体验，但如果我们可以将我们最喜欢的游戏主机变成一台支持更好多媒体的平板电脑，那么不必携带另一台设备将是有益的。

* * *

## 更新 1:开关启动安卓系统...非常慢

该交换机现在可以启动 AOSP，尽管它在任何可用状态之前还有很长的路要走。开发人员表示，构建目前滞后是因为 GPU 驱动程序不工作，但 Wi-Fi 和蓝牙工作正常。开发商认为规章制度为实现这一目标做了大量的工作。

* * *

## 更新 2:交换机的 Android 端口接近

开发者细则、langer_hans、一些 LineageOS 开发者和其他独立开发者已经联合起来，在任天堂 Switch 上开发一个可用的 Android 版本。他们在过去几周取得的进步令人难以置信。就在过去的 3 天里，开发者修复了 [Wi-Fi](https://www.reddit.com/r/SwitchHacks/comments/bzg32d/so_i_heard_you_guys_wanted_portal_on_the_switch/eqs5lqp/) 、 [touch](https://www.reddit.com/r/SwitchHacks/comments/bzg32d/so_i_heard_you_guys_wanted_portal_on_the_switch/eqsen7e/) 、 [sound](https://www.reddit.com/r/SwitchHacks/comments/bzg32d/so_i_heard_you_guys_wanted_portal_on_the_switch/eqxt127/) 。像[谷歌 Chrome](https://www.reddit.com/r/SwitchHacks/comments/bzg32d/so_i_heard_you_guys_wanted_portal_on_the_switch/eqzp0pt/) 和 [Discord](https://www.reddit.com/r/SwitchHacks/comments/bzg32d/so_i_heard_you_guys_wanted_portal_on_the_switch/eqsf1qk/) 这样的应用程序是有效的。即使是为 NVIDIA SHIELD Android TV 开发的游戏，如 Portal，[也已经被证明可以在 Android 上运行。](https://photos.google.com/share/AF1QipNHx59hsjtPDoZYEYUOJx6w9-w3pVMow5wGeY0-FBKtOCdFBQOnsFvU0N3sNrWAPQ?key=enRsSGNocHprbFItN0t1UndtNFctQU5WcnlJTmpR)

开发人员目前正在努力:修复基于陀螺仪的自动旋转，使控制超频变得容易，获得更好的以控制器为中心的发射器，LP0 睡眠，手持 joycon 支持，USB 硬盘支持，以及安装 TWRP。我们正在密切关注这些进展，一旦有公开版本发布，我们会及时通知您。