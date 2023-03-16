# Android 中的动态系统更新问:Project Treble 将如何改进未来的 Android 版本

> 原文：<https://www.xda-developers.com/android-q-dynamic-system-updates-project-treble/>

随着 Android 8.0 Oreo 的发布，谷歌公布了三重项目(Project Treble)T1:Android OS 框架和厂商 HALs 和 Linux 内核通信方式的重大重组。Treble 是一项旨在减少 Android 平台版本和[安全补丁碎片](https://www.xda-developers.com/linux-kernel-long-term-support-google/)的重大举措，所有使用 Android Pie 发布的 Android 品牌设备都需要支持 Treble 项目。原始设备制造商和供应商通过启动通用系统映像(GSI)——AOSP Android 的纯库存版本——并通过[供应商测试套件](https://source.android.com/compatibility/vts) (VTS)和通用系统映像兼容性测试套件(CTS-on-GSI)，来测试三重兼容性。事实证明，GSI 不仅允许为原始设备制造商工作的软件工程师测试三重兼容性，还为 XDA 的大型定制 ROM 社区打开了大门。对于 Android Q 版本，谷歌希望让 GSIs 对另一个群体有用:应用开发者。

由于任何给定的 Android 平台版本的第一个稳定版本和源代码发布通常在 8 月到来[，如果开发人员希望在真实设备上测试下一个 Android 版本，他们通常需要使用谷歌智能手机，如果他们不想等待更新到达他们自己的硬件的话。然而，谷歌去年与原始设备制造商合作，为几款设备推出了](https://www.xda-developers.com/android-pie-source-code-aosp/)[安卓 P beta](https://www.xda-developers.com/android-p-beta-program-is-now-available/) ，今年他们又推出了[安卓 Q beta](https://www.xda-developers.com/android-q-beta-3-released/) 。除了正式的 Android Q 测试版，谷歌今年还发布了正式的 Q 测试版 GSI，因此任何拥有 Project Treble 兼容设备的开发人员都可以安装最新的 Q 版本，而不必等待数月才能到达他们的设备。这种测试下一个 Android 版本的新方法给了开发者更多的机会，因此也给了他们更多的时间，来测试他们的应用程序对 Android 的重大改变。

不幸的是，目前安装 GSI 的方法很困难。它需要解锁引导加载程序，这意味着擦除所有用户数据和/或取消保修，并通过快速引导协议刷新映像。如果他们的设备[甚至允许解锁引导程序](https://www.xda-developers.com/xda-huawei-decision-stop-bootloader-unlocking/)，这对于一个应用开发者来说并不是一个快速简单的过程。这就是为什么在过去几个月的里，谷歌一直在研究一种启动 GSIs 的新方法。输入一个新功能，称为动态系统更新，或 DSU。

(这项功能之前是以“实时图像”、“动态 Android”和“Android on Tap”的名称开发的，所以如果谷歌在几周或几个月后称之为其他东西，不要感到惊讶。)

## Android Q 中的动态系统更新

DSU 特性的目标是允许开发人员在不干扰当前安装的情况下启动到 GSI。这意味着不需要解锁引导加载程序，也不需要擦除用户数据。安装过程也大大简化了，因为谷歌已经通过 ADB 提供了一个命令行界面和一个可以通过意图控制的应用程序。下面是使用 DSU 启动 GSI 的样子:

在该视频*中，运行 Android Q beta 3 的谷歌 Pixel 3 XL 重启进入 GSI。在这种环境下，应用程序开发人员可以安装并测试他们的应用程序的 Q API 兼容性。当他们完成测试后，他们可以简单地重新启动设备上的常规 Q beta 3 软件。你基本上是双启动 GSI，所以你可以安全地测试你的应用程序！

*我们在谷歌 I/O 2019 上录制了这个视频，当时 DSU 还没有公开发布，所以在拍摄的 Pixel 3 XL 上的 Q beta 3 版本被谷歌稍微修改了一下，以包括 DSU 支持。如果符合以下要求，运行 Q beta 4 和更高版本的设备有资格支持 DSU。

### 动态系统更新的要求

对谷歌来说，实现双重启动和运行并非易事。谷歌的 DSU 测试平台 Pixel 3 的分区管理方式必须做出重大改变。因此，对 DSU 支持的第一个主要要求是设备支持动态分区。动态分区涉及一个真正的存储分区，它被划分成可调整大小的逻辑分区，如系统、供应商、odm、oem、产品等。在安装 GSI 的过程中，通过从现有的用户数据分区中取出未使用的块，为新的系统和用户数据分区保留空间。由于这些新分区的大小可能有几千兆字节，DSU 支持仅对逻辑分区有意义，否则设备将需要永久保留几千兆字节的存储空间用于 GSI 安装。

其他需求包括一个 ramdisk，它决定是引导到恢复、系统还是逻辑分区，以及一个元数据分区来存储 GSI 的元数据。根据项目三冠王 Iliyan Malchev 的说法，一般来说，DSU 支持的构建模块是 Android Q 发布要求。我们不确定*支持 DSU 所需的一切*是否是 Android Q 发布的要求，但我们可以假设，即使不是所有的设备都发布了 Android Q *也可以*支持 DSU，即使谷歌目前没有要求他们这样做。到目前为止，只有 Pixel 3、Pixel 3 XL、Pixel 3a 和 Pixel 3a XL 具有动态分区，而在这些设备中，只有 Pixel 3 和 Pixel 3 XL 支持 Android Q beta 4 中的 DSU。虽然 DSU 支持不是必需的，但谷歌希望原始设备制造商无论如何都能启用该功能，因为它简化了三重兼容性的安全测试。例如，OEM 软件工程师可以将 GSI [放在 SD 卡](https://android-review.googlesource.com/c/platform/system/gsid/+/928766)上，这样他们就可以在多个设备上快速启动以测试三重兼容性。

### 动态系统更新的安全性

由于 DSU 本质上引入了第二个操作系统，谷歌需要确保这个新的安装不能被篡改，以破坏设备的完整性。因此，与原始安装相同的基本安全保护也适用于 GSI 安装:Android 验证的引导和 SELinux 策略。此外，只有具有 INSTALL _ DYNAMIC _ SYSTEM signature | privileged 权限的应用程序可以启动 GSI 安装，而具有 MANAGE_DYNAMIC_SYSTEM signature 权限的应用程序可以启用/禁用或擦除 GSI 安装。这意味着只有可信的系统级应用程序才能与 DSU 一起工作。

为了确保原始用户数据得到保护，谷歌在 Android Q 中添加了一个名为“**检查点**的[额外保护机制](https://android.googlesource.com/platform/system/vold/+/master/Checkpoint.cpp)，该功能通过将检查点分区恢复到原始状态来防止用户数据被破坏。然而，检查站不仅对 DSU 有用。它们还用于防止拙劣的[项目主线](https://www.xda-developers.com/android-q-project-mainline-security/) APEX 模块和 [A/B](https://android.googlesource.com/platform/system/vold/+/d3992498556fb1dce783d9d5e59f38cad492a6c3) OTA 更新。([带有 A/B 分区](https://www.xda-developers.com/how-a-b-partitions-and-seamless-updates-affect-custom-development-on-xda/)的设备已经有回滚保护，但是这些回滚需要工厂数据重置，而用户数据检查点则不需要。)

### 安装 GSI

如果你的设备像 Pixel 3 系列一样支持 DSU，那么安装 GSI 就很容易了。首先，您必须确保通过以下两种方式之一启用动态系统功能标志:

1.  如果您使用的是用户调试版本，请在设置>系统>开发选项>功能标志中启用 settings_dynamic_android 标志。
2.  如果您使用的是用户版本，运行以下 adb shell 命令:

    ```
     setprop persist.sys.fflag.override.settings_dynamic_system 1 
    ```

然后，从谷歌或你设备的原始设备制造商那里下载最新的安卓 Q 测试版 GSI。(DSU 只允许安装由谷歌或原始设备制造商签名的 GSI。)下载后，使用 [simg2img](https://github.com/anestisb/android-simg2img) 将稀疏图像转换为原始图像。使用 gzip 打包原始映像，然后将生成的归档文件复制到设备外部存储(例如/data/media/0/Download)或实际外部存储介质(如物理 SD 卡)上的某个位置。最后，以正确的意图启动 DynamicSystemInstallationService 应用程序，开始安装:

```
 adb shell am start-activity \ -n com.android.dynsystem/com.android.dynsystem.VerificationActivity \ -a android.os.image.action.START_INSTALL \ -d file:///storage/emulated/0/Download/system_raw.gz \  
```

一旦你点击重启，你将启动到 GSI。该设备在 GSI 的可用性取决于您的设备的 OEM 厂商实施 Treble 的情况如何(或者说，他们违反 Treble 兼容性的程度有多低)。)有些设备使用 GSIs 会比其他设备更好，但一般来说，不要指望将此安装用作日常驱动程序。你应该测试你的应用程序，然后通过重启退出。如果您想留在 GSI 安装中进行进一步的测试，那么您可以使用 [gsi_tool](https://android.googlesource.com/platform/system/gsid/+/refs/heads/master/gsi_tool.cpp) shell 命令。

DSU 的完整 GSI 安装说明可以在[这里](https://developer.android.com/topic/dsu#using-dsu)找到。bug 可以在 [Google Issue Tracker、](https://issuetracker.google.com/issues?q=componentid:470386%2B) [Reddit](https://www.reddit.com/user/AndroidGSI) 或者 [Stack Overflow](https://stackoverflow.com/questions/55841972/getting-started-with-gsi) 上归档。

### 动态系统更新背后的原因

当我与谷歌 I/O 的 Iliyan Malchev 交谈时，他重申了 Treble 团队的 Hung-ying Tyan 在 11 月的 Android 开发峰会上关于早期 GSI 接入的讲话。谷歌让 DSU 去**尽可能广泛地征集反馈**。目标是提高 GSI 的质量，反过来**也会提高未来安卓版本的质量**，因为 GSI 是最纯粹的安卓形式。谷歌是目前唯一一家测试下一版本 GSI 兼容性的公司(例如，Android Q 系统映像在 Android P 供应商实现上的工作效果如何)，但随着越来越多的人使用 GSI 并提供反馈，原始设备制造商可以修复三重兼容性违规，因此 GSI 在未来会工作得更好。Iliyan 表示，原始设备制造商和高通这样的供应商对在下一版本的系统映像中重用以前 Android 版本的供应商映像非常感兴趣。像 DSU 这样的倡议帮助谷歌和原始设备制造商填补了像 VTS 和 CTS-on-GSI 这样的自动化测试的覆盖缺口。因此，谷歌让更多的测试人员对下一个 Android 版本给出反馈，同时也听到关于三重兼容性违规的消息，以便 OEM 可以改进他们的工作。

Android Q 中添加的动态系统更新是受欢迎的，但它不会是你们一些人所希望的双引导解决方案。如前所述，只有谷歌或原始设备制造商签署的系统镜像可以安装。当我问 Iliyan 关于扩展 DSU 以支持替代 Android 系统的生态系统的可能性时，他说这在技术上是可行的，因为 DSU 只是一个提供系统映像的渠道。任何原始设备制造商都可以使用它，只要最终结果是 Android 兼容的。谷歌还没有创造出 OTA 系统的替代品，DSU 也不打算用于真正的双引导。无论如何，谷歌在 Treble 上所做的工作正在使 Android 更加模块化，所以如果原生双引导在未来成为现实，我不会感到惊讶。