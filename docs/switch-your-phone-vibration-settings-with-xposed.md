# 使用 x 曝光功能切换手机振动设置

> 原文：<https://www.xda-developers.com/switch-your-phone-vibration-settings-with-xposed/>

几个月前，[我们推出了一款名为 Vybe 的应用](http://www.xda-developers.com/android/vybe-generates-your-own-customized-vibrations/ "Vybe Generates Your Own Customized Vibrations")。这是一个有趣的应用程序，允许用户轻松自由地定制来电和短信的振动模式，而无需冒险修改系统文件。虽然振动可能不是最重要的个性化功能，但如果你希望有所不同，知道这个选项是很好的。

XDA 资深会员 [itandy](http://forum.xda-developers.com/member.php?u=2536649) 推出了一款名为 Android 手机振动器的 mod，为你的手机振动提供额外的定制选项。这个 mod 以 x 曝光模块的形式出现，所以它必须通过 [rovo89](http://forum.xda-developers.com/member.php?u=4419114) 的[x 曝光框架](http://www.xda-developers.com/android/say-goodbye-to-custom-stock-roms-and-hello-to-xposed-framework/)来激活，这无疑是你们大多数人都熟悉的。快速重启后，您将能够访问并激活一系列振动定制，例如:

1.  当拨出的电话接通时振动
2.  来电接通时振动
3.  来电等待时振动
4.  通话结束时振动
5.  在每分钟的 45 秒标记时，在拨出电话时振动
6.  拨出电话接通后，在固定时间振动一次
7.  调整振动强度

Itandy 还在线程中包含了一个方便的 FAQ，为一些人遇到的问题提供了一个可能的修复方法，以及修复该问题的详细步骤。

如果你想看看这个模型，去[原始线程](http://forum.xda-developers.com/showthread.php?t=2417965)获取更多信息并下载。模块的源代码也可以在其 [Github](https://github.com/itandy/xperia_phone_vibrator) 中找到。