# TWRP 发布了谷歌像素和像素 XL

> 原文：<https://www.xda-developers.com/twrp-has-been-released-for-the-google-pixel-and-pixel-xl/>

让自定义 ROM 开始刷新！用户来我们论坛的一个最常见的原因是刷新自定义模块、内核或 rom。为了社区的利益，开发人员投入了无数的时间来定制他们的软件。但是如果没有安装这些修改的方法，这些工作都是不可行的。

在你进入 Android 改造世界之前，第一步是解锁你的引导程序。对于 [Pixel](http://forum.xda-developers.com/pixel) 和 [Pixel XL](http://forum.xda-developers.com/pixel-xl) 的用户来说，这一步已经可以在这两款设备的[所有变种](http://forum.xda-developers.com/pixel-xl/development/twrp-alpha1-pixel-devices-t3500312)上实现。下一步是刷新自定义恢复映像，这将允许您刷新自定义 ROM 或内核映像，并允许您在出现任何问题时进行完整的系统备份。这就是非常受欢迎的[团队胜利恢复项目](https://twrp.me/) (TWRP)的用武之地。

几乎每个原始设备制造商的众多设备上都可以使用 TWRP，它已经成为任何想要修改设备上软件的人的首选定制恢复。现在，这两款谷歌 Pixel 手机很快就可以加入这一乐趣了。XDA 资深公认开发者 [Dees_Troy](http://forum.xda-developers.com/member.php?u=912474) 刚刚为谷歌 [Pixel](http://forum.xda-developers.com/pixel/development/twrp-alpha1-pixel-devices-t3500314) 和 [Pixel XL](http://forum.xda-developers.com/pixel-xl/development/twrp-alpha1-pixel-devices-t3500312) 发布了首款**TWRP**T4alpha。假设您已经解锁了引导加载程序，现在您可以将恢复刷新到您的设备上。尽管如此，我们应该注意到 TWRP 的安装方式有一些变化。

* * *

**安装**

如果您曾经手动将 TWRP 安装到您的设备上，那么您可能熟悉将 TWRP 映像刷新到恢复分区所需的 *fastboot* 命令。**由于分区的改变使得“无缝更新”可以在 Android Nougat 的 Pixel 和 Pixel XL 上运行，你将不会发出同样的命令。**忘掉你认为你知道的一切，在行动前仔细阅读以下说明。本质上，你实际上要做的是安装 TWRP 的是**引导**TWRP 镜像，然后使用**自动安装脚本**，它将处理两个引导分区的**TWRP。**

首先，如果你还没有，你需要获取[谷歌 USB 驱动](https://developer.android.com/studio/run/win-usb.html)以及快速启动二进制文件(我们建议下载并解压[最小 ADB &快速启动](http://forum.xda-developers.com/showthread.php?t=2317790)到你选择的目录)。接下来，为你的设备下载合适的 TWRP 安装文件( [Pixel](http://forum.xda-developers.com/pixel/development/twrp-alpha1-pixel-devices-t3500314) 和 [Pixel XL](http://forum.xda-developers.com/pixel-xl/development/twrp-alpha1-pixel-devices-t3500312) )。你需要移动。zip 文件压缩到设备的内部存储中，但保留。img 文件。然后，打开命令提示符，通过在命令提示符下输入*快速启动设备*来检查您的设备是否被识别。如果您看到设备的序列号，则快速启动协议会检测到您的设备。最后，您需要通过发出以下命令来临时启动 TWRP 映像:

```
 fastboot boot path/to/twrp.img 
```

注意“path/to/”指的是下载的 TWRP **镜像**文件所在的实际目录。确保你发出的是***fastboot****boot***和**而不是** fastboot **flash** ，并且你引导的文件是**而不是**zip 文件。发出启动命令后，您的设备将从您的计算机中检索 TWRP 映像，并临时启动到 TWRP。至此，您差不多完成了。

你现在需要做的就是通过将 TWRP 刷新到你设备的两个引导分区来让它在重启后存活下来。幸运的是，所有的工作都由您之前下载的自动安装脚本来处理。只需使用 TWRP 界面导航并安装 TWRP 安装 zip 文件**，就像你安装任何定制的 ROM、mod 或内核 zip 文件**一样。此后，无论使用哪个活动分区插槽，您都可以访问 TWRP。

* * *

**TWRP 阿尔法 v1**

因为这是一个 **alpha** 版本，所以肯定会有问题。现在，迪斯·特洛伊概述了**需要注意的三个问题**。首先，由于 Nougat 引入了基于文件的加密(FBE ),数据恢复可能会造成问题。

> #### 基于文件的加密(FBE)可能比较棘手。如果恢复工作不正常，它会触发数据的自动擦除。我在我的 Pixel XL 上进行了一点测试，但还没有时间进行广泛的测试。有时，TWRP 将无法提示您输入密码，或者无法正确设置解密。如果发生这种情况，重新启动 TWRP。这似乎是某种时间问题，我还没有时间去追踪它。

没人说这可能会发生在你身上，但它可能会发生在你身上。如果你不经常离线或在云上备份你的数据，那么当出现问题并且你的全部数据被删除时，不要感到震惊。我以前也遇到过这种事，很糟糕。

更新#2: Dees_Troy 对可能出现的问题提供了更技术性的解释，以及他计划如何解决这个问题。更多细节见文末第二个补遗。

接下来，如果您当前正在您的设备上使用多用户功能(包括访客功能)，那么您将需要**暂时避免使用 TWRP**。

> #### 基于文件的加密意味着每个用户的文件夹都单独加密。为了进行正确的备份、工厂重置等，我们必须让用户解密设备上的每个帐户。

目前，TWRP 仅支持单用户设置，即使您碰巧知道设备上其他用户的加密密码。Dees_Troy 告诉我们，他已经使用命令行工具成功地解密了更多的用户，但在 TWRP 实现这一功能现在不是一个高优先级，而是可能会在未来的更新中发布。上周，我们的 XDA Twitter 账户代表 Dees_Troy 对用户进行了调查，询问他们是否使用多用户功能，绝大多数人表示他们不使用多用户功能，因此我们不认为这一限制会影响很多人。

但是还有一个问题与大多数将要安装 TWRP 的用户更相关。目前, **SuperSU 将不会与 TWRP 并肩作战。**

> #### 如果您目前是根用户，此时安装 TWRP 将删除根用户。需要升级超级苏才能让 TWRP 和超级苏共存。

更新#1:如果你目前正在使用 SuperSU，并计划使用闪光 TWRP，请参见 Chainfire 在文章末尾的附录。 Dees_Troy 向 XDA 开发商解释了这种干扰的原因:

> #### Chainfire 使用 bootimage 的 ramdisk 来做他的无系统根。这是谷歌打算用于恢复的同一个内存盘。我很确定 Chainfire 能够想出一个办法让它和 TWRP 一起工作，但是 TWRP 需要对 init 二进制文件做一个小的改动来让 decrypt 正常工作，Chainfire 需要对他的 init 二进制文件做一个不同的改动来让他的 ramdisk 正常启动和恢复。

换句话说，Chainfire 的无系统根方法修改了 TWRP 需要修改的同一个二进制文件，以便让数据解密工作。因此，当您刷新 TWRP 时，您正在覆盖由 Chainfire 的无系统根方法对 init 二进制文件所做的更改。虽然这是一个小挫折，但由于 Pixel 的双分区性质(以及未来的牛轧糖设备)，TWRP 有一些漂亮的新功能。

> #### 像素设备有 2 个 ROMs 固件“插槽”。TWRP 将检测当前活动的插槽，并使用该插槽进行备份和还原。在“重新启动”页面和“备份->选项”下有按钮来更改插槽。更改活动插槽将导致 TWRP 切换 TWRP 正在备份或还原的插槽。您可以备份插槽 A，切换到 B，然后恢复备份，这样会将 A 的备份恢复到插槽 B。在 TWRP 更改插槽也会告诉引导加载程序引导该插槽。

这实质上意味着你很快就能在你的设备上双启动。不幸的是，由于定制恢复刚刚*发布*，你最喜欢的定制 ROM 开发者需要一些时间在厨房里为你的 Pixel 手机做些什么。

* * *

**附录 1 -与 TWRP 一起的 SuperSU】**

我们被 Chainfire 告知，任何目前在谷歌 Pixel 或 Pixel XL 上使用 SuperSU 的人**强烈建议**在安装 TWRP 之前，将普通启动映像刷新到两个分区。为了做到这一点，您需要为您的设备下载[工厂镜像](https://developers.google.com/android/images)，并手动从档案中提取股票启动镜像。然后，您需要使用 fastboot 将引导映像刷新到两个分区，如下所示:

```
 fastboot flash boot_a boot.img
fastboot flash boot_b boot.img 
```

发出这两个命令会将出厂映像中的普通启动映像刷新到设备上的两个启动分区中。然后，您可以继续安装 TWRP。

* * *

**附录 2 -基于文件的 TWRP 加密**

在与 Dees_Troy 的交谈中，他就恢复何时可能出错并导致全部数据擦除给出了以下解释:

> #### 基于 ext4 文件的加密不允许你对一个*非*空的文件夹应用加密策略。目前，我们正在通过不删除选定的文件夹列表来解决这个问题(我们可以删除文件夹中的内容，但不能删除文件夹本身)。如果出于某种原因，需要加密的文件夹被删除，恢复可能会创建一个未加密的文件夹，然后用一些东西填充它。一旦文件夹为非空，就不能对其设置加密。当设备再次启动 Android 时，init 二进制文件会尝试设置加密策略，如果在设置策略时发现错误，它会强制执行擦除操作。[这正是](https://android.googlesource.com/platform/system/core/+/android-7.1.0_r7/init/builtins.cpp#341)抛出错误和开始擦除的地方，如果你关心这类事情的话。

用不太专业的术语来说，在还原 NANDroid 备份的过程中，恢复需要覆盖备份中保存的分区中所有必要的现有文件。为了访问数据分区中的文件，恢复需要使用您的解密密码解密该分区。虽然恢复能够简单地删除和覆盖数据和系统分区中的每个文件夹，但这样做可能会导致加密策略出错。

通过删除一个本应加密的文件夹，TWRP 将在其位置创建一个未加密的文件夹，并从这个新目录中的备份恢复所有文件。但是，由于基于文件的加密将使用不同的加密密钥对不同的文件和文件夹进行加密，而不是对整个分区进行加密，因此对设备上单个文件夹的这种单个更改破坏加密将导致整个链抛出错误。Android 的政策是随后启动一次全面的数据擦除，导致 Android 擦除你内部存储中的所有数据。

幸运的是，Dees_Troy 已经**确定了需要从 TWRP 的删除过程中排除的文件夹列表**，这样就不会触发这个错误。他替换了 init 二进制文件，这样它会在恢复过程中触发错误，但不会擦除设备，从而允许他准确记录哪些文件夹不能删除。我们收到了一份完整的文件夹列表，但由于篇幅原因，我们在此不再赘述。

* * *

[**谷歌像素**下载 TWRP ](http://forum.xda-developers.com/pixel/development/twrp-alpha1-pixel-devices-t3500314)

[**谷歌像素 XL** 下载 TWRP ](http://forum.xda-developers.com/pixel-xl/development/twrp-alpha1-pixel-devices-t3500312)

你打算在你的设备上运行定制的 ROM 或内核，还是继续使用现有的固件？请在下面的评论中告诉我们！