# Android P 中的一项新设置将允许运营商定义 LTE 信号条的显示方式

> 原文：<https://www.xda-developers.com/android-p-carriers-define-lte-signal-bars/>

大约 8 年前，全球引入了 4G LTE 技术，尽管许多公司都在展望建设 5G 网络，但世界上许多地区，尤其是美国以外的地区，仍然需要应对较差或劣质的 LTE 信号强度。例如，在委内瑞拉，我经常发现自己在室内时注意到 LTE 信号强度的下降，在那里网络可以中继回 3G、2G 或完全失去信号。这在美国的一些地方也是一个常见的问题，尤其是在农村和偏远地区。

影响手机信号的因素有很多，包括设备的外部构造、制造商提供的频段、运营商，甚至是你的位置，但 Android 以同样的方式解析接收到的信号(以 dBm 为单位)，将其准确地反映为大家都熟悉的信号条。然而，Android P 可能会改变一些事情。

[我们之前报道过](https://www.xda-developers.com/android-p-signal-strength-carriers/)在下一个主要版本的 Android 中，运营商将有能力对用户隐藏信号强度，但似乎 Android P 也将允许运营商决定如何定义和向用户显示实际的 LTE 信号条。

## Android P 中的 LTE 信号条是怎么回事？

LTE 信号条只是信号强度的直观表示:手机以 dBm 为单位计算您所在位置的当前手机信号强度，然后将该值解析为我们在状态栏中看到的信号条。这让普通人大致了解了他们当前所在区域的接收强度。信号条几乎存在于每一个带有蜂窝无线电的设备上，我们在现代智能手机时代之前就已经看到了。

 <picture>![](img/a95ffe86000fdb69bbaf91e992b1d99a.png)</picture> 

Signal Strength can be seen in Settings > About phone > Status as of the latest Android 8.1 Oreo release, but carriers will be able to hide this from users on Android P.

然而，我们在 Android 开源项目中发现的一对[夫妇](https://android-review.googlesource.com/#/c/platform/packages/apps/CarrierConfig/+/569544/)提交了一种新的配置，允许运营商为 5 个 LTE 信号条中的每一个定义定制的信号强度阈值。一个完整的仪表可能会显示更低或更高的 dBm 值，这可能会导致运营商的客户认为他们的信号比 Android P 更新前更强。

在 Android 8.1 及更低版本中，LTE 信号强度阈值由 Android 框架下的“config_lteDbmThresholds”值定义。由于这些是特定于设备的值，这意味着 LTE 阈值目前是特定于设备的，而不是特定于运营商的。显然，这些值很容易被制造商和运营商等修改，这意味着特定运营商的设备可能会有特定运营商的信号阈值，但这一变化表明(没有双关语)这些阈值现在是通用的，也存在于运行 Android P 的设备的解锁版本中——当用户更换 SIM 卡时，运营商的配置就会生效。

承诺中提到的运营商包括荷兰的沃达丰 Libertel(20404)、美国的威瑞森无线(311480)和澳大利亚的 Telstra corp .(50501，50511，50571，50572)。我们无法解释这些运营商为什么要求这种改变(我们已经联系威瑞森进行评论，但还没有听到关于这个问题的官方回应)，所以我们只能推测一些可能的原因。

## 为什么包括这一变化？

与信号强度隐藏一样，运营商可能会要求这项功能，而谷歌只是乐于助人。现在，这并不一定有负面的含义，因为一些运营商可能希望用实际上对特定运营商或国家有意义的数字来标准化信号条:更低或更高的 dBm 数字可能是特定运营商或国家的标准，因此，阈值可以调整，以便信号条不总是位于 1 或 5。

 <picture>![](img/657e21f647411d88ecad0e4093f9ee5f.png)</picture> 

Carriers in Venezuela, like Movistar, Movilnet, and Digitel, use only one LTE band, unlike other countries using multiple bands and frequencies. As such, weaker signal and lower dBm numbers are standard, and tweaking signal thresholds could be a good use case for these countries/carriers.

然而，对这一变化的一个不太仁慈的解释是，一些运营商可能想篡改信号强度栏后面的数字，导致非技术熟练的用户认为他们的信号在同一部手机的一个运营商上比另一个运营商好。

然而，这种变化背后的实际原因还不清楚，所以不要急于下结论。

## 现在怎么办？

截至目前，没有任何 API 受到这些变化的影响或限制，那些寻求准确测量信号强度的人可以从 Play Store 下载类似 signal strength 的应用程序，至少目前是这样。

如果运营商的目标是阻止用户访问准确的电话数据，我们可能会看到未来的努力锁定这些应用程序使用的 API，以提供蜂窝信号统计数据。