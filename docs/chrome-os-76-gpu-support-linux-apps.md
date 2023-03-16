# Chrome OS 76 添加了一个标志来启用 GPU 对 Linux 应用程序的支持

> 原文：<https://www.xda-developers.com/chrome-os-76-gpu-support-linux-apps/>

自从 Linux 应用程序第一次出现在 Chrome OS 设备上已经有一年多了。从那以后，越来越多的 Chromebooks 开始得到支持，项目也变得更好。但是，有一个特性是用户强烈要求的，那就是图形加速。到目前为止，Linux 应用程序还没有 GPU 支持。Chrome OS 76 的第一个开发版本添加了一个名为“Crostini GPU 支持”的标志，最终实现了爱好者的愿望。

基思·I·迈尔斯最先注意到这个新功能。它在 Chrome OS 76.0.3789.0 中可用，这是 Chrome OS 76 的第一个开发版本。不言而喻，这个特性现在是不稳定的。它还处于非常早期的阶段，所以程序错误和稳定性问题是意料之中的。此外，请记住，只有少数 Chromebooks 支持 GPU 加速:

*   谷歌像素书(eve)
*   Dell Inspiron 14
*   联想 Yoga Chromebook C630
*   宏碁 Chromebook 13
*   宏碁 Chromebook Spin 13
*   惠普 X360 Chromebook 14

如果你拥有其中任何一款，并且准备安装一个非常实验性的 Chrome OS 版本来测试 Crostini GPU 加速，你可以阅读下面的说明。

1.  打开 Chrome 浏览器，导航到[Chrome://flags/# crostini-GPU-support](chrome://flags/#crostini-gpu-support)，启用标志；
2.  浏览器将提示您重新启动设备，单击“立即重新启动”按钮即可；
3.  现在您必须更新容器。打开终端，运行“sudo apt-get update”命令；
4.  现在运行“sudo apt-get dist-upgrade”命令，然后再次重启你的设备；
5.  现在，为了确保安全，再次打开终端并运行“glxinfo -B”。S

如果您在日志中看到“Device: virgl”列，那么您已经成功启用了 GPU 加速。显存一栏对于部分用户输出 0MB，但这似乎不是问题。你可以在下面的视频中看到 GPU 支持显示了多大的改进。请记住，Portal 是一款专门为 Windows 编写的游戏，它运行在 Chrome OS 中的 Linux 容器中，有自定义的 GPU 支持，因此即使是最小的结果也令人惊讶。

Chrome OS 76 稳定版将于 8 月发布。除了 Crostini GPU 加速，它还带来了[虚拟桌面](https://www.xda-developers.com/chrome-os-virtual-desktops-chromebooks/)。也有一些小的变化，如[重排“清除所有”按钮](https://www.xda-developers.com/chrome-os-76-clear-all-notifications-button/)。我们相信，在最终版本发布之前，还会有更多的功能被添加进来，这离最终版本发布还有 3 个多月的时间。

* * *

**来源: [Keith I Myers](https://kmyers.me/blog/chromeos/chromeos-76-0-3789-0-rolling-out-to-the-dev-channel-adds-crostini-gpu-flag/) /来源:[关于 chrome book](https://www.aboutchromebooks.com/news/video-pixel-slate-portal-steam-with-gpu-acceleration-chrome-os-76-chromebook/)**