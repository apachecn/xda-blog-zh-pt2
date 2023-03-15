# 如何在任何手机上启用 Google 相册无限存储

> 原文：<https://www.xda-developers.com/enable-google-photos-unlimited-storage/>

CST 时间 09:40 更新:经过进一步测试，这个技巧似乎仍然会导致上传的照片不符合您的 Google Drive 存储限制。换句话说，行不通。然而，这一招仍然可以让你的手机获得像素专属壁纸！原文如下。

在众多功能中，谷歌 Pixel 系列最伟大、最有用的独有功能之一是谷歌照片的无限存储。该功能允许您将您现有的所有图片和视频以**原始质量**备份到 Google 相册，而无需将它们计入您现有的 Google Drive 存储中。不过，该功能仅限于 Pixel、Pixel XL、Pixel 2、Pixel 2 XL 和 Moto X4 Android One edition。不过，如果你是**的粉丝**，XDA 成员[发现了一个小小的变通办法，可以让你在任何运行 Android Nougat 或更高版本的 Android 手机上，获得 Google Photos 无限存储空间以及**Google Wallpapers 应用**上的专属壁纸类别。](https://forum.xda-developers.com/member.php?u=6995375)

* * *

## 在任何 Android 手机上启用无限制的 Google 相册存储和像素专属壁纸

以防我们之前没有说清楚，**你需要 root 访问权限**才能继续学习教程，所以在继续之前，请确保你的手机已经正确 root。然后，按照以下步骤操作:

1.  将 [nexus.xml](https://www.androidfilehost.com/?fid=673791459329053057) 下载到您的手机。
2.  打开您选择的根文件管理器(我们在这里使用了 Solid Explorer，但是您几乎可以在这里使用任何根文件管理器，比如 [MiXplorer](https://forum.xda-developers.com/showthread.php?t=1523691)
3.  复制刚刚下载的 nexus.xml 文件，粘贴到/system/etc/sysconfig 中。
4.  然后，将文件权限设置为 644 (rw-r - r -)。
5.  重启你的手机。
6.  启动后，进入谷歌照片的设置页面，清除谷歌照片的应用数据。你完了！

照片现在会认为你正在使用 Pixel，因此，你应该会看到一个对话框，告诉你现在可以在谷歌 Pixel 设备上使用无限存储空间。此外，**你现在应该可以访问谷歌壁纸应用程序上的更多壁纸类别，以及 Urbane 类别上的默认 Pixel 2 壁纸。**

### 可选版本。必要时进行适当编辑

对于大多数设备来说，只需将文件放在 sysconfig 目录中就足够了。然而，如果放置上述文件对你不起作用，你将不得不把你的手弄得更脏。下载 BuildProp 编辑器，然后查找并更改/设置以下 build.prop 值:

```
 ro.product.model=Pixel 2 XL 
```

```
 ro.product.brand=Google 
```

```
 ro.product.manufacturer=Google 
```

```
 ro.opa.eligible_device=true 
```

### 更新 1 -魔术模块

这里有一个由 XDA 资深会员 [dariomrk](https://forum.xda-developers.com/member.php?u=7692227) 制作的 [Magisk 模块](https://forum.xda-developers.com/apps/magisk/google-photos-unlimited-hi-res-upload-t3688114)，以防你想无系统地进行这些更改(从而通过安全网)。

### 更新 2 -进一步测试

Redditor /u/stek29 已经[对这个技巧](https://www.reddit.com/r/oneplus/comments/762v8v/roothow_to_enable_google_photos_unlimited_storage/dob3l6x/)进行了更多的测试，并发现您可能不需要擦除 Google Photos 中的数据，该文件不需要命名为 nexus.xml，并且唯一被检查的标志显然是 NEXUS_PRELOAD。

### 更新 3 -上传可能仍然会影响驱动器存储

我们听说这个技巧是由 OpenGapps 的团队在几个月前发现的，并且已经被 Google 悄悄地修补了。在这种情况下，应用这个技巧仍然会导致上传的照片应用到您的 Google Drive 存储(即没用)。我们自己还没有证实，但是如果我们证实了，我们会更新上面的教程。

### 更新 4 -谷歌照片无限存储不起作用，像素壁纸仍然有效

我已经确认，使用这种技巧上传的“原始质量”的照片仍然会计入您的驱动器存储空间。我的硬盘显示我昨天上传了 0.2GBs 的照片和视频。这意味着这个技巧被修补了，很可能是在 OpenGapps 的人发现它的时候。奇怪的是，这个技巧不知何故仍然会触发 Google 相册向您显示原始质量的入职信息。

* * *

### 说明

一些 Pixel 专有服务和功能(如无限制的 Google Photos 存储)的资格是在 nexus.xml 文件中定义的，默认情况下包括在 system/etc/sysconfig 目录下的所有 Google Pixel 手机中，而不是通常(并且可以在其他设备上轻松复制)的简单 build.prop 标志。系统分区在没有 root 用户的情况下是可读的，这意味着所有应用程序都可以很容易地检查系统分区中的值。一些谷歌应用程序，如谷歌照片和谷歌壁纸，会检查 nexus.xml 文件中的特定标志，以便为 Pixel 用户提供特定功能。然而，只要你的手机有这个特定的文件，这些应用程序就会认为用户正在使用谷歌像素，因此会在你的手机上启用这些独家功能。所以只需使用根访问和根文件管理器将它插入系统分区就可以了。

到目前为止，我们已经在一台运行非官方 Android 8.0 Oreo ROM 的 Moto G 2015 上进行了测试，我们可以确认它可以工作。然而，它肯定能在大多数 Android 牛轧糖设备上工作。虽然我们不能保证它在 Marshmallow 或更低版本上工作，但这是可能的，因为该应用程序似乎只检查 nexus.xml 文件中的特定标志，而不是系统相关的值。

谷歌极有可能在短期内修补这个问题——毕竟，[这不是我们第一次发现我们不应该发现的快捷方式](https://www.xda-developers.com/enable-google-lens-in-google-assistant-right-now/)。所以，我们鼓励你测试一下，并在评论区给我们反馈。并且一定要检查[的原始教程](https://forum.xda-developers.com/redmi-note-3/how-to/google-exclusive-wallpapers-guide-how-t3687906)，最初是为小米红米 Note 3 制作的，如果这对你有用的话！