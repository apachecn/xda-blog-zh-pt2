# 如何通过 OnePlus 6 的测试版 Android Pie 版本的 SafetyNet

> 原文：<https://www.xda-developers.com/pass-safetynet-beta-android-pie-oneplus-6/>

如果你愿意切换到该公司最新的开放测试版 OxygenOS，你现在就可以在你的 OnePlus 6 上获得 Android Pie。虽然它配备了 Android Pie 的所有最新功能，如自适应电池和最新的材料设计主题，但它也不是没有问题。其中一个主要问题是不支持 Google Pay。事实上，该设备没有通过安全网证明 API 测试。这不仅意味着你不能使用 Google Pay，而且你将无法登录 Snapchat，玩 Pokemon Go，或者使用几乎任何需要通过 SafetyNet 的应用程序。你甚至不能通过谷歌 Play 商店安装网飞[(尽管侧装 APK 仍然有效)。](https://www.xda-developers.com/netflixs-safetynet-exclusion-is-actually-a-new-feature-in-the-google-play-console/)

不过，有一个办法可以解决这个问题。你不仅可以在 OxygenOS 的最新开放测试版上通过 SafetyNet，而且 Google Pay 也可以完美运行。您可以使用 Magisk，也可以自己修改 build.prop 文件。如果你想通过 Magisk 来实现，那么你需要一个 Magisk 模块，由 XDA 知名贡献者 [Didgeridoohan](https://forum.xda-developers.com/member.php?u=4667597) 制作，它可以让你改变你设备的指纹。

## 如何通过 OnePlus 6 的测试版 Android Pie 版本的 SafetyNet

当您的设备未能通过 ctsProfile 检查，但通过了 basicIntegrity，这很可能是因为您的手机指纹。指纹本质上是您正在使用的 ROM 的唯一标识符，用于检查您正在使用的 Android 版本是否已通过谷歌的兼容性测试套件(CTS)验证。如果指纹与已经通过 CTS 认证的 Android 版本不匹配，那么它将立即无法通过该测试。因此，我们需要修改驻留在 build.prop 文件中的指纹。你可以用两种不同的方法做到这一点。

### 方法 1 -手动修改 build.prop

这是我个人选择的选项，因为它比 Magisk 路线更容易。我们稍后会谈到这一点。你仍然需要你的 OnePlus 6 通过 Magisk 进行根操作，但我们不会使用 Magisk 模块。一旦你有了根，从谷歌 Play 商店下载任何 build.prop 编辑器，或者你可以通过大多数支持根的文本编辑器来完成。

我个人使用这个应用程序来修改我的 build.prop，但是任何应用程序都可以。

一旦安装了可以用来修改 build.prop 的应用程序，请导航到

```
 ro.build.fingerprint 
```

并将值从

```
 ro.build.fingerprint=OnePlus/OnePlus6/OnePlus6:9/PKQ1.180716.001/1808301430:user/release-keys

```

或者无论当前的构建特征是什么，都要:

```
 ro.build.fingerprint=OnePlus/OnePlus6/OnePlus6:8.1.0/OPM1.171019.011/06140300:user/release-keys

```

重启你的设备，你就可以通过安全网了。这样做的缺点是你正在对/system 进行修改，所以更新你的手机或者刷新你的 ROM 将会覆盖这个修改。你在伪造最新稳定版本的指纹，所以对谷歌来说，你的 Android 版本*已经过*CTS 测试。你现在可以在 Android Pie 上使用 Google Pay 了。

### 方法 2 -使用 Magisk 模块

这是我们之前提到的 Magisk 模块，我们目前不推荐它的原因是你必须使用新的 Magisk Canary 版本。Resetprop，用于无系统地修改 build.prop，在 Android Pie 上不起作用，除非你用的是 Magisk 最新的 Canary build。虽然这样做可以让你[玩像堡垒之夜移动或命运/大令](https://www.xda-developers.com/fate-grand-order-fortnite-mobile-magisk/)这样的游戏，但你会受到使用金丝雀版本的其他错误的影响。除非你确切地知道你在做什么，否则使用它并不是一个好主意。如果你愿意继续，那么你可以查看 [XDA 论坛的帖子](https://forum.xda-developers.com/apps/magisk/dev-magisk-canary-channel-bleeding-edge-t3839337)，了解如何在你的 OnePlus 6 上安装 Magisk Canary。

一旦你设置好了，你需要下载并安装“MagiskHide Props Config”模块，它可以在 Magisk 模块报告中找到。一旦你完成了，下载任何终端模拟器并输入“props”。

[app box Google play jackpal . Android term]

*这是我个人使用的安卓终端应用。*

你应该会看到类似下面的截图。

一旦你重新启动，你也应该通过安全网。虽然上述两种方法都有效，但在 Magisk 的测试版发布之前，我个人建议直接修改你的 build.prop。Magisk Canary 可能有许多错误，如果修改你的 build . prop 不会影响 SafetyNet，那就更安全了。