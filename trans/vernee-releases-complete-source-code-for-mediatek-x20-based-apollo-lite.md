# Vernee 发布基于联发科 X20 的 Apollo Lite 源代码

> 原文：<https://www.xda-developers.com/vernee-releases-complete-source-code-for-mediatek-x20-based-apollo-lite/>

如果 Vernee 这个名字对你来说很陌生，你并不孤单。毕竟，当你把这个微不足道的中国 OEM 厂商与三星、HTC 或 LG 这样的行业巨头相比时，你会发现它毫无机会。

然而，有一件有趣的事情将这家 OEM 厂商与中国类似的智能手机 OEM 厂商和一些行业巨头区分开来。

[![Vernee Apollo Lite](img/cdfde096ee1d769a8c4cf9a8448a7cd2.png) ](http://static1.xdaimages.com/wordpress/wp-content/uploads/2016/11/1476916912402700069.jpg) Vernee 目前的智能手机阵容由旗舰产品 Vernee Apollo 及其规格略低的兄弟产品 [Vernee Apollo Lite](http://www.vernee.cc/apollo-lite/overview.html) 打头阵。阿波罗运行在联发科 [Helio X25](http://mediatek-helio.com/x20/) 6797T SoC 上，而阿波罗 Lite 运行在联发科 [Helio X20](http://mediatek-helio.com/x20/) 6797 SoC 上。这两种 SoC 的区别主要在于 CPU 和 GPU 的最高频率限制。本文的重点将是较小的兄弟，Vernee Apollo Lite 及其 Helio X20 SoC。

为了让自己与众不同，Vernee 走了一条与众不同的道路，吸引经常推动手机购买的人群，但没有形成非常大的数量:发烧友和开发者....

他们通过发布 Vernee Apollo Lite 的整个源代码来做到这一点，包括几个专有元素。是的，你没看错。

当然，你不必相信我的话。你可以查看公告并从 [Vernee 的论坛](http://bbs.vernee.cc/forum.php?mod=viewthread&tid=1455&extra=page%3D1&mobile=2)下载源代码，但被告知它不是桌面友好的，你将不得不使用移动浏览器来访问该链接。为了方便起见，我们附上论坛帖子的截图。

由于下载是在速度不可靠的中国服务器上进行的，我们论坛上的用户已经创建了一个压缩源代码的镜像，同时[将代码完全上传到 GitHub](https://github.com/MT6797?tab=repositories) ，这将使浏览更加容易，而不需要下载完整的源代码。

Vernee 发布的源代码足够完整，可以为该设备构建一个标准 ROM。你还可以在其中找到许多专有的联发科代码，这使得这种源代码下降对于其他 Helio X20 MT6797 SoC 设备非常重要。除此之外，它还包括引导程序代码、预加载程序以及其他专有资料，如相机 HAL。

我们被告知，这也不是 Vernee 第一次发布完整的源代码。XDA 承认开发人员 [DerTeufel1980](http://forum.xda-developers.com/member.php?u=4196889) ，团队 M.A.D .的成员，曾集体[负责为联发科设备](http://www.xda-developers.com/xda-external-link/jiayu-s3-plus-mediatek-mt6753-receives-unofficial-aosp-7-0-rom/)带来全功能的 Android 7.0，也评论说 Vernee 为其中一款中规格设备 Vernee Thor 也做了同样的事情。在大多数高通设备获得其 Alpha 版本之前，这样的源代码投放已经帮助他们更新了专有的 RIL 和相机库，并构建了功能完整的 Android 7.1 ROMs。

那么这给 Vernee 和 Apollo Lite 带来了什么？由于这是一个不太知名的品牌，由于完全缺乏信息和品牌意识，它没有引起开发者的兴趣。尽管如此，该设备的用户告诉我们，在其他论坛上可以获得该设备的工作 [TWRP](http://bbs.vernee.cc/forum.php?mod=viewthread&tid=981) 以及早期 CM13 版本。由于这款设备在 XDA 开发者大会上还没有自己的论坛，Vernee Apollo Lite 的用户和开发者已经在这个帖子中聚集了。

在所有这些之后，有人可能会问:问题出在哪里？非常令人惊讶的是，没有一个我们能立即发现。你会得到一台规格不错的设备:5.5 英寸 FHD 显示屏，十核联发科 Helio X20 MT6797 SoC，三集群设置，4GB lpddr 3 RAM，32GB 内部存储，可扩展 micro-sd，16MP 后置摄像头，三星 f/2.0，3,180 mAh 不可拆卸电池，USB Type-C 和联发科的 Pump Express 3.0 快速充电标准。

所有这些都预装了 Android 6.0，价格为 229 美元(加上 Vernee 不断提供优惠，所以你可以以更低的价格买到一个)，这里没有什么可以立即抱怨的。是的，廉价的中国智能手机在使用几个月后就有不可靠的坏名声，但我与其他中国品牌的个人经历改善了我对其可用性和硬件功能的总体看法。

来自一个不知名品牌的这种对开发者友好的态度隐约让我们想起了类似的自发事件，其中一些事件以深深的失望而告终。原始设备制造商可以随时承诺对开发者友好，但最终，行动才是最重要的——不管这是一种时尚还是一种做生意的方式。

你对 Vernee 发布 Apollo Lite 的源代码有什么看法？请在下面的评论中告诉我们！

*非常感谢 [Vernee 线程](http://forum.xda-developers.com/general/device-reviews-and-information/vernee-apollo-lite-helio-x20-4gb-ram-hd-t3362898/)中所有论坛成员的提示。*