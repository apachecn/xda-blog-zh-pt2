# 通过重新签署 APK 永久停止任何 Android 应用程序的更新

> 原文：<https://www.xda-developers.com/stop-updates-android-application/>

有很多应用程序存在，有些人觉得被更新毁了。一些变化包括与应用程序捆绑的广告软件，或者应用程序基本上变成了一个恶意软件。曾经被誉为轻量级应用、UI 辉煌的应用 quick pic[被猎豹移动](https://www.xda-developers.com/xda-external-link/quickpic-now-owned-by-maker-of-clean-master/)收购，慢慢开始包含其他应用的广告。如果能够停止更新，回到人人喜爱的应用程序，这个在广告被推送给用户之前就存在的应用程序，岂不是很好？

嗯，有一种方法可以通过 XDA 实验室、XDA 应用和游戏论坛以及 APKMirror 等其他网站来实现。以 QuickPic 为例，猎豹移动更改之前的最后一次更新是 4.5.2 更新。如果我们把这个 APK 安装到我们的设备上，我们*可以*禁用谷歌 Play 商店中的自动更新，但是如果你在点击更新你设备上所有其他应用程序时不小心更新了它，该怎么办？然后你必须卸载应用程序，然后重新安装旧版本，或者恢复备份——这两者都很麻烦。但是如果我们可以永久停止一个应用程序的更新会怎么样呢？

* * *

## 如何重新签名您的 APK 文件以停止更新

本教程需要一点设置，但是一旦完成，你将拥有所有你需要的未来文件，这将会快很多。对于这个教程，你需要 Java 和一个在你的电脑上打开 APK 文件的方法。任何标准的 zip 查看器都应该工作正常。你还需要 [**安卓工作室**](https://developer.android.com/studio/index.html) 。**本指南不需要 root，只需要在安全设置中启用“允许未知来源”即可。对于本教程，我将使用 QuickPic v4.5.2。它将适用于任何 APK，但是。**

### 第一步

导航到 Android Studio 文件夹，找到 keytool 应用程序。对于我来说，这个在 C:\ Program Files \ Android \ Android Studio \ JRE \ bin。以管理员身份打开命令窗口，导航到该文件夹。您现在需要利用 keytool 来生成一个密钥库，以便对您的 APK 进行重新签名。接下来，在命令窗口中键入以下内容。

```
 keytool -genkey -v -keystore C:\my-release-key.keystore -alias alias_name -keyalg RSA -keysize 2048 -validity 10000 
```

用您选择的名称替换“my-release-key ”,用您选择的名称替换“alias_name”。系统将提示您输入用户名和密码。输入这些，你就可以走了。保持文件夹和命令窗口打开。

### 第二步

将您想要签名的应用程序复制到您找到 keytool 的文件夹中。

### 第三步

使用任何 zip 查看器打开您选择的 APK 作为存档。我推荐 7Zip。删除 APK 中的“META-INF”文件夹，然后继续。META-INF 包含密钥签名文件。为了方便使用，也可以将 APK 复制到包含 jarsigner 的文件夹中。Jarsigner 用于重新签署您的 APK。

### 第四步

在命令窗口的文件夹内，键入以下命令来重新签名您的 APK。

```
 jarsigner -verbose -sigalg SHA1withRSA -digestalg SHA1 -keystore C:\my-release-key.keystore
my_application.apk alias_name 
```

用所需信息替换“我的发布密钥”、“我的应用程序”和“别名”。您将被要求输入密钥库密码。一旦进入，你会看到文件已经签署。

### 第五步

把文件复制到你的手机上，然后试试吧！它应该可以很好地安装，如果你试图通过 Play Store 更新它，你会发现它不能。

正如你在上面看到的，我们的修改成功了！

* * *

## 说明

Android 有一个 APK 签名形式的安全系统，这意味着你设备上的应用程序都必须有一个仅由开发者持有的特殊密钥，才能接受同一应用程序的更新。这意味着如果有人修改你的 APK 并试图欺骗用户认为这是一个新的更新，一个简单的密钥验证可以显示这不是一个合法的更新，然后 Android 实际上完全阻止了更新。这是一个安全功能，我们可以用它来停止任何我们选择的 Android 应用程序的更新，永远停止！

仅此而已！希望这个教程对一些用户有所帮助。