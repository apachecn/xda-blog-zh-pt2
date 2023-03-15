# 如何发现隐藏的快速启动命令

> 原文：<https://www.xda-developers.com/how-to-discover-hidden-fastboot-commands/>

在我尽可能多地探索 Android 定制的过程中，我有了许多模糊但有趣的发现。我已经向您展示了如何通过筛选手机上所有隐藏的应用程序活动来访问您设备上的隐藏菜单。最近，我向您展示了如何在某些智能手机上访问[隐藏的硬件诊断工具](http://www.xda-developers.com/how-to-access-hidden-diagnostic-tools-on-your-android-phone/)。现在，我意识到你们中的一些人对你的智能手机没有在之前的文章中提及感到失望，我为此道歉。

为了弥补这一点，我将带您经历一些更高级、更令人兴奋的事情:**转储您设备的引导程序，以发现隐藏的快速启动命令**。这个指南虽然是在我的 [Nexus 6P](http://forum.xda-developers.com/nexus-6p) 上完成的，但也绝对可以在大多数智能手机上复制。但是，您可以访问的命令将因设备而异。大多数命令在任何实际情况下都不会真正帮到你，但是深入了解你的手机设置还是很有意思的。让我们开始吧。

免责声明:只要你知道自己在做什么，并能适当地遵循指示，你的设备就不会出什么问题。但是，我们仍然在摆弄我们的设备分区和引导程序，所以不知道如果你输入错误的命令会发生什么。确保您准备好了设备外备份！

* * *

**准备**

在我们开始之前，有一件非常非常重要的事情需要注意。为了提取您的设备的引导程序，**您将需要在您的手机上的 root 访问权限。**如果您没有 root 访问权限，您可以出于教育目的继续阅读本指南，但您将无法执行任何必要的命令。明白了吗？很好。你需要满足的另一个先决条件是确保你的电脑有所有的**合适的 ADB/fastboot 驱动**。如果你没有 ADB/fastboot 二进制文件，那么我推荐从我们的论坛安装[最小 ADB & Fastboot](http://forum.xda-developers.com/showthread.php?t=2317790) 。至于驱动程序，你可以从这里获取谷歌 Nexus 设备[的必要驱动程序，从这里](https://developer.android.com/studio/run/win-usb.html)[获取所有其他设备的必要驱动程序](https://developer.android.com/studio/run/oem-usb.html)。你怎么知道你是否准备好了？插入您的设备，在开发人员设置下启用 USB 调试，打开命令提示符，并键入:

```
 adb devices 
```

如果你看到你的设备的序列号弹出，那么你有正确的驱动程序。

* * *

**转储引导程序**

我们的第一步是在我们的设备上打开一个外壳，这样我们就可以通过 ADB 运行命令。我们最好在 ADB 上运行命令，因为我们在虚拟键盘上打字时更容易出错，而在这里你不想出错。您应该在命令提示符下运行的第一个命令是:

```
 adb shell 
```

如果您看到命令提示符从显示 ADB 二进制目录变为显示 Android 设备的代码名称，那么您已经成功地进入了设备的本地命令行 shell。现在，为了访问我们需要转储的分区，您需要超级用户权限。为此，请键入以下内容:

```
 su 
```

设备代号前的符号应该从 **$** 变为 **#** ，表示您现在可以使用提升的权限运行命令。现在小心点！

接下来，我们将找出您设备的引导程序映像的确切位置。为了找到确切的目录，我们将按名称打印出所有分区及其目录的列表，并查找一个名为' **aboot '的目录**您需要输入如下两个命令:

```
 cd /dev/block/bootdevice/by-name
ls -all 
```

正如您在上面看到的，打印出了一个巨大的分区目录列表。这些分区是按名称排序的，所以我们可以很容易地辨别出引导程序分区的位置。在我的例子中，bootloader，也就是上图中的**‘aboot’**，可以在/dev/block/mmcblk0p10 中找到。这个**会根据你的设备的不同而变化**，所以重要的是你要按照这些指示来找出你的引导程序所在的真正目录。但是，请注意这个目录，因为我们将在以下命令中引用它来转储引导加载程序:

```
 dd if=/dev/block/{YOUR ABOOT PARTITION} of=/sdcard/aboot.img 
```

一旦成功，您应该会在内部存储的根目录下找到一个名为' **aboot.img** 的文件。现在我们已经转储了引导装载程序，我们需要检查它以确定我们可以找到哪些隐藏的命令。

* * *

**隐藏的快速启动命令及其用途**

您可能熟悉一些更常见的快速启动命令，例如**快速启动闪存**或**快速启动。**在[开源快速启动协议](https://android.googlesource.com/platform/system/core/+/master/fastboot)中定义了更多的快速启动命令。以下是每台安装了基于最新 AOSP 代码的引导加载程序的设备上可用的快速引导命令列表:

这个列表中缺少的是快速启动 **oem** 命令。这些命令对于 Android 设备制造商来说是**特有的**，并且没有任何地方有完整的列表或文档来说明哪些快速启动 oem 命令是可用的。现在，如果你的设备制造商能提供一个列出所有 oem 命令的快速启动命令(试试**快速启动 oem？看看这是否可行)，那么你就不需要再做什么了。如果没有任何命令打印可用的 fastboot oem 命令列表，那么您需要从 aboot.img 打印一个**字符串**列表，并手动搜索 oem 命令。**

“strings”是一个 linux 命令，它的文档可以从这里的获得。如你所知，我个人使用的是 Windows 系统，所以我用的是模仿 Linux 中“字符串”的[程序。aboot.img 文件上的“strings”命令的原始输出将会](https://technet.microsoft.com/en-us/sysinternals/strings.aspx)[非常混乱](https://paste.omnirom.org/view/cd3e07f7)，但是如果你简单地 CTRL+F 为“oem ”,你应该找到你需要的。如果你想细化你的搜索，你可以试试这个命令(对于我链接的 Windows 版本):

```
 strings * | findstr /i oem 
```

对于 Nexus 6P，我编译了以下快速启动 oem 命令列表:

```
 fastboot oem unlock-go
fastboot oem frp-unlock
fastboot oem frp-erase
fastboot oem enable reduced-version
fastboot oem device-info
fastboot oem enable-charger-screen
fastboot oem disable-charger-screen
fastboot oem enable-bp-tools
fastboot oem disable-bp-tools
fastboot oem enable-hw-factory
fastboot oem disable-hw-factory
fastboot oem select-display-panel
fastboot oem off-mode-charge enable
fastboot oem off-mode-charge disable
fastboot oem ramdump enable
fastboot oem ramdump disable
fastboot oem uart enable
fastboot oem uart disable
fastboot oem hwdog certify begin
fastboot oem hwdog certify close
fastboot oem get-imei1
fastboot oem get-meid
fastboot oem get-sn
fastboot oem get-bsn
fastboot oem get_verify_boot_status 
```

**请注意，除非您愿意承担风险，否则不要尝试上述任何命令或您在设备上发现的任何命令。这些命令对用户隐藏是有原因的。**

也就是说，我已经为我发现的一些快速启动命令想到了一些巧妙的用法(这些命令可能会也可能不会出现在你的设备上，所以请按照上面的说明进行检查！)那应该是看中了最铁杆的安卓发烧友。这里有两个命令可能有一些实际用途。

首先是**快速启动 oem(启用|禁用)-充电器-屏幕**命令。这样做的目的是禁用手机关机时弹出的充电屏幕。如果你不喜欢手机关机时充电屏幕的炫目亮度，那么你可以通过这个隐藏的快速启动命令禁用它！

接下来是**快速启动 oem 关闭模式-充电(启用|禁用)**命令。此命令决定当检测到电源时，您的设备是否会自动打开。默认情况下，它被设置为“禁用”我承认这个命令对手机没什么用，但是如果你打算把平板电脑安装到汽车的仪表板上，你会发现这个命令非常有用。您可以将设备设置为在平板电脑通电时立即开机，例如当您的汽车电池启动时。相反，使用 Tasker 等自动化应用程序可以在断电时轻松关闭平板电脑。顺便说一下，这个命令完全按照写在 [Nexus 7 (2013)](http://forum.xda-developers.com/nexus-7-2013) 上的命令工作。

* * *

关于 Android 可定制性的课程到此结束。在下面的评论中分享你发现的命令(最好是在一个 pastebin 链接中)!

*感谢 XDA 资深公认开发者 [Dees_Troy](http://forum.xda-developers.com/member.php?u=912474) 对本文制作的协助！*