# 未来的 ARM 大核心 CPU 将不再支持 32 位应用

> 原文：<https://www.xda-developers.com/future-arm-cpu-drop-support-32-bit-apps/>

2020 年 5 月，ARM 宣布了其 2020 年 CPU 阵容，包括 [ARM Cortex-A78](https://www.xda-developers.com/arm-announces-cortex-a78-cpu-mali-g78-gpu-ethos-n78-npu/) A 系列 CPU 内核和新的 [ARM Cortex-X1](https://www.xda-developers.com/arm-announces-cortex-x-custom-cpu-program/) 内核，这是 Cortex-X 定制 CPU 计划下的第一款产品。新内核还没有进入任何运输设备——用户必须等到 2021 年初才能看到采用新 IP 的手机。这就是 ARM 宣布其新产品的方式:2019 年 5 月宣布的 [ARM Cortex-A77](https://www.xda-developers.com/arm-cortex-a77-cpu-announcement/) CPU 核心，直到 2020 年 2 月才开始发货。ARM Cortex-A78 和 Cortex-X1 与其前辈一样是 64 位内核，但它们也支持旧的 32 位应用程序。不过，ARM 现在已经证实，这种情况将会改变。未来的 ARM 大内核，包括 Cortex-A 和 Cortex-X CPU 内核，将从 2022 年开始变为 64 位。

这一声明是由 ARM 公司副总裁兼客户业务总经理保罗·威廉姆森在 ARM DevSummit 主题演讲中宣布的(通过 [*AndroidAuthority*](https://www.androidauthority.com/arm-64-bit-1165264/) )。这一消息意味着未来将不再有硬件支持旧的 32 位应用程序。

然而，这对绝大多数应用来说不应该是坏消息。这是因为[谷歌要求自 2019 年 8 月以来提交给 Google Play 的](https://www.xda-developers.com/google-play-stop-serving-native-apps-without-64-bit-cpu-support/)应用必须是 64 位的。ARM 还指出，大约 60%的应用已经兼容 64 位。大多数不是 64 位的应用不属于西方生态系统。对于应用程序开发人员来说，有足够的时间来更新他们的旧应用程序，考虑到 2022 年宣布的 CPU 核心可能要到 2023 年初才能上市。然而，如果 32 位应用程序不再更新，这一声明意味着它将停止在 64 位设备上运行，这些设备将推出未来的 ARM Cortex-A 内核。

Android 本身已经是 64 位了，因为该操作系统早在 2014 年 5.0 版 Lollipop 中就引入了 64 位支持。然而，Android 和 ARM 的 CPU 内核继续支持 32 位应用程序，这意味着 Android 截至目前并不是一个仅 64 位的操作系统，不像 iOS 那样，在 2017 年随着 iOS 11 的推出，只支持 64 位。32 位应用程序的传统支持将在 2022 年从硬件部分结束，预计谷歌将在未来版本的 Android 中取消 32 位应用程序支持。如前所述，这对于最终用户来说应该是不可见的。

迁移到 64 位有什么好处？其中包括操作系统、应用程序和游戏的性能提升，在某些情况下提升了 20%。这对开发人员来说也更容易，因为他们不必支持两个二进制文件。他们可以专注于优化单个 64 位二进制文件，这可能意味着更快的更新时间。

对于 ARM 来说，这一消息意味着它可以从其 CPU 设计中去除额外的硅，因为它需要这些硅来支持传统的 32 位技术。这可以节省硅面积，这意味着在相同的芯片尺寸下可以有更强大的 CPU。ARM 的 2021 和 2022 Cortex-A CPU 分别代号为 Matterhorn 和 Makalu。Makalu 将会转换到 64 位。ARM 承诺在今年发布的 Cortex-A78 和 Makalu 之间将性能提高 30%，因为该公司继续推进其 CAGR(复合年增长率)。

向专用 64 位的过渡将从大 CPU 核心开始，其中可能包括 Cortex-X 系列，尽管 ARM 没有具体说明它们。2017 年宣布的 [Cortex-A55](https://www.xda-developers.com/arm-unveils-cortex-a75-a55-processors-and-mali-g72-gpu/) “小核心”是 32 位/64 位设计，其继任者可能于明年推出，仍将支持 32 位传统应用。因此，最终结果将是一种 CPU 集群设计，它将仅 64 位的 Makalu 与更小的 32 位/64 位小内核(如 Cortex-A55 的继任者)混合在一起。然而，从开发者和用户的角度来看，最终产品将是 64 位的。Cortex-A55 的继任者可能会在更长时间内支持 32 位，但对于使用 Makalu 驱动设备及更高设备的用户来说，这将无关紧要。ARM 还将在 Cortex-M 和 Cortex-R 系列 CPU 中保持 32 位支持。

因此，Android 向 64 位的独家转移将在 iOS 于 2017 年完成向 64 位的过渡后大约五年发生。同样，除了性能提高的好处之外，所有这些都不会对最终用户产生太大影响。在基于 ARM 的 Makalu CPU 的设备到来之前，应用程序开发人员有责任用 64 位支持更新他们所有的传统应用程序。