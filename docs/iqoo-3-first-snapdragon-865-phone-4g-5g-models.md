# iQOO 3 是第一款有 4G 和 5G 两种型号的骁龙 865 手机

> 原文：<https://www.xda-developers.com/iqoo-3-first-snapdragon-865-phone-4g-5g-models/>

是时候让首款搭载高通骁龙 865 的旗舰手机上市了。骁龙 865 是高通 2020 年的旗舰 SoC，[12 月](https://www.xda-developers.com/qualcomm-snapdragon-865-processor-specifications-features/)宣布。与骁龙 865 一同发布的第一批手机是骁龙 865 版的[三星 Galaxy S20](https://www.xda-developers.com/samsung-galaxy-s20-specs-features-pricing-availability/) 系列。两天后，小米在中国推出了[米 10 和米 10 Pro](https://www.xda-developers.com/xiaomi-launches-mi-10-90hz-screen-108mp-camera-snapdragon-865/) 。骁龙 865 的下一批旗舰产品是 Realme X50 Pro 和 iQOO 3。两者都计划分别于 2 月 24 日和 2 月 25 日在多个市场推出。Realme X50 Pro 和 iQOO 3 都被单独作为“印度第一款 5G 手机”进行营销。关于 iQOO 3 的细节可以在[我们之前的报道](https://www.xda-developers.com/iqoo-3-5g-48mp-quad-rear-camera-gaming-trigger-buttons/)中看到。iQOO 3 的有趣之处在于，虽然它被宣传为印度第一款 5G 手机，但它同时也是第一款同时推出 4G 和 5G 型号的骁龙 865 手机。为了搞清楚这一点，让我们深入研究骁龙 865 的调制解调器的背景。

## 骁龙 865 需要独立的骁龙 X55 调制解调器来提供连接

骁龙 865 打破了骁龙前几年的旗舰 SOC，因为它没有集成的调制解调器。骁龙 855 有一个集成的[骁龙 X24 4G LTE 调制解调器](https://www.xda-developers.com/qualcomm-x24-modem/)，同时可选地支持分立的[骁龙 X50](https://www.xda-developers.com/qualcomm-5g-snapdragon-x50-modem/) 5G 调制解调器。另一方面，骁龙 865 只支持一个单独的调制解调器:更新的[骁龙 X55](https://www.xda-developers.com/qualcomm-snapdragon-x55-5g-modem-2019-android-smartphones/) 5G 调制解调器-射频系统。(就其本身而言，这使其成为自 2014 年高通骁龙 805 以来第一款没有集成调制解调器的骁龙旗舰 SoC。)这种特殊的调制解调器是去年宣布的，打算用于骁龙 865 手机(尽管 12 月下旬的两次骁龙 855 发布会最终也使用了它)。这意味着骁龙 865 没有集成的 4G 调制解调器，也不支持单独的 4G 调制解调器。设备制造商不能将任何其他调制解调器用于 SoC。

根据高通的说法，骁龙 865 没有集成调制解调器的原因与设计 5G 旗舰手机的复杂性有关。5G 调制解调器的芯片尺寸是另一个可能的原因。第三个也是更实际的可能因素是成本。X55 5G 调制解调器本质上可能比 X24 LTE 调制解调器更贵，因为它的功能更先进。因此，采用骁龙 865 + X55 组合的手机预计将比其 4G 驱动的前辈更贵，随着高通从调制解调器芯片销售的专利许可中获得收入，其底线将受益于市场上更昂贵的旗舰手机。

骁龙 765 确实有一个集成的 5G 调制解调器(X52 调制解调器)，所以下一款骁龙旗舰 SoC 可能会有一个集成的调制解调器。在这一点上，我们不必就分立调制解调器和电池寿命的因素得出结论。这方面只能在单独测试骁龙 865 手机后才能测试，因为最终产品受到许多因素的影响。

骁龙 X55 支持 5G -毫米波和低于 6GHz 的种类。自然也是 2G/3G/4G/5G 多模调制解调器。这意味着支持传统的 2G/3G HSPA/4G LTE 网络。在 5G 支持方面，骁龙 X55 支持全球使用的 6GHz 以下和毫米波频率的 5G 频段。支持 3.5GHz、600MHz、2.5GHz 等 6GHz 以下频段，以及 26GHz、28GHz 和 39GHz 等毫米波频段。理论上，我们大多数人认为骁龙 865 +骁龙 X55 组合意味着所有骁龙 865 手机必须只有 5G。早期的骁龙 865 手机发布会验证了这种想法，但 iQOO 3 却与之背道而驰。

让我们深入研究一下。从理论上讲，每部拥有骁龙 865 调制解调器的手机都支持 6GHz 以下和毫米波 5G。然而在实际使用中，除非手机至少有三个高通的毫米波天线模块(QTM525)，否则它将无法实际使用毫米波 5G，因为毫米波信号的特性很差，[这里已经描述过了](https://www.xda-developers.com/qualcomm-snapdragon-x60-modem-5g-smartphones/)。因此，如果设备制造商希望手机支持 sub-6GHz 和 mmWave 5G，除了认证手机的 mmWave 5G 频段外，还需要在手机中集成至少三个 QTM525 天线模块，以确保它支持 mmWave 5G。因此，并不是每个骁龙 865 5G 手机都能够拥有毫米波 5G。例如，小米 10 没有这种功能，三星 Galaxy S20 的普通骁龙 865 版本也没有。今年将有更多的旗舰产品不支持毫米波，因为目前毫米波的可用性非常有限，即使在可用的地区也是如此。

4G 支持呢？骁龙 X55 调制解调器支持全球 LTE 频段。然而，这并不意味着任何带有 X55 调制解调器的手机都将自动支持所有 LTE 频段。设备制造商选择在其设备上仅支持某些 LTE 频段，即使调制解调器支持更多频段。从 FDD-LTE 到 TDD-LTE，越来越多使用全球 LTE 频段的手机进入市场。然而，预算和许多中档手机仍然选择禁用许多 LTE 频段。

至于为什么大多数开箱即用的设备上没有启用更多 LTE 频段的问题，这与认证有关。设备制造商必须对他们的设备进行认证，才能在特定的频率上发送无线电信号。这需要大量的测试，这意味着需要钱。例如，如果小米不打算在北美推出[小米 Mi A2](https://www.xda-developers.com/xiaomi-mi-a2-review/) ，为什么它要认证这款手机使用大多数手机用户永远无法使用的美国 LTE 频段？这种方法将节省设备制造商的资金，并且在大多数情况下，节省下来的资金将传递给消费者。

另一个因素是，电话可能需要在电话中添加额外的硬件来支持某些频率的更宽覆盖范围，即使调制解调器支持这些特定的频率。高通拥有自己的射频前端(RFFE)解决方案。手机，尤其是 5G 手机，将需要基带、收发器和前端的端到端解决方案。RFFE 模块[可以在高通的网站](https://www.qualcomm.com/products/rf)上看到。**这完全是关于成本**，特别是在预算和低端中档手机中，设备制造商很容易做出决定，减少可用的 LTE 频段数量。

## iQOO 3 的 5G 和 4G 版本背后的基本原理

那么，为什么即将推出的 iQOO 3 有 5G 和 4G 两种版本呢？iQOO 是第一家制造 5G 和 4G 版本骁龙 865 手机的设备制造商，但我怀疑它不会是最后一家。第一个问题是:iQOO 是如何做到这一点的？我们得到的信息是，这款手机将采用骁龙 X55 调制解调器，支持 5G。**因此，iQOO 必须专门禁用 X55 调制解调器的 5G 功能，以纯粹为 4G LTE 和传统网络提供连接。**

鉴于上述认证信息，iQOO 将开发一款支持 5G 的独立 4G 手机的最可能原因是成本。设备制造商不需要为低于 6GHz 的 5G 频率认证设备。它可以通过认证必要的 4G LTE 频率来完成这项工作，并在市场上销售手机。缺少 5G 认证带来的成本节约将传递给消费者，从而使其成为一款负担得起的骁龙 865 动力旗舰产品。

**要知道印度还没有 5G 网络，这一点很重要。**目前，5G 网络在印度铺开还有很长的路要走。[必须牢记电信提供商](https://www.xda-developers.com/india-reliance-jio-airtel-vodafone-idea-telecom-carrier-monopoly-uncertain-future-agr-judgment/)的财务状况。即使抛开这一点(如果我们只考虑 Jio)，5G 试验仍有待完成，尽管[华为已被允许参与 5G 试验](https://www.zdnet.com/article/huawei-allowed-to-enter-5g-trial-phase-but-will-it-be-allowed-to-win/)，但它在印度 5G 网络中的全部角色仍有待完全确定。5G 频谱拍卖可能在今年年底举行，或者更有可能的是，它们将再次推迟到 2021 年。在这种情况下，5G 网络在印度铺开的最早时间框架将是在 2021 年底，或者更有可能是在 2022 年初至年中。到那时，iQOO 3 将近两年了，从而否定了它作为“印度第一款 5G 手机”的卖点。

我想到了另一个问题:如果印度在很长一段时间内都不会有 5G 网络，那么为什么还要在印度销售 5G 变体呢？可能的答案是为了营销利益。“印度第一部 5G 手机”是一个很好的口号，Realme 和 iQOO 都在争夺它。这种区别的实际相关性可以忽略不计，还有一点是，iQOO 3 5G 版本的用户将能够在几年后上线时使用印度的第一个 5G 网络。现在，它没有任何好处。另外，三星知道这一点，这就是为什么它在印度只推出了 Galaxy S20 系列的 4G 版本，价格略低于欧洲 5G 或美国 5G 版本的价格。 [Exynos 990](https://www.xda-developers.com/samsung-exynos-990-5g-modem-5123-7nm/) SoC 支持分立的 Exynos 5G 调制解调器 5123，三星很可能会像 iQOO 一样，在 5G 网络尚不存在的市场上禁用调制解调器的 5G 功能。

在我看来，iQOO 和三星做出了明智的决定。iQOO 还决定在印度销售 iQOO 3 的 5G 版本，这一决定的作用有限，尽管我们只有在了解两种版本的定价后才能更好地理解这一点，这将在发布会上公布。在 iQOO 看来，4G 型号是基本型号，而 5G 型号将被定位为额外收费的高级专业型号。这种策略会奏效吗？我们正密切关注市场，看故事如何发展。