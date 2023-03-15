# 使用 Xposed 禁用 Android 充电唤醒

> 原文：<https://www.xda-developers.com/no-wake-on-charge-xposed-module/>

# 使用无唤醒充电模块，摆脱充电烦恼

这个 Xposed 框架模块允许你禁用 Android 充电唤醒和一些其他充电烦恼。

几乎每一个原始设备制造商都根据自己的特殊需求对 Android 进行了改造。HTC 和索尼等公司已经改变了默认的 Android 用户界面，添加了声音，并修改了大量的内置功能，以适应他们自己的理念和商业协议。一些添加的功能非常烦人，同样难以禁用。但是用常规设置菜单做不到的事情，一般都可以用 Xposed Framework 来完成。

这些小烦恼之一是安卓充电唤醒。当你将手机连接到充电器上时，屏幕会在没有特别好的理由的情况下被唤醒。更糟糕的是，一些原始设备制造商甚至会在出现这种情况时添加特定的声音。不幸的是，没有简单的方法在某些固件上禁用这种行为。为了解决这个问题，XDA 的资深会员 [moneytoo](http://forum.xda-developers.com/member.php?u=426237) 创建了一个 x 曝光模块，可以消除所有这些小烦恼。该模块禁止在充电和拔出充电器时唤醒，也禁止充电声音。

该模块最初是为三星 Galaxy S5 设计的，但它可以在几种设备上工作。就我个人而言，我在 Nexus 4 上进行了测试，效果非常好。也许确定它是否有效的最好方法是把它安装在你的设备上，然后自己去看。在使用这个模块之前，请确保您已经安装并运行了 Xposed Framework。

你可以通过访问[无唤醒充电线程](http://forum.xda-developers.com/xposed/modules/mod-wake-charge-v0-1-t2826406)来摆脱这些小的充电烦恼。