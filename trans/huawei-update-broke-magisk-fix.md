# 华为推出了一个破坏 Magisk 的更新，但它可以很容易地修复

> 原文：<https://www.xda-developers.com/huawei-update-broke-magisk-fix/>

尽管最近在美国和澳大利亚遇到了麻烦，华为继续在世界各地发展业务。该公司迅速成长为主导中国市场，现在挑战苹果和三星等公司。他们的华为 P20 旗舰产品阵容是他们成功的证明，评论家们对它的相机、制造质量和功能大加赞赏，他们肯定会凭借[华为 Mate 20](https://www.xda-developers.com/huawei-mate-20-notch-render-specifications/) 再次掀起波澜。该公司的子品牌 Honor 提供像 [Honor Play](https://www.xda-developers.com/hands-on-with-the-honor-play/) 和 [Honor 10](https://www.xda-developers.com/honor-10-mini-review-two-months-later/) 这样的设备，在中档市场竞争。正是因为这样的智能手机，XDA 的许多人都是华为和 Honor devices 的粉丝，但正如你们许多人所知，华为决定[停止提供 bootloader 解锁代码](https://www.xda-developers.com/huawei-honor-request-bootloader-unlock-code/)，这是一个令人惊讶的反消费者举措，实际上阻止了他们手机的大多数开发和修改。

[我们之前已经在门户网站](https://www.xda-developers.com/xda-huawei-decision-stop-bootloader-unlocking/)上解决了这个问题，我们仍然对这个决定感到非常失望。让华为这样的巨头改变他们的决定，或者至少拿出一个妥协方案并不容易，虽然[在这方面已经取得了一些进展](https://forum.xda-developers.com/honor-view-10/development/honor-bootloader-unlocking-limited-t3837880)，但对于热衷者来说，形势仍然严峻。最近的一次更新让人们对该公司失去了更多的信心，因为这次更新导致基于 Magisk 的**手机不再启动，除非股票 ramdisk 映像被重新刷新**。因此，不仅华为和 Honor 设备所有者无法解锁他们的 bootloaders，那些已经解锁的设备也无法对其设备进行 root。许多人抨击该公司似乎是(又一个)反狂热分子的举动，但对更新的调查显示，软砖是更新的副作用，并不是故意阻止 Magisk/root。这是我们所知道的关于这次更新的一切。

* * *

## 华为的“Patch01”更新阻止了基于 Magisk 的手机启动

这个问题首先由 XDA 资深成员 [Tecalote](https://forum.xda-developers.com/member.php?u=6870018) 在 Magisk Beta XDA 论坛的官方帖子上[曝光](https://forum.xda-developers.com/apps/magisk/beta-magisk-v13-0-0980cb6-t3618589/post77415750#post77415750)，然后[进一步详述](https://forum.xda-developers.com/showpost.php?p=77418253&postcount=6557)。该成员在他的华为 P9 上偶然发现了这个问题，此前他对他的设备进行了重新命名，以便他可以安装官方的 Android Oreo 更新，然后安装了一个小的“修复错误”的 OTA 更新。更新本身被称为“补丁 01”，包括对彩信和游戏的修复，但它也包括一个内核补丁，可以软砖 Magisk 根源的设备。

据他说，在进行更新之前，他刷新了原始启动映像、原始恢复，并卸载了 Magisk Manager，此时手机成功启动。然而，更新后重新刷新 Magisk 导致手机卡在“你的设备不可信”的闪屏中。更新后的固件只使用原来的 b528 内存磁盘映像启动。无论是否禁用 dm-verity、强制加密或 Android 验证启动，此行为都会持续存在，Magisk v16.0 和 v16.7 都已经过测试。(只是刷新 TWRP 并不是问题，因为恢复会被刷新到它自己的分区 recovery_ramdisk，但是之后尝试 root 手机会触发 bootloop。)

到目前为止，已经有几个用户确认了这种行为。这似乎也不仅限于华为 P9，因为华为 Mate 10 论坛上的[用户也在安装“patch 01”OTA 更新后确认了同样的行为，这让我们认为该补丁将推广到所有目前支持的华为/Honor 手机。鉴于华为最近关于引导加载程序解锁的行动，不难看出为什么人们认为这次更新是为了故意阻止根。Magisk 背后的主要开发者 XDA 认可的开发者/认可的贡献者](https://forum.xda-developers.com/showpost.php?p=77405758&postcount=256) [topjohnwu](https://forum.xda-developers.com/member.php?u=4470081) ，最初在他的 Twitter 账户上承认了这个问题。

Tecalote 本人以及几名华为用户和开发人员在过去几天里承担了彻底调查该问题的任务[，并设法找到了解决方案](https://forum.xda-developers.com/showpost.php?p=77560239&postcount=27389)。

### 为什么要这样做？

最初的证据(以及高度仓促的猜测、谣言和文章/讨论)让用户相信，推出这一更新的唯一目的是将根用户锁定在设备之外。毕竟，华为最近对 bootloader 解锁采取了敌对的态度。这也不是手机制造商第一次追求 root 手机:去年，我们报道 LG 包含了一个 [root checker 工具](https://www.xda-developers.com/lg-root-checker-tool-slow-performance/)，当它检测到 root 时会失控。当然，我们也有许多[制造商和运营商阻止 bootloader 解锁](https://www.xda-developers.com/august-security-update-on-nokia-phones-blocks-the-only-bootloader-unlock-method/)以防止用户干扰他们的手机的案例，最近我们也包括华为。

然而，XDA 资深会员 Tecalote 和其他用户的进一步研究显示，这不一定是华为打击根用户的案例。相反，更有可能的是，我们正在处理一个内核补丁的意外副作用，导致 Magisk 补丁的 ramdisk 映像不兼容，并阻止手机启动。此外，用户可以很容易地解决这个问题，让 Magisk 在打补丁的手机上正常工作。

归根结底，我们无法确定这是否是故意的，因为华为的确切意图不得而知。我们看不到这个更新存在的正当理由，如果确实是故意阻止根用户的话，因为受影响的用户已经经历了重重困难来解锁他们的引导程序。但是考虑到最近的研究和围绕这个主题的背景，以及在更新后你仍然可以安装 Magisk 的事实，我们认为这根本不是故意的。

### 我该如何解决这个问题？

如果你已经更新了你的设备，并想在上面安装 Magisk，你需要在安装前启用“保留 AVB 2.0/dm-verity”标志，正如 Tecalote 在我们的论坛上透露的那样。您不能简单地在 TWRP 上刷新最新的 Magisk zip，因为上述标志不会在安装时自动设置，但是您可以使用 Magisk Manager 手动修补启动映像:

1.  从官方线程下载最新的 Magisk 管理器 APK，安装在您的设备上并打开应用程序。
2.  确保“**保留 AVB 2.0/dm-verity** ”复选框已启用，如果已禁用，则将其启用。如果您的设备已加密，还要确保启用了“保留强制加密”。
3.  点击安装按钮，选择“**补丁启动镜像文件**”选项。这将在应用程序中创建一个 Magisk 补丁的启动映像。
4.  将生成的引导映像闪存到您的设备。你可以在快速启动模式下安装它，方法是将文件移动到你电脑的快速启动目录，重启你的手机到快速启动模式并使用“`fastboot flash boot boot.img`”命令，或者直接用 TWRP 刷新它，点击“安装镜像”按钮并刷新新打好补丁的 boot.img
5.  重新启动系统并再次打开 Magisk Manager 应用程序。如果弹出窗口询问您是否要继续 Magisk 的附加设置，请点击是。
6.  尽情享受吧！

如果你已经根深蒂固，不想采取更新，你仍然可以走老派的方式禁用 OTA 管理器:

1.  从谷歌 Play 商店或 XDA 实验室下载 Solid Explorer、MiXplorer、FX File Explorer 或任何其他支持 root 的文件浏览器。
2.  打开应用程序，接受条款和条件，授予其权限，并授予其 root 访问权限。
3.  转到您的存储根目录，然后转到/system/app/HwOUC。
4.  将 HwOUC.apk 重命名为 HwOUC.bak。
5.  重新启动，你应该准备好了。

[appbox xda com.mixplorer]

如果你由于[项目的三重支持](https://www.xda-developers.com/android-pie-gsi-project-treble/)而运行[自定义 ROM](https://www.xda-developers.com/android-pie-android-9-port-custom-roms/) ，那么你应该是安全的，因为这个功能应该只影响华为自己的 EMUI 软件。

如果你已经更新了“Patch01”更新，如果你想从“patch 01”更新回滚，我们非常不鼓励这样做:一些更新可能有不同的 XLoader(如华为 Mate 10 的一些更新)，如果你刷新了不兼容的 XLoader ，你就有**永久阻止你的设备的风险。此外，Magisk 的解决方法已经找到。降级不适合胆小的人，所以如果你真的想这么做并承认风险，我们建议你搜索我们的论坛，为你的设备寻找一个可行的降级方法。**

* * *

## 底线

阻止引导加载程序解锁和禁止 root 访问的政策是我们可以接受的，即使我们不同意这些政策。但是主动阻止已经解锁了 bootloaders 的 rooted 用户，并故意用更新来屏蔽他们的手机？这没有什么好的理由，而且至少在我们看来，这太没有必要了，特别是考虑到根用户在华为庞大的全球用户群中所占的比例微不足道。我们理解为什么用户会认为华为在屏蔽 root，但我们真的不认为这是事实。

寻根不应被视为类似于盗版、黑客或任何网络犯罪。一部有根的 Android 智能手机相当于一台有管理权限的 Windows 电脑...或者拥有超级用户权限的 Linux PC。那些选择根化他们的设备的人充分意识到根化所涉及的安全风险，并且只是在寻找方法来在他们花了很多钱拥有的设备上获得额外的功能。

虽然我们不认为这是一个有意的改变，但我们确实联系了华为进行澄清，如果我们收到回复，我们将相应地更新这篇文章。如果你真的对 root/使用 rom 感兴趣，购买华为/Honor 设备仍然不是最明智的选择:正如我们之前提到的，他们仍然不提供 bootloader 解锁代码。但与此同时，如果你已经更新了，只需按照上述步骤重新获得根。