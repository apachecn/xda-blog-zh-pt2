# 如何在不更改锁屏密码的情况下更改您的 Android 加密密码

> 原文：<https://www.xda-developers.com/how-to-manually-change-your-android-encryption-password/>

随着越来越多的用户在技术领域寻求更好地保护他们的私人数据，谷歌继续为他们更注重隐私的消费者在 Android 中引入更多功能。

值得注意的是，谷歌在 Android Lollipop 中引入了全磁盘加密(FDE ),并要求任何装有 Android Marshmallow 的设备都必须激活 FDE。但是，尽管有这些改进，有一个问题多年来一直被许多安全爱好者嘲笑:无法使用安全的加密密码。

好吧，我可能有点夸张了。这并不是说你*不能*设置一个真正安全的加密密码，但是由于你的[加密密码(部分)与你的锁屏密码](https://source.android.com/security/encryption/#changing_the_password)捆绑在一起，所以每次你想使用手机时，你都不得不输入一个非常难的密码。对于真正的安全爱好者来说，这将被视为必须做出的牺牲，但对于不太投入的人来说，这种巨大的不便是不可取的。那么，用你的指纹怎么样？我们只能说，一些对不让政府看到他们的私人数据感兴趣的人可能[不太重视生物认证](http://www.wired.com/2013/09/the-unexpected-result-of-fingerprint-authentication-that-you-cant-take-the-fifth/)，至少目前是这样。

那么，确切地说，我们应该如何将我们的加密密码与我们的(通常)短锁屏密码(因此，容易受到暴力攻击)分离呢？某些定制的 rom，如专注于安全的 [Copperhead OS](https://copperhead.co/android/) 允许你设置单独的加密和锁屏密码，但那些没有 Copperhead OS 支持的设备的用户怎么办？

* * *

**与密码器接口**

幸运的是，我们可以使用 Android 内部使用的相同命令来更改您的加密密码。这些命令在 [cryptfs.c 文件](https://android.googlesource.com/platform/system/vold/+/master/cryptfs.c)中定义，该文件包含在 AOSP 使用的[加密文件系统实现。](http://www.am-utils.org/docs/cryptfs/cryptfs.html)

***免责声明:如果您选择使用下面描述的方法来更改您的加密密码，您需要自担风险。某些供应商(如 LG)或定制 rom(如 CM13)稍微修改了使用 cryptfs 所需的语法，因此您需要调整并使用正确的语法。更多详情[此处](https://github.com/nelenkov/cryptfs-password-manager)。忘记密码意味着如果重新启动，您将被完全锁定在设备之外。***

如果您在您的设备上有 root 访问权限，或者至少有一种方法可以临时获得 root 访问权限，那么您将需要在 [shell 终端模拟器](https://play.google.com/store/apps/details?id=jackpal.androidterm&hl=en)中输入以下命令之一。

如果您使用的是 5.0 Lollipop 之前的 Android 版本，请输入以下命令:

`vdc cryptfs changepw <yournewpass>`

对于 Android 5 上的用户。x 棒棒糖:

`vdc cryptfs changepw password <yournewpass in hexadecimal>`

对于 Android 6 上的用户。x 棉花糖:

`vdc cryptfs changepw password <yournewpass>`

您可以通过输入以下命令来验证您的新密码(或检查您的旧密码):

`vdc cryptfs verifypw <yourpass>`

如果您在终端输出中看到一个代码“200 ”,那么您就正确地输入了当前设置的加密密码。注意:如果您目前使用模式锁作为密码，那么当您在此处输入密码时，您需要将每个模式点转换为一个数字(将点模式视为 T9 拨号器，因此左上角的点对应于 1，右下角的点对应于 9)。

如果你更希望有一个图形界面来更改你的加密密码，你可以在 Play Store 上使用这个[应用。担心此应用程序的任何潜在安全问题？没问题，因为它是开源的，你可以通过](https://play.google.com/store/apps/details?id=org.nick.cryptfs.passwdmanager)[使用应用描述中链接的源代码](https://github.com/nelenkov/cryptfs-password-manager)自己编译应用。

* * *

*对于 Android 每一次迭代背后的加密进化，你可以阅读这篇[精彩的文章](https://nelenkov.blogspot.com/2014/10/revisiting-android-disk-encryption.html)。*