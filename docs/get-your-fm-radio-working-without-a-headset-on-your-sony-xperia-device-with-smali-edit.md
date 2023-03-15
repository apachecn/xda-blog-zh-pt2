# 使用 Smali Edit 在索尼 Xperia 设备上无需耳机即可收听调频广播

> 原文：<https://www.xda-developers.com/get-your-fm-radio-working-without-a-headset-on-your-sony-xperia-device-with-smali-edit/>

如果你没有不小心扯破或摔坏手机附带的耳机，它很可能已经不可救药地丢失了，再也找不到了。在 Xperia 设备上，这太糟糕了，因为没有它，你将无法赶上你最喜欢的电台名人或收听前 40 名而不通过移动宽带进行流媒体播放。但是，嘿，现在有一种方法可以让索尼 Xperia 用户在不需要耳机的情况下听广播，这要归功于 XDA 公认的贡献者[*DaRk-Lord*](http://forum.xda-developers.com/member.php?u=4872623)写的一篇教程。

很像之前的[特色 smali 编辑教程](http://www.xda-developers.com/android/add-a-quick-launch-panel-to-your-rom-with-a-smali-modification/)，这个教程可以是一个快速简单的修复，任何人都可以遵循和应用，无论是新手还是专业人士。它只需要反编译和编译 apk 的知识，为此有许多教程和工具，当然，还有实际的 *Radio.apk* 文件。反编译完 APK 后，导航并打开 *PhfHandler.smali* 。在那里，进行必要的代码更改，保存文件，编译 APK，并将其推送到您的设备上。这里也有这个过程的截图，供任何想要更多指导的人参考。

如果你渴望收听每日早间广播，但似乎找不到(不再)需要的耳机，请查看位于[原始主题](http://forum.xda-developers.com/showthread.php?t=2640394)的教程开始收听。