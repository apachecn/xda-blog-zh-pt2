# 用 XThemeEngine 主题化所有的手机

> 原文：<https://www.xda-developers.com/theme-all-the-rooted-phones-with-xthemeengine/>

你可能还记得，也可能不记得去年的某个时候，一个名叫 XDA 的成员向这个世界介绍了一个全新的概念，名为 Xposed Framework。这基本上使用户能够破解任何 ROM 和改变几乎任何东西，而无需编码，用厨房破解 ROM，甚至通过恢复闪烁 zip。这种工具的可能性几乎是无限的，而且几乎没有风险。有些人在这里或那里发布了一些东西，但正如大多数新奇的概念一样，东西需要时间才能在人们的脑海中站稳脚跟。好消息是，越来越多的人开始看到这个框架的神奇之处，并开始使用它来添加功能，否则将需要一个全新的 ROM(因为您想要的可能在您最喜欢的 ROM 中找不到)。XDA 论坛成员 [ruqqq](http://forum.xda-developers.com/member.php?u=1274109) 就是其中之一，他基于 Xposed 发布了一些相当有趣的东西。

XThemeEngine 类似于 CyanogenMod 及其衍生产品中的 TMobile 主题引擎。本质上，选择一个主题，下载它，并通过引擎应用它。没有闪烁，也没有混乱。唯一不同的是，CM 引擎仅适用于 AOSP rom(有一些类似于 VR 主题引擎的引擎，但这一个完全建立在 Xposed 平台上)。dev 声明，如果满足两个条件，这将起作用:设备需要被根化，并且需要安装 Xposed framework。它已经在多种设备上进行了测试，没有出现任何问题。dev 还声明，从头开始创建新主题是可能的(事实上非常简单)(也提供了模板)，因此您可以尽情发挥您的想象力。如果你的想象力有点枯竭，你想使用一个现有的主题，移植也可以通过以下几个步骤轻松完成。

请乘坐它转一圈，与世界其他地方分享你的创作。请记住，这仍然是在测试阶段，因此，有一些错误。所以，请阅读整个开放职位的所有细节。

> XThemeEngine 允许您像 T-Mobile/CM10 主题引擎一样为您的设备添加主题。安装主题 apk，从 XThemeEngine 应用程序激活主题。瞧啊。

你可以在[原始线程](http://forum.xda-developers.com/showthread.php?t=2240180)中找到更多信息，你可以在[这个线程](http://forum.xda-developers.com/showthread.php?t=1574401)中阅读更多关于 Xposed 框架的信息。

想在门户网站上发表什么吗？联系任何新闻记者。