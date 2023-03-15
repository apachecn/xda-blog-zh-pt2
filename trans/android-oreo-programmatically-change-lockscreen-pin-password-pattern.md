# Android Oreo 增加了以编程方式改变锁屏 Pin、密码或模式的命令

> 原文：<https://www.xda-developers.com/android-oreo-programmatically-change-lockscreen-pin-password-pattern/>

从外观上看，Android Oreo 拥有许多秘密改进。[主题支持](https://www.xda-developers.com/android-oreo-command-line-themes/)，[安卓电视通知禁用](https://www.xda-developers.com/android-oreo-android-tv-notification/)，[减少解锁延迟](https://www.xda-developers.com/android-oreo-lock-screen-latency/)等等。所有这些都在奥利奥的承诺历史中。在官方变更日志中没有发现，但是我们发现了更多。一个这样的发现是以编程方式改变锁屏 pin、密码或模式的命令。乍一看，这似乎没什么用，但是这个命令有一些有趣的应用，在向您展示如何使用它之后，我们将在下面概述这些应用。

**警告**:如果你不小心的话，**可能会把你自己锁在你的设备之外**。你已经被警告了。这只是为了展示谷歌添加的新命令，也是为了从理论上展示你能用它做什么。**如果你承担不起丢失数据的后果**，或者你没有根，就不要乱来。如果您意外地将自己锁定在设备之外并拥有 root 权限，请删除/data/system 中的以下文件:gatekeeper.pattern.key、gatekeeper.password.key 以及任何其他 gatekeeper 文件。

* * *

## 以编程方式更改锁屏 Pin、密码或模式

Android Oreo 增加了一些新的调试命令来改变各种锁屏方式。在[提交](https://android.googlesource.com/platform/frameworks/base/+/android-8.0.0_r1/cmds/locksettings/src/com/android/commands/locksettings/LockSettingsCmd.java)之后，命令如下所示。注意你需要首先使用 **adb shell** ，因为这些需要通过设备的 shell 来执行。这些命令用于设置锁屏的模式、pin 或密码，但是如你所见，如果你需要也可以清除这些。

```
 locksettings set-pattern 
locksettings set-pin
locksettings set-password
locksettings clear 
```

这些命令的作用相当明显。模式有一点不同，但足够简单易懂。例如，对于右图所示的模式，您使用的命令如下。

 `锁紧装置设置-模式 159

模式是通过给每个单元格分配一个数字来设置的，所以左上角是“1”，中间是“5”，右下角是“9”。这就是我们如何达到 159 -你只需将每个图案点的位置映射成一个数字，就像它是一个 T9 拨号器。

重要的是，您使用这些方法设置的任何 pin、密码或模式也会更新加密密码，就像您从设置中设置它一样。有一种方法可以设置一个与锁屏不同的[加密密码，但是不推荐，除非你知道你在做什么。](https://www.xda-developers.com/how-to-manually-change-your-android-encryption-password/)

## TimePIN 的回归？

在运行 Android Oreo 的根设备上，一个潜在的有趣用例是重新创建一个类似于 [TimePIN](https://forum.xda-developers.com/showthread.php?t=2640494) 的应用程序。TimePIN 所做的是动态地将锁屏的 PIN 号更改为当前时间，尽管你可以通过反转数字、偏移数字等方式来混淆它。让它更加安全。例如，在时间 11:56，pin 将是 1156。如果偏移量为-1003，则实际引脚应为 0153。

随着 Android Marshmallow 的发布，当设备管理员应用程序不再能在设备上更改密码时，这种能力被打破了。但是多亏了这些新命令，应该可以在根设备上复制这个功能。

我们基于这一概念创建了一个概念验证 Tasker 配置文件！**我们强烈建议不要使用它，**,因为它很快就被组装在一起，不能保证它能完美地工作。如果您真的想要类似 TimePIN 的功能，请不要使用它。如果你是一个正在阅读这篇文章的开发者，并且认为你可以用它来制作一个应用程序，请成为我们的客人！

你可以从这里下载 [Tasker 项目。通过首先在 Tasker 的首选项中禁用初学者模式来导入它，然后在主屏幕中长按左下方的主页图标来调出导入选项。找到并导入. prj.xml 文件。要设置它，您需要执行两个步骤:](https://www.androidfilehost.com/?fid=673368273298981036)

1.  转到 Tasker 中的 var 选项卡，将您当前的 pin 设置为%OldPIN
2.  打开“设备关闭”配置文件的任务。在“运行 Shell”操作中，在命令末尾添加所需的备份 pin。此外，请确保%OldPIN 和您的备份 PIN 之间有一个空格。您的命令应该如下所示:lock settings set pin-old % old pin 3523

现在启用两个配置文件。

请记住，目前更改 pin 码也将更新加密 pin 码，所以如果你不小心，你可能会意外地无法解密手机中的数据。我们想重申，以上是我们提出的概念证明，希望更有能力的开发人员可以正确地研究这个问题。

* * *

## 总结

总的来说，这是一个有趣的发展，可能对那些想在手机上创建动态 pin 的人有用，或者甚至对那些需要保存手机的人有用，如果调试在计算机上被打开并被允许的话。上面的 Tasker 配置文件只是通过 Android shell 调用 adb 命令，因此可以像 adb 命令一样更改 PIN。`