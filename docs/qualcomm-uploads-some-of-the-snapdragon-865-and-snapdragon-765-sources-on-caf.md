# 高通骁龙 865，骁龙 765 来源上传到 CAF

> 原文：<https://www.xda-developers.com/qualcomm-uploads-some-of-the-snapdragon-865-and-snapdragon-765-sources-on-caf/>

# 高通在 CAF 上传了一些骁龙 865 和骁龙 765 的资料

在 Code Aurora 论坛上，高通发布了他们的骁龙 865 和骁龙 765 移动平台的一些源代码。

回到 2019 年 12 月，在骁龙科技峰会期间，高通宣布了[骁龙 865](https://www.xda-developers.com/qualcomm-snapdragon-865-processor-specifications-features/) 和[骁龙 765](https://www.xda-developers.com/qualcomm-snapdragon-765-processor-specifications-features/) 移动平台。这些芯片组是高通迄今为止最强大的旗舰和中端 SOC，它们已经在许多高端设备上出货，如三星 Galaxy S20 (865)，小米 Mi 10 (865)，一加 8 (865)和 OPPO Reno3 Pro (765)。自高通首次宣布这些 SOC 以来的 4 个多月里，该公司已经开始上传与这两个移动平台相关的一些资源。

Code Aurora Forum，简称 CAF，拥有各种高通骁龙 SOC 的源代码。作为 SoC 供应商，高通向 OEM/ODM 分发 Linux 内核的分叉版本，然后 OEM/ODM 在出货设备上添加特定于设备的更改。此外，高通对 AOSP 框架进行了修改，以优化该公司骁龙移动平台的安卓系统。高通将他们修改过的 Linux 内核、AOSP 框架和其他软件工具私下分发给它的合作伙伴，作为董事会支持包(BSP)的一部分。另一方面，CAF 是高通公开发布这些 Linux 内核变化和 AOSP 框架变化的地方。这个 CAF 版本对于那些希望把它作为一个起点而不是纯粹的 AOSP 的定制 ROM 开发者来说是有用的，这就是为什么你有时会在我们的论坛上看到“基于 CAF”的 ROM。

总结一下:

*   主线 Linux 内核- > Android 通用内核- > SoC 专用内核(高通在 CAF 上发布的)- > BSP ->设备专用内核(要求 OEM 厂商发布的)
*   AOSP-> AOSP+SoC 厂商做的框架改动(Apache 2.0 下不需要发布，但高通反正要发布)- > BSP - > OEM Android 软件(OxygenOS，ZenUI 等。)

现在就可以在 CAF 上浏览[【骁龙 865】(代号“科纳”)](https://source.codeaurora.org/quic/la/platform/vendor/qcom/kona/)[【骁龙 765】(代号“利托”)](https://source.codeaurora.org/quic/la/platform/vendor/qcom/lito/)的相关发布。高通之前在 2019 年 5 月发布了骁龙 855 [的部分源代码，这意味着今天的发布比我们预期的提前了大约一个月。](https://www.xda-developers.com/qualcomm-snapdragon-855-snapdragon-675-sources-caf/)