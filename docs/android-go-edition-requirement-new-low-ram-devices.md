# 谷歌计划让新的低 RAM 设备需要 Android Go

> 原文：<https://www.xda-developers.com/android-go-edition-requirement-new-low-ram-devices/>

2017 年，[谷歌宣布](https://www.xda-developers.com/android-go-optimizes-android-o-to-run-on-low-end-devices/)面向低端设备的安卓修改版。“Android Go 版”是专为内存为 1GB 或更少的设备打造的。与此同时，谷歌发布了其许多[流行服务](https://www.xda-developers.com/android-google-go-assistant-lens/)的轻量级[“Go 版】版本](https://www.xda-developers.com/google-camera-go-hands-on-gcam/)。不过，Android Go 从来都不是这些低端设备的必要条件。然而，这种情况可能很快就会改变。

根据谷歌“Android 11 Go edition 设备配置指南”(日期为 2020 年 4 月 24 日)的泄露副本，谷歌计划将 Android Go Edition 作为新推出的 2GB 或更低 RAM 设备的要求。以下是将要实施的新要求:

*   *   从 Android 11 开始，具有 512MB RAM(包括升级)的设备没有资格预载 GMS。
    *   所有使用 Android 11 发布的新产品，如果它们具有 2GB 或更少的 RAM，则必须为 activity manager . islowramdevice()API 返回 true，并作为 Android Go 设备发布。
    *   从 2020 年第四季度开始，所有使用 Android 10 发布的新产品，如果其内存为 2GB 或更少，则必须为 activity manager . islowramdevice()API 返回 true，并作为 Android Go 设备发布。
    *   以前推出的标准 GMS 配置的 2GB RAM 设备不应通过 MRs 或 letter 升级转换为 Android Go 配置。它们仍将是标准的安卓系统

这意味着从今年晚些时候，也就是 2020 年第四季度开始，任何配备 2GB 或更少 RAM 的新 Android 10 设备*都必须*使用 Android Go 版本。此外，任何使用 Android 11 的设备*和内存小于 2GB 的设备*都必须使用 Android Go。基本上，低 RAM Android 10 设备仍有一些时间来满足要求，但新的低 RAM Android 11 设备将不会有这样的机会。**

如前所述，Android Go 最初是为内存小于 1GB 的设备设计的，但对于 OEM 厂商来说并不需要*来实现。配备 2GB 内存的 Android Go 设备的推出实际上也是一种新的趋势。这一变化似乎发生在去年年底，谷歌更新了网站以反映这一变化。2GB RAM 设备的引入将 64 位内核/用户空间带入了 Go Edtion 生态系统。*

这些即将到来的要求应该会对低端 Android 设备的看法产生相当大的变化。放弃对超低端 512MB 设备的 Android 11 GMS(谷歌移动服务)支持意味着我们在未来不会看到它们。而 Android Go 安装在 1GB 和 2GB 设备上意味着整体性能更好。这个范围内的设备可能会非常受欢迎，这使得 Android 体验尽可能好变得非常重要。

我们上周从一个消息来源那里听说了这个即将到来的变化，这份文件证实了我们之前所听到的。然而，有可能从我们的来源和这份文件的信息已经过时，谷歌可能已经收回这一要求。我们将密切关注谷歌的任何公开声明以及内部文档的任何更新，看看我们是否能找到更多信息。

*感谢蒂莉·科特曼( [@deletescape](https://twitter.com/deletescape) )找到了包含这些信息的文档！*