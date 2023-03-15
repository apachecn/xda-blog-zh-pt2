# 以下是如何将主屏幕镜像到 Mi 11 Ultra 的后部显示屏

> 原文：<https://www.xda-developers.com/xiaomi-mi-11-ultra-mirror-to-rear-display/>

迄今为止，Mi 11 Ultra 是小米唯一一款在后置摄像头岛上配备辅助显示屏的智能手机。这家中国 OEM 厂商选择了 1.1 英寸的 AMOLED 屏幕，你可以用它来查看时间、电池电量、一些通知，甚至控制你的音乐。本质上，它实际上是在手机背面显示一个 Mi 波段。然而，MIUI 并没有为外部显示提供那么多定制选项。小米甚至不让你在副屏访问所有已安装的应用，这绝对是个败笔。为了解决这一问题，XDA 成员 [GuyWithRootedPhone](https://forum.xda-developers.com/m/guywithrootedphone.8789269/) 开发了**mirror 2 reaultra**——一款基本上将你的 Mi 11 Ultra 主屏幕内容镜像到后显示面板的应用。

这位在 GitHub 上也被称为 *tpkarras* 的开发者发布了 Mirror2RearUltra 应用程序，作为一种独特的解决方案，以充分利用 Mi 11 Ultra 的辅助显示屏。不过，这款应用没有任何花哨的用户界面。所有你得到的是一个新的快速瓷砖安装后。只要你点击名为“镜像到后屏幕”的磁贴，应用程序就会开始将主屏幕内容投射到辅助显示器上。值得注意的是，你可能需要点击后屏幕来唤醒它。

准确地说，这款应用目前只是一个概念验证。这里和那里还需要一些润色。例如，在某些情况下，录制/演职确认屏幕会出现在 Mi 11 Ultra 的背面屏幕上。也有一些关于次要显示屏亮度和旋转的小故障，但开发人员正在解决这些问题。对于阅读本文的任何应用程序开发人员来说，Mirror2RearUltra 是开源的，因此您可以查看代码库，提交新的补丁，或者自己编译应用程序。

**mirror 2 reaultra for the Mi 11 Ultra:[XDA 下载讨论线程](https://forum.xda-developers.com/t/4419811/) || [GitHub Repo](https://github.com/tpkarras/Mirror2RearUltra)**

由于 MIUI 具有非常激进的电池管理设计，它有突然终止后台应用程序的趋势。因此，您可能会发现 Mirror2RearUltra 在一段时间后停止工作。为了让它在后台运行，请确保关闭此应用程序的 MIUI 节电功能。

* * *

请在下面的评论区告诉我们你对 Mirror2RearUltra 的看法。