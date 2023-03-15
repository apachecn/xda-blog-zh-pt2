# 谷歌 Pixel 和 Pixel XL 现在可以使用 Root 了:以下是我们的发现

> 原文：<https://www.xda-developers.com/root-is-now-available-for-the-google-pixel-and-pixel-xl/>

这种方法已经过时，可能行不通。请访问我们的 Google Pixel 和 Pixel XL 论坛，了解最新的根方法。

正如承诺的那样，谷歌 Pixel T1 和 T2 Pixel XL T3 的无系统根在 T4 已经上市 T5。XDA 资深公认开发人员 [Chainfire](http://forum.xda-developers.com/member.php?u=631273) [在过去几天里正在为运行 Android 7.1 牛轧糖的谷歌 Pixel](http://www.xda-developers.com/chainfires-systemless-root-for-pixel-phones-is-coming/) 手机开发 root，他已经达到了一个开发阶段，现在他已经可以轻松地与社区分享他的工作了。

通过安装 SuperSU **2.78 SR2** 、可以获得 Google Pixel 和 Google Pixel XL 的 Root 访问权限，这使得 *su* 可以在不接触系统分区的情况下访问，并允许切换 dm-verity。在你启动你的设备之前，你首先需要解锁你的引导程序。解锁引导程序的第一步是下载 adb 和 fastboot 二进制文件(我们建议从我们的论坛下载[最小 ADB & Fastboot](http://forum.xda-developers.com/showthread.php?t=2317790) )，然后为您的机器安装合适的 [Google USB 驱动程序](http://forum.xda-developers.com/showthread.php?t=2317790)。

如果你直接从谷歌购买了你的 Pixel 设备，那么你只需要发出一个*快速启动闪烁解锁*命令，然后是*快速启动 oem 解锁。*如果你从威瑞森或 EE 购买了你的 Pixel，你需要[通过 dePixel8 工具](http://www.xda-developers.com/verizon-pixelpixel-xl-bootloader-unlock-has-been-released/)解锁你的引导程序。但是快点，因为阳光开发者已经提到他们的引导装载解锁漏洞可能会在即将到来的 11 月安全更新中被修补！

* * *

**如何在你的 Pixel 上安装 SuperSU**

正如 Chainfire 在他的 Google+帖子中提到的，你需要首先从他的网站上下载 Pixel 或 Pixel XL 的**引导到根**图像。你可以[点击这里](https://download.chainfire.eu/1007/CF-Root/CF-Auto-Root/root-sailfish-pixel.zip)下载谷歌 Pixel 的 zip 文件，或者[点击这里](https://download.chainfire.eu/1008/CF-Root/CF-Auto-Root/root-marlin-pixelxl.zip)下载谷歌 Pixel XL 的 zip 文件。下载 zip 文件后，需要**快速启动**引导**到根**镜像，**不要** **快速启动闪存镜像！**换句话说，这两个设备需要的唯一命令如下:

```
 fastboot boot boot-to-root.img 
```

等待几分钟，在几次重启后，你将会以完全 root 权限启动。耶！

* * *

**根访问的直接使用**

顺便说一下，除了 root 访问应该带来的通常功能之外，我们还测试了一些我们知道你们都会感兴趣的东西。首先，你能让 Google Now 恢复运行吗？答案是**是的！**你所需要做的就是编辑 **build.prop** 做如下修改，重启，然后清除谷歌应用数据，你就不会再看到谷歌助手了。

变化

```
 ro.opa.eligible_device=true 
```

到

```
 ro.opa.eligible_device=<strong>false</strong> 
```

另一个常见的隐藏功能是什么:**双击唤醒？**我们四处寻找隐藏的开关，并发现了它。

```
 sailfish:/sys/devices  
```

不幸的是，当我们改变这个值时，它似乎并不坚持。现在，似乎你必须刷新一个定制的内核，比如 [ElementalX](http://forum.xda-developers.com/pixel-xl/development/kernel-elementalx-pxl-0-02-t3487072) 来让 d2tw 工作。

我们测试的其他一些东西包括 Titanium Backup 是否工作(**它工作**)，更好的电池状态(**工作**)，底层/层主题(**似乎有一些问题**，以及广告拦截(**失败**)。Ad-away 目前无法工作，因为默认情况下/system 不能以读写方式安装，所以我们必须等到 TWRP 可用后，才能为 Ad-Away 刷新[无系统解决方案](http://forum.xda-developers.com/showthread.php?t=2190753)。是的，我们已经尝试使用 [FlashFire](https://play.google.com/store/apps/details?id=eu.chainfire.flash&hl=en) 来刷新无系统根的 Ad-Away 启用程序，但这似乎在此时也不起作用。

```
 sailfish:/sys/devices 
mount: '/system' not in /proc/mounts 
```

更新:Chainfire 已经确认 FlashFire 和其他应用程序需要更新才能使用。更多详情见下文。

更新 2: Chainfire 给我们发了一条消息，告诉我们在应用程序更新之前，AdAway 可以正常工作。见文末补遗。

这里有一些截图显示钛备份工程，虽然。因此，如果您来自另一台设备，并且想要恢复所有备份的应用程序，您可以放心，所有应用程序数据现在都将被恢复。

我们将继续深入我们的像素设备，看看我们可以切换什么。哪个“像素专属”功能会是下一个倒下的？

* * *

**实现根**的“奋斗”

在发行说明方面，Chainfire 相当细致。当你是一个为成千上万的用户提供实现根访问的方法的开发者时，尽可能透明是有意义的，以免你面对一大群困惑的用户，他们想知道为什么某些东西坏了。虽然他的 [Twitter 账户](https://twitter.com/ChainfireXDA) (@ChainfireXDA)更多地用于发布简短的公告，但 Chainfire 往往会在他的 [Google+](https://plus.google.com/+Chainfire) 账户上发布非常受欢迎的冗长解释。[这次也不例外](https://plus.google.com/+Chainfire/posts/fvEPo42GKXS)。

首先，Chainfire 解释了他需要解决的两个 Pixel 手机的变化，以实现 root 访问。具体来说，Chainfire 首先描述了像素设备上的新分区布局。

> #### *新的分区布局(Pixel 和可能的许多未来设备):*
> 
> -有几个 Android 分区中的两个，引导、系统、供应商
> 
> -恢复和缓存分区消失了
> 
> Android 的根目录/目录现在是系统分区的一部分，而不是引导分区(initramfs)
> 
> - Recovery 现在位于正常的引导映像中，并使用它的 initramfs(以前由 Android 使用)

正如我们之前所报道的，两个 Pixel 手机上的这些[分区变化](http://www.xda-developers.com/exclusive-dual-boot-may-be-possible-on-pixel-phones/)将[需要对当前的根方法](http://www.xda-developers.com/pixel-phones-not-yet-rootable-with-current-methods/)进行一些修改。Chainfire 已经证实，对/system 分区的这些修改需要一种不同的方法，一种可能涉及修改内核的方法。

> #### 使用 Pixel 的新分区布局，我们正在更改的那些文件已经移动到系统分区(我们最初认为的/system 现在是该分区的文件系统中的一个子文件夹)。那么，我们可以只修改包含所有这些文件的系统分区，而不修改引导映像吗？虽然我个人更喜欢修改启动映像，不去管系统，但反过来也可能是一个解决方案，我知道一些技术用户甚至更喜欢这样。
> 
> #### 然而，我不能让这个工作。引导装载程序实际上向内核(驻留在引导映像中)发送强制启用 dm-verity(强制系统分区的完整性)的信息，如果不( *drum roll* )修改引导映像，我们就无法拦截或更改这些信息。我的第一个成功的像素根就是这样完成的——通过修改两者(早先发布的图片就是这次尝试的结果)。

换句话说，正如我们所怀疑的，如果不对内核进行一些修改，就无法禁用 dm-verity。因为内核是强制启用 dm-verity 的，所以 Chainfire 需要稍微修改内核，以阻止 dm-verity 阻止对系统分区的更改。幸运的是，Chainfire 发现他的修改只需要一个小的内核二进制补丁，而不需要完整的内核重新编译。因此，他的解决方案应该仍然是具有 A/B 分区方案的 Android 7.1 设备的通用解决方案。

为了更详细地解释这种新的 root 方法，Chainfire 通过让内核使用引导映像的 initramfs 作为其根目录，而不是系统分区中的任何内容，来实现无系统 root。为此，系统分区中的根目录内容被导入到引导映像中，这样就可以修改这些文件，而不必修改任何系统文件。系统分区挂载到/system_root，而/system 本身通过 sim 链接到/system_root/system。最后，他的内核补丁修改了内核，使得它忽略了从通常会强制 dm-verity 的引导装载程序发送的命令。

然而，这种新方法带来了一些相当小的问题。某些应用程序，如 FlashFire 或 AdAway(我们已经展示了这两个都不工作)希望系统分区被挂载为/system，而不是/system_root，并且需要相应地更新。但是，您可以尝试像这样重新安装系统

```
 mount -o rw,remount /system_root 
```

这应该允许您写入/system。我们还没有测试修复了哪些根应用，但是你可以自己测试。最后，Chainfire 不确定 suhide 是否会使用这个新的生根方案，但他表示他将继续寻找一个变通办法。

* * *

要为谷歌 Pixel 手机下载 SuperSU，请前往 [XDA 论坛主题](http://forum.xda-developers.com/apps/supersu/2014-09-02-supersu-v2-05-t2868133)。非常感谢 Chainfire 将 root 带到了设备上！让游戏开始吧！

[**参观 SuperSU XDA 分论坛！**](http://forum.xda-developers.com/apps/supersu)

这个故事还在发展中，我们会根据新的信息进行更新。在这篇文章的制作过程中，谷歌牺牲了一个像素。窃取杰夫的数据。

* * *

**附录# 1:AdAway 的临时修复**

从我们的[论坛](http://forum.xda-developers.com/showthread.php?t=2190753)下载 AdAway v3.1.2，然后使用[终端仿真器](https://play.google.com/store/apps/details?id=jackpal.androidterm&hl=en)或 ADB shell 输入以下命令:

```
 mkdir /su/etc; cp /system/etc/hosts /su/etc/hosts; echo "#!/su/bin/sush\nmount -o bind /su/etc/hosts /system/etc/hosts" > /su/su.d/50adaway; chmod 0700 /su/su.d/50adaway 
```

重新启动，你应该有系统范围的广告拦截。