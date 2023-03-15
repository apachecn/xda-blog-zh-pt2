# Play Protect 警告 OxygenOS 5.0.1 上的 OnePlus 3/3T 用户卸载“FactoryMode”

> 原文：<https://www.xda-developers.com/oneplus-3-oxygenos-501-play-protect-factory-mode/>

OnePlus 3 & 3T 的 Android Oreo 更新于上个月以 OxygenOS 5.0 的形式开始推出[。今天，该公司宣布](https://www.xda-developers.com/oxygenos-5-android-oreo-released-oneplus-3-oneplus-3t/) [OxygenOS 5.0.1](https://www.xda-developers.com/oxygenos-oneplus-3-aptx-hd-december/) 的广泛上市，它增加了对高通 aptX HD 蓝牙音频编解码器的支持，一种新的自适应屏幕校准模式，12 月的安全补丁等等。自从更新开始推出以来，许多用户都收到了来自 Google Play Protect 的消息，告诉他们卸载一个名为“**工厂模式**”的“有害应用”

[一加论坛上](https://forums.oneplus.net/threads/google-play-protect-factory-mode-harmful.735406/) [和](https://forums.oneplus.net/threads/factorymode.735361/) [Reddit](https://www.reddit.com/r/oneplus/comments/7n7hct/anyone_getting_a_disable_harmful_app_factorymode/) 上来自用户[的大量](https://forums.oneplus.net/threads/new-bug-is-it-real-oos-5-0-1.735795/)报道显示，这条信息似乎被广泛传播。该消息称 FactoryMode 应用“**包含试图绕过 Android 安全保护**的代码。这是一个相当模糊的信息，但听起来却非常令人担忧。这是怎么回事？

 <picture>![OnePlus 3 FactoryMode Play Protect OxygenOS 5.0.1](img/be69b67e506917bd046301f7cbc58c42.png)</picture> 

Play Protect Warning Users to Uninstall FactoryMode. Credits: [/u/speedlever](https://www.reddit.com/r/oneplus/comments/7n7hct/anyone_getting_a_disable_harmful_app_factorymode/drzsxub/)

显然，FactoryMode 应用程序取代了以前被称为 EngineerMode 的应用程序，这是一个预装的系统应用程序，可以被物理访问设备的用户利用来获得 root 访问权限。一加[最终移除了负责这个根方法的代码](https://www.xda-developers.com/qualcomm-denies-involvement-root-backdoor-oneplus/)，他们也选择移除 EngineerMode 并将其更名为 FactoryMode。

不管出于什么原因，Google Play Protect 已经确定 FactoryMode 应用程序中仍有一些代码可能对安全有害。Google Play Protect 的工作原理是扫描应用程序的代码，并寻找与已知的有害代码集相匹配的指纹。它并不完美，但数据库一直在增长，用户完全无法访问，以隐藏谷歌能够检测到的内容。

因此，Play Protect 不会指定应用程序中的哪些代码被视为有害。由于与更改 SELinux 状态相关的功能，Viper4Android 等应用程序过去曾触发过此消息。有可能 FactoryMode 应用包含类似的东西。请记住，FactoryMode 应用程序是一个预装的系统应用程序，因此它已经拥有比标准 Android 应用程序更多的权限。

现在，你可以忽略 Play Protect 卸载 FactoryMode 的请求，因为这里不太可能有任何对用户有害的东西。然而，这仍然让我们质疑*为什么* Play Protect 首先将 FactoryMode 标记为有害应用，我们希望一加在不久的将来会对此事有一个答案。我们已经联系了一加进行评论，当我们收到回复时会更新这篇文章。

* * *

## 卸载 FactoryMode

如果你仍然想卸载该应用程序，那么你可以输入以下 ADB 命令(摘自我们关于[卸载系统膨胀软件](https://www.xda-developers.com/uninstall-carrier-oem-bloatware-without-root-access/)的指南)来摆脱它:

```
 adb shell pm uninstall -k --user 0 com.oneplus.factorymode

adb shell pm uninstall -k --user 0 com.oneplus.factorymode.specialtest 
```