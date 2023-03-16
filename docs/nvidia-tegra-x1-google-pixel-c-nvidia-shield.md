# 发现 Tegra X1 漏洞，影响谷歌 Pixel C 和 Nvidia Shield

> 原文：<https://www.xda-developers.com/nvidia-tegra-x1-google-pixel-c-nvidia-shield/>

如果你是一个游戏玩家，你可能已经听说了昨天关于任天堂 Switch 令人难以置信的消息:它已经被完全破解了。在 [Nvidia Tegra X1](https://www.xda-developers.com/nvidia-announces-the-powerful-tegra-x1-soc/) 中发现了一个新的漏洞，这是一种在任天堂 Switch 发现的片上系统，但也有像 [Google Pixel C](https://forum.xda-developers.com/pixel-c) 和 [Nvidia Shield Android TV](https://www.xda-developers.com/nvidia-shield-the-tegra-x1-powered-android-tv-box/) 这样的设备。这个名为 [Fusée Gelée](https://github.com/reswitched/fusee-launcher/blob/master/report/fusee_gelee.md) 的漏洞是由 [Katherine Temkin](https://twitter.com/ktemkin) 与致力于打开自制软件访问开关的黑客团队 [ReSwitched](https://reswitched.tech/) 合作发现的。在他们的工作过程中，他们发现了一个漏洞，该漏洞实现了他们正在寻找的东西，但由于其平台特异性，影响的设备可能比他们预期的更多。

我不会假装能够完全详细地描述该漏洞，但基本的解释是，在 T186/X2 之前发布的 Nvidia Tegra SoCs 容易受到通过 USB 软件堆栈进行的攻击，该软件堆栈允许在设备上执行任意代码。特别是，该漏洞利用发送专门构建的 USB 复制操作(其长度由攻击者控制)来获得对“启动和电源管理处理器”的控制，然后以可能的最高权限将任意代码加载到主应用程序处理器上。

由于错误存在于引导 ROM 中，因此在工厂没有硬件修订版的情况下，无法对其进行修补。这意味着所有带有上述 Tegra 片上系统的设备都容易受到攻击，没有任何软件更新能够修补它。幸运的是，它需要物理访问设备才能利用，所以只要攻击者无法亲自访问，您的设备就是安全的。撇开安全问题不谈，这一发现让游戏社区议论纷纷，因为它对任天堂 Switch 家酿啤酒(老实说，对盗版)的影响。)但由于我们不是一个游戏论坛，让我们来讨论一下这一发现的其他含义。

* * *

## Android on Switch？屏蔽设备的定制引导加载器？fuseégelée 对我们意味着什么。

由于该漏洞原本打算在 2018 年 6 月 15 日披露，因此开发该漏洞的开发团队没有太多时间来完全投入使用。我们预计在未来几天和几周内会有一些修改。作为一个玩笑，在[fail 0 overflow](https://fail0verflow.com/blog/2018/shofel2/)的家伙已经测试了在任天堂 Switch 上运行 GNU/Linux 发行版，如下所示。

将来，甚至有可能让 Android 在任天堂 Switch 上运行。如果有足够多的开发人员关注它，我们可以在上面运行 [LineageOS 15.1](https://www.xda-developers.com/lineageos-15-android-oreo-officially-announced/) (而且 Switch 肯定有专门的用户群)。现在说肯定还为时过早，但鉴于 SoC 已经用于真正流行和有据可查的 Android 设备(Pixel C 和 Nvidia Shield)，我猜测这很可能会发生。

至于现有的搭载 Tegra X1 SoC 的 Android 设备，有很多值得期待的地方。当然，像 Pixel C 和 Shield 这样的设备已经有了一个蓬勃发展的开发者社区，但这种利用提供的设备访问级别将是前所未有的。据 LineageOS 开发人员和 XDA 资深成员 [npjohnson](https://forum.xda-developers.com/member.php?u=5848265) 称，开发人员可以开始构建一个定制的引导加载程序，如基于 UEFI 的引导加载程序(甚至像 [EFIDroid](https://www.xda-developers.com/efidroid-is-a-second-stage-bootloader/) 用于原生多重引导)，修改可信执行环境(TEE)以允许 [Widevine L1](https://www.xda-developers.com/android-netflix-hd-amazon-prime-video-hd-drm/) 或 OMX 在不支持它的设备上安全解码，烧断保险丝然后读取它们，伪造锁定状态，等等。

这个严重的 Tegra X1 漏洞有很多可供开发人员利用，所以我们必须等待，看看人们能够编造出什么。尽管如此，漏洞就是漏洞，所以如果你担心有人可能会利用它来窃取你的数据，最好是更换设备，因为这个问题没有解决办法。