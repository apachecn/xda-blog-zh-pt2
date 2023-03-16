# 高通在 CAF 上发布骁龙 855 和 675 源

> 原文：<https://www.xda-developers.com/qualcomm-snapdragon-855-snapdragon-675-sources-caf/>

高通目前在高端市场和中端市场都占据着移动领域的主导地位。高通骁龙 855 是他们最新的高端移动片上系统，在许多不同的方面都比去年的骁龙 845 有了重大升级，Adreno 640 GPU、基于 7 纳米的八核设置和专用 NPU 只是骁龙 855 的部分改进。所述芯片组用于几款 2019 年旗舰设备，包括[三星 Galaxy S10 系列](https://www.xda-developers.com/samsung-galaxy-s10e-review-exynos/)、 [LG G8 ThinQ/V50 ThinQ](https://www.xda-developers.com/arcore-1-9-lg-g8-lg-v50-scene-viewer/) 和[一加 7/7 Pro](https://www.xda-developers.com/oneplus-7-pros-zen-mode-screen-recorder-older-oneplus/) 。另一方面，骁龙 675 是今年最引人注目的中端 SOC 之一，它被用于几款设备，如[小米红米 Note 7 Pro](https://www.xda-developers.com/xiaomi-redmi-note-7-pro-camera-update/) 。

基于骁龙的设备在我们的论坛上非常受欢迎，不仅因为它们随处可见，还因为我们有现成的资源、文档和高通芯片组的 HALs。与三星和联发科等芯片制造商相反，高通的大多数平台特定代码都可以在代码极光论坛(CAF)上公开获得，供开发人员修改。这与设备制造商提供的特定于设备的内核源代码和 blobs 相结合，使得基于高通的设备的 ROM 开发更加容易。虽然来源的缺乏不像过去那样是个大问题(毕竟，现在你可以在大多数现代设备上运行 GSI)，但 CAF 版本仍然使许多事情变得更简单。

现在，高通骁龙 855 (sm8150)和高通骁龙 675 (sm6150)的 CAF 源代码已经可用，大约是在骁龙 845 (sdm845)源代码[可用](https://www.xda-developers.com/qualcomm-snapdragon-845-sources-caf/)后 10 个月。因此，开发者现在可以开始为他们的设备进行构建了。这对用户来说意味着，在接下来的几周/几个月里，你将会看到更多基于这些平台的定制 rom 和内核。

开发者可以在这里下载并查看骁龙 855 源代码[，而骁龙 675 源代码也可以在这里](https://source.codeaurora.org/quic/la/kernel/msm-4.14/tag/?h=LA.UM.7.1.r1-14000-sm8150.0)下载[。](http://source.codeaurora.org/quic/la/kernel/msm-4.14/tag/?h=LA.UM.7.9.r1-06100-sm6150.0)