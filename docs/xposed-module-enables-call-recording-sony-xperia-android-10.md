# 通过这个曝光的模块在索尼 Xperia 手机上录制通话

> 原文：<https://www.xda-developers.com/xposed-module-enables-call-recording-sony-xperia-android-10/>

谷歌手机应用程序最近获得了期待已久的[通话记录功能](https://www.xda-developers.com/google-phone-app-rolls-out-call-recording-nokia-phone-users-india/)，尽管由于相关法律，该公司可能已经针对特定国家和/或地区推出了该功能。虽然有可能[在非 Pixel(或非 Android One)手机上安装](https://www.xda-developers.com/google-phone-non-pixel-play-store-download/)谷歌制造的拨号器应用程序，并祈祷呼叫记录功能被激活，但如果将此选项作为股票拨号器的一部分，会方便得多。XDA 公认的开发者 [serajr](https://forum.xda-developers.com/member.php?u=3989065) 也会对索尼 Xperia 社区有同样的想法，因为他提出了一个 Xposed 模块，可以在任何运行 Android 10 的索尼手机上进行通话记录。

**[x 曝光框架 XDA 论坛](https://forum.xda-developers.com/xposed)**

几款[老款](https://www.xda-developers.com/sony-xperia-1-xperia-5-receive-official-android-10-update/) Xperia [手机](https://www.xda-developers.com/sony-xperia-xz3-xz2-xz2-compact-xz2-premium-receive-official-android-10-update/)至今已经通过 OTA 收到了 Android 10 的味道，并且都兼容这个 mod。然而，安装部分有点棘手，因为用户需要首先刷新 Magisk 的最新版本，然后是 [EdXposed 框架](https://edxp.meowcat.org/)。一旦 EDX exposed 启动并运行，您可以从 serajr 创建的讨论线程下载该模块的 APK，通过 EdXposed Manager 安装并激活它。重新启动是必要的，以使更改生效，你应该得到一个专用的“录音呼叫”的拨号器用户界面上的选项。

该模块与股票拨号器应用程序的“设置>通话”部分无缝集成。用户可以选择 AMR 和 MP3 作为录音格式，他们甚至可以打开来电和/或去电的自动录音。最后，有一个主开关来切换整个呼叫记录功能，这对于诊断模块中的意外错误特别有用。

该模块的 UI 不支持多语言(仅支持英语)，这是一个已知的限制。在写这篇文章的时候，这个模块只有编译后的版本，但是开发者已经承诺“很快”会分享源代码。

**[索尼 Xperia 通话录音曝光模块— XDA 下载讨论线程](https://forum.xda-developers.com/crossdevice-dev/sony/xposed-stock-call-recording-q-v1-0-0-t4088727)**