# 并非所有支持蓝牙 5 的智能手机都是一样的，原因如下

> 原文：<https://www.xda-developers.com/check-bluetooth-5-all-features-supported/>

尽管蓝牙从现代智能手机诞生的第一天就已经存在，但它仍在不断发展。蓝牙规范的新迭代每隔几年发布一次，最新的是 2016 年宣布的[蓝牙 5](https://www.bluetooth.com/bluetooth-technology/bluetooth5/bluetooth5-paper) 。虽然目前大多数智能手机都正式支持它，但大量智能手机都缺少蓝牙 5 规范中定义的关键功能。最近，Reddit 上的[帖子强调了这一点，引起了我们的注意。蓝牙 5 带来了许多新的改进和优化，但遗憾的是其中一些是可选的。这意味着智能手机制造商可以正确地声称他们的设备支持蓝牙 5，而忽略了规范中的一些关键改进。](https://www.reddit.com/r/Android/comments/ak2tqq/what_is_really_wrong_with_bluetooth_5_how_the/)

## 新物理学

蓝牙 5 规范定义的重要新特性之一是三种物理层的选择。PHY 是物理层的首字母缩写，实质上是芯片组。芯片组至少必须支持 LE 1M PHY 以支持蓝牙 5。LE 1M PHY 是蓝牙 4 中使用的 PHY，它具有每秒 1 兆符号(Ms/s)的符号速率。然而，勒 2M PHY 将这一速度提高了一倍，达到 2 毫秒/秒。此外，还有勒编码的 PHY，它在不增加功耗的情况下，提供了大约四倍于蓝牙 4 的范围。

关于乐 2M 和乐编码的关键是，对于蓝牙 5，它们都不是强制性的。这意味着制造商可以提供与蓝牙 4 相同的通信能力，但吹捧蓝牙 5 支持。虽然大多数设备支持 le 2M 或 LE 编码，但绝大多数设备并不同时支持两者。

## 延伸广告

蓝牙 5 带来的另一个改进是更长的广告包。广告数据包是您的设备在尝试与其他设备通信时广播的内容，本质上是向其他设备广告自己。更长的广告数据包意味着您的设备可以发送更多关于自身的信息，并接收更多关于其他设备的信息。信标从扩展广告中受益最大。beacon 是一种小型蓝牙发射器，公司用它来做产品广告等。例如，可以在游乐园部署一个信标，当人们走过时，他们的手机会接收到来自信标的信号，并接收关于某个景点的信息。广告包越长，可以提供的信息就越多。在蓝牙 4 中，广告数据包被限制为 37 个八位字节的信息。然而，在蓝牙 5 中，数据包可以长达 255 个八位字节，这是一个巨大的进步。

不过，在蓝牙 5 中，延长广告长度并不是强制性的。此外，扩展广告不向后兼容，这意味着蓝牙 4 设备甚至不能接收具有扩展长度的数据包。这是不好的，因为这意味着支持延长广告长度的少数设备将几乎没有其他设备可以利用它。

| 

特征

 | 

蓝牙 4

 | 

蓝牙 5

 |
| --- | --- | --- |
| 乐 1M | 是 | 是 |
| 勒 2M | 不 | 是(可选) |
| LE 编码 | 不 | 是(可选) |
| 扩展广告 | 不 | 是(可选) |

总之，蓝牙 5 中可用的三个主要特征对于被分类为支持蓝牙 5 的设备来说不是必须被支持的。当然，蓝牙 5 带来的其他功能也是强制性的——例如改善对其他频率的干扰——但这些更多的是生活质量的改善，而不是改变游戏规则的东西。

## 我的设备支持这些功能吗？

有一个非常简单的方法来测试你的设备是否支持上面提到的三个特性中的任何一个。首先，只需从谷歌 Play 商店下载 nRF Connect。

从那里，滚动所有的介绍信息(图 1)。接下来，单击“确定”允许应用程序将文件复制到您的设备，这些文件对应用程序正常运行至关重要(图 2)。现在，点击屏幕左上角的三格“汉堡”按钮，然后点击“设备信息”(图 3 和图 4)。您应该会看到一个带有“是”或“否”的特性列表。如果“支持高速(乐 2M)”旁边有“是”，则您的设备支持 2 倍速度的蓝牙 5。如果“支持长距离(PHY 编码)”旁边有“是”，则您的设备支持 4x 范围的蓝牙 5。如果“支持扩展广告”旁边有“是”，则您的设备支持蓝牙 5 的 255 八位字节广告(图 5)。

目前，许多旗舰似乎至少缺少其中一项功能。然而，情况正在改善。虽然三星 Galaxy S9+仅支持其中一项功能——PHY 2m 层，但 Galaxy S10+支持所有三项功能。小米和一加旗舰也支持所有三个功能。POCO F1 等著名的廉价设备也支持一切，因此价格不太可能是问题的根源。

三星直到最近才增加对所有三个功能的支持，这很不寻常，因为他们一直以来都在设备中尽可能多地添加功能。同样令人惊讶的是，一加包含了一切，因为他们之前不愿意添加对他们认为不必要的功能的支持。不那么令人惊讶的是小米的全力支持，过去他们对功能齐全的手机并不陌生。话虽如此，考虑到小米之前对增加对热门功能的支持(如[、相机 2 API](https://www.xda-developers.com/redmi-note-7-camera2-api-google-camera/) )的疑虑，一些人可能会不同意。

| 

设备

 | 

勒 2M

 | 

LE 编码

 | 

延伸广告

 |
| --- | --- | --- | --- |
| 三星 Galaxy S10+(骁龙) | 是 | 是 | 是 |
| 小米 Mi 9 | 是 | 是 | 是 |
| 一加 6T | 是 | 是 | 是 |
| 华为 Mate 20 Pro | 是 | 是 | 是 |
| 华为 Mate 20 X | 是 | 不 | 不 |
| 谷歌像素 3 | 是 | 不 | 是 |
| 诺基亚 7 Plus | 是 | 不 | 不 |
| 雷蛇手机 2 | 是 | 不 | 是 |
| Pocophone F1 | 是 | 不 | 是 |
| 三星 Galaxy Note 9(骁龙) | 是 | 不 | 不 |

遗憾的是，很少有设备支持蓝牙 5 中规定的所有功能，因为要利用新功能，通信设备都需要支持该功能。根据在前面提到的 Reddit 帖子上附和他们设备信息的用户，市场目前接近 0%,而不是完全支持的设备的 5%。谢天谢地，最近的旗舰似乎支持所有的主要功能。

蓝牙 5 是设备连接向前迈出的一大步，所以智能手机社区花了这么长时间才跟上真是令人惊讶。但现在已经清楚我们错过了多少，我们可以让 OEM 知道错过这些功能是不可接受的，并希望巩固他们已经开始做出的改变。