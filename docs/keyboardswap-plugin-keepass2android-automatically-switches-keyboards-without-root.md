# KeyboardSwap 插件切换 keepass 2 没有根的 Android 键盘

> 原文：<https://www.xda-developers.com/keyboardswap-plugin-keepass2android-automatically-switches-keyboards-without-root/>

Android 上的密码管理器长期以来一直被谷歌忽视，但这将随着 Android O 的出现而改变。Android O 的[自动填充框架](https://developer.android.com/preview/features/autofill.html)将[极大地改善用户/密码数据输入](https://www.xda-developers.com/agilebits-shows-off-what-android-os-autofill-framework-will-look-like/)，还将消除对[性能昂贵的可访问性服务](https://www.xda-developers.com/android-os-autofill-framework-will-finally-resolve-a-long-standing-lag-issue-with-password-managers/)的需求，但不幸的是，大多数设备将接受 Android O 还需要相当长的时间。对于我们这些将等待数月 Android O 可用于我们的设备的人来说，标准的密码管理器功能已经足够了。XDA 开发团队中个人最喜欢的一个是 [Keepass2Android](https://play.google.com/store/apps/details?id=keepass2android.keepass2android) ，它是流行的开源 [Keepass](http://keepass.info/) 密码管理器的 Android 移植。Keepass2Android 允许您从您选择的云存储中访问您的密码数据库，它还具有指纹数据库解锁和/或通过完整密码的简写快速访问数据库的功能。但是有一个很棒的功能已经被锁定了很多年，只能由根用户使用:自动切换键盘/输入法。一个名为 KeyboardSwap 的新 Keepass2Android 插件旨在解决这一问题。

Android 中的许多密码管理器都提供了自己的键盘(在 Android 中也称为输入法)，因为 Android 系统剪贴板是出了名的不安全。任何请求读取剪贴板权限的应用程序都会自动被授予该权限，无需用户输入，除非您熟悉 App Ops 命令行，否则您也不能轻易撤销该权限。Keepass2Android 也没有什么不同，它的键盘虽然不美观，但却完成了任务。然而，在许多 Android 设备上，不进入设置，就没有快速简单的方法来改变输入法。OEM 和定制 rom 的一些软件在通知面板或导航栏中提供了输入法切换器，但许多没有。这也是 Keepass2Android 的自动键盘切换功能如此有用的原因。

在我们关于 Keepass2Android 的 XDA 聚焦文章的评论中，我们的一位用户指出，Keepass2Android 仍然依赖过时的[安全设置](https://play.google.com/store/apps/details?id=com.intangibleobject.securesettings.plugin)应用程序来自动切换输入法。既然我们现在知道安全设置的大多数功能都可以在没有 root 访问权限的情况下复制，我认为 Keepass2Android 可以用另一个应用程序替换安全设置。我给 Keepass2Android 的开发者 Philipp Crocoll 发了一封电子邮件，里面有一个我想到的非 root 解决方案，这个解决方案就是 KeyboardSwap 插件。

它的工作方式很简单。应用程序使用 [WRITE_SECURE_SETTINGS](https://developer.android.com/reference/android/Manifest.permission.html#WRITE_SECURE_SETTINGS) 权限，该权限通常受到用户应用程序的限制，但可以通过 Android 调试工具(ADB)中的包管理器命令行界面手动授予。你所要做的就是[从谷歌 Play 商店](https://play.google.com/store/apps/details?id=keepass2android.plugin.keyboardswap2)安装插件，确保你使用的是 Keepass2Android 的测试版，然后在设置好 ADB 后，在命令提示符/终端中输入以下命令:

```
 adb shell pm grant keepass2android.plugin.keyboardswap2 android.permission.WRITE_SECURE_SETTINGS 
```

该插件然后可以将 Keepass2Android 输入法服务的名称写入 [`Settings.Secure.DEFAULT_INPUT_METHOD`](https://developer.android.com/reference/android/provider/Settings.Secure.html#DEFAULT_INPUT_METHOD) 设置，Android 将在下次需要键盘输入时自动打开该键盘。当然，这项服务实际上必须在 Keepass2Android 中启用，方法是进入设置- >应用程序设置- >密码输入访问- >键盘切换，然后切换“自动切换键盘”功能。

例如，如果你当前的默认键盘是 [Gboard](https://play.google.com/store/apps/details?id=com.google.android.inputmethod.latin) ，那么 KeyboardSwap 插件会将`com.google.android.inputmethod.latin/com.android.inputmethod.latin.LatinIME`保存为当前键盘，然后一旦你在应用程序中选择了密码条目，就将 DEFAULT_INPUT_METHOD 更改为`keepass2android.keepass2android/keepass2android.softkeyboard.KP2AKeyboard`。当关闭 Keepass2Android 输入法时，那么 KeyboardSwap 插件会将 Gboard 输入法服务恢复到 DEFAULT_INPUT_METHOD 设置。

对最终用户来说，一旦许可被授予，插件就“正常工作”一旦插件安装好了，你就不用担心任何与插件相关的事情了。您可以将应用程序图标从应用程序抽屉中隐藏起来，并且永远不再触摸它。如果您在工厂重置或卸载，然后重新安装应用程序，只有到那时，您将不得不再次授予许可。否则，这是一个简单的插件，你可以设置和忘记，它会让你的密码输入快一点点。