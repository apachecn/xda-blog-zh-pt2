# 小米可能正在开发一款名为 Mi Watch 的 Wear OS 智能手表

> 原文：<https://www.xda-developers.com/xiaomi-mi-watch-wear-os-smartwatch/>

虽然可穿戴设备市场正在蓬勃发展，但对运行谷歌 Wear OS 的智能手表的需求却没有那么热。Fossil Group 和 Mobvoi 仍然支持基于 Android 的智能手表平台，但三星和华为等大型 Android 智能手机品牌选择发布运行自己操作系统的智能手表。这种情况有很多原因，但也许有一个解决方案可以重振该平台的销售，那就是平价智能手表的激增。例如，小米以其广泛的平价消费电子产品而闻名，他们可能正准备通过一款名为 Mi Watch 的智能手表涉足 Wear OS 生态系统。

前几天，谷歌开始推出 Wear OS 应用程序的 2.28 版本。在这个应用程序中，出现了一个名为“小米 _ 伴侣 _ 姓名”的新字符串，其值为“Mi Wear”。小米目前在谷歌 Play 商店上提供“Mi Fit”应用程序，在自己的应用程序商店上提供“ [Mi Health](https://www.xda-developers.com/mi-health-xiaomi-fitness-app/) ”应用程序，但目前没有“Mi Wear”应用程序。

查看代码中引用该字符串的位置，我们可以看到 Wear OS 应用程序正在检查是否存在“PartnerCompanion”应用程序。这里显示的一个包名是“com.huawei.health”，对应的是[华为健康](https://play.google.com/store/apps/details?id=com.huawei.health)应用。华为 Watch 和 Watch 2 都运行在 Android 上，而不是像较新的 Watch GT 智能手表那样运行在 Lite OS 上，所以在这里看到华为健康的参考并不奇怪。另一方面，包名“com.xiaomi.wearable”与我们在谷歌 Play 商店、小米的应用商店或 APKMirror 等第三方网站上找到的任何应用都不对应。和华为健康一样，我们可以看到这个未发布的“Mi Wear”应用有一个 Wear OS 应用正在检查的“PartnerService”。

在 Wear OS APK 中提到一个未发布的 Mi Wear 应用足以告诉我们小米正在开发一款运行 Android 的智能手表，但进一步分析表明，一个新的智能手表名称已经出现在代码中:Mi Watch。虽然我们无法确认这是否会成为小米新智能手表的名字，但它听起来确实非常接近小米给智能手表起的名字。毕竟，该公司的整个智能手表、平板电脑和电视产品系列都带有“Mi”品牌。

最后，我们不知道哪家公司将为小米生产这款产品。例如，华米[为小米生产可穿戴的 mi 手环](https://www.xda-developers.com/xiaomi-mi-band-5-huami/)，因此小米的合作伙伴之一有可能正在生产这款产品。如果我们对这款潜在智能手表有更多了解，我们会让你知道。

* * *

*Via:[9 to 5 Google](https://9to5google.com/2019/09/23/xiaomi-wear-os/)*

*感谢 PNF 软件为我们提供了使用许可 [JEB Decompiler](https://www.pnfsoftware.com/?aid=xdadev) ，这是一款针对 Android 应用的专业级逆向工程工具。*