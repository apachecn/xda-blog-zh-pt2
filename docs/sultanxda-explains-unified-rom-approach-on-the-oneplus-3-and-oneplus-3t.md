# SultanXDA 解释了 OnePlus 3/3T 上的统一 ROM 方法

> 原文：<https://www.xda-developers.com/sultanxda-explains-unified-rom-approach-on-the-oneplus-3-and-oneplus-3t/>

当我们报道 XDA 知名开发商 [Sultanxda](http://forum.xda-developers.com/member.php?u=4800121) 发布了他的[定制 CyanogenMod 13 ROM 和 OnePlus 3T](https://www.xda-developers.com/sultanxdas-unofficial-cyanogenmod-13-lands-on-the-oneplus-3t-through-unified-builds/) 内核时，许多人惊讶地看到为 OnePlus 3T 发布的“相同”ROM 版本也出现在了 OnePlus 3 上(反之亦然！).

Sultanxda 采用统一的方法为 [OnePlus 3](http://forum.xda-developers.com/oneplus-3) 和 [OnePlus 3T](http://forum.xda-developers.com/oneplus-3t) 分发 rom，因为它们的硬件和低级软件非常相似。这意味着 ROM 提供了两种设备之间的交叉兼容性，可以将相同的 ROM 压缩文件分发给两个设备。交叉兼容的 zip 允许用户(以及开发者)不必担心意外地刷新错误的 zip 并得到一个砖砌的设备。这并不是说 OnePlus 3/3T 很容易砌砖——它只是让所有相关方都不那么头疼。

为了鼓励采用他的方法，我们联系了 XDA 公认的开发者 Sultanxda，让他对整个过程做了更多的解释。以下是从对话中获得的重点内容:

### 允许统一 rom 的 OnePlus 3/3T 有何不同？

统一 ROM 之所以可能，是因为一加统一了 BSP(专有库)[板支持包]。尽管统一内核很容易，但统一 ROM 对于[ROM]开发者来说通常是不可能的，因为 BSP 中的不一致性只有 OEM 才能解决。**在我这边，我所要做的就是统一内核，分离一些 GPU 固件镜像。Snapdragon 820 和 821 之间的 GPU 固件映像不同，因此它们不能交叉兼容。**我修改了内核，让它[为每个设备加载正确的 GPU 固件](https://github.com/sultanxda/android_kernel_oneplus_msm8996/commit/1982414e09b5d34a8fc6d9aa0646d30cf6eec958)来解决这个问题。然后我[在这个提交中将相应的固件映像](https://github.com/sultanxda/proprietary_vendor_oneplus/commit/c65ab93923769e7c65fcea798ffff0ddb5ec213b)添加到 ROM 中。其余特定于设备的固件映像(如调制解调器映像)位于每个设备上的固件分区中，因此**GPU 问题** ***是我面临的唯一与固件相关的问题**。*

### ROM 和内核如何判断它是哪个设备？

多亏了引导装载程序，内核知道它运行在哪个设备上。引导加载程序选择与其主板 ID 匹配的设备树配置(打包到内核映像中),并将此配置传递到内核。这使内核能够灵活地为 OnePlus 3 和 OnePlus 3T 加载适当的配置。您可以通过超链接找到 [OnePlus 3](https://github.com/sultanxda/android_kernel_oneplus_msm8996/blob/9857213361a3ade42786d03ea6347136a6ebd60f/arch/arm/boot/dts/qcom/msm8996-v3.0-pmi8996-mtp_15801.dts#L23) 和 [OnePlus 3T](https://github.com/sultanxda/android_kernel_oneplus_msm8996/blob/9857213361a3ade42786d03ea6347136a6ebd60f/arch/arm/boot/dts/qcom/msm8996pro-pmi8996-mtp_15811.dts#L23) 的板卡 ID。

### 你只需要一个修改过的内核来支持统一构建吗？

***不，ROM 也必须统一。**一加从 OP3 的公开 Betas 版开始统一 BSP，并在 OP3T OxygenOS 正式版中保持统一。**这意味着 rom 必须使用 OP3 开放测试版或 OP3T 官方 OxygenOS 版本的专有库才能实现统一。**还有我上面描述的 GPU 固件镜像要求，OP3T 的触摸屏固件也需要包含在 ROM 中(这是在我上面链接的 GPU 固件提交中添加的)。*

此外，对于统一内核有一个警告:开发人员必须要么使用我的内核(已经统一)，要么他们必须在 OP3T 的 OxygenOS 内核中添加 OP3 支持。由于骁龙 821 的不完全支持，对 OP3T 的支持不能简单地添加到 OP3 的内核中，因此统一可能需要有意愿的 OP3 开发者做大量的工作。当我收到 OP3T 时，我的内核已经完全支持骁龙 821(因为我的内核是基于 CAF 的骁龙 821 分支)，所以统一过程对我来说相当容易。

我相信很多开发人员更愿意使用 OP3T 的 OxygenOS 内核，而不是我的内核，这需要在它上面添加对 OP3 的支持。我并没有考虑为 OxygenOS ROMs 开发一个统一的内核，所以可能需要做更多的工作来实现它。

### 其他开发人员可以看看代码，看看这是如何做到的吗？

是的。Sultanxda 提到他所有的作品都可以在他的 [GitHub 账户](https://github.com/sultanxda)上公开获得，所以任何有必要知识的人都可以看到 ROM 的统一是如何进行的。当然，这个过程有点复杂，需要一定水平的专业知识，但是**这是一个“一劳永逸”的过程**，好处是维护更少，重复工作更少，而且人们不会混淆两个设备的文件，因为只有一个 zip 文件可以用于两个设备。一旦 ROM 或内核被统一并被确认在 OnePlus 3 和 OnePlus 3T 上完全可用，就只需要很少的额外工作。

* * *

我们希望我们带来了新的信息，这将有助于更多的开发者选择设备的统一版本。[OnePlus 3T 上的开发正在增长](https://www.xda-developers.com/cyanogenmod-14-1-joins-oneplus-3ts-rom-roster-as-development-picks-up/)，统一版本是这两款设备未来的发展方向。