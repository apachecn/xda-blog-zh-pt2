# Halium 是一个开源项目，致力于非 Android 移动操作系统的公共基础

> 原文：<https://www.xda-developers.com/halium-is-an-open-source-project-working-towards-a-common-base-for-non-android-mobile-operating-systems/>

如果你是一个 Android 发烧友，也探索过纯基于 Android 的定制 rom 的世界，你可能听说过 Ubuntu Touch、Sailfish OS 等项目。

这些都是雄心勃勃的，通常是长期运行的非 Android、基于 GNU/Linux 的移动操作系统。然而，碎片化使得这些替代操作系统的开发和用户采用变得非常困难...但这正是项目 Halium 的用武之地。

这个开源项目试图汇集来自 Ubuntu Touch ports、Sailfish OS 社区开发者、open webOS Lune OS 项目和 KDE 等离子移动贡献者以及其他开发者(我们怀疑是 Jolla)的开发者来**结束在他们各自项目的底层基础上看到的碎片化**。目前，Ubuntu Touch、Sailfish OS/Mer、Plasma Mobile 和其他软件使用不同的 Android 源代码树和方法来构建不同的堆栈。这导致最流行的非 Android、基于 GNU/Linux 的移动操作系统项目在使用 Android 源代码树、如何启动 Android init 以及如何将映像闪存到设备上时出现了很多碎片。这些项目中的许多本质上做同样的工作，但是以不同的方式。

理想情况下，这些部分不应该是分开的，因为所有这些操作系统最终都有相同的目标——在使用 Android 二进制驱动程序的同时进行引导。因此，Halium 的目标是建立一个通用的 Linux 基础，然后所有这些不同的项目都可以使用它在各自的手机上启动。这意味着**标准化 Linux 内核构建和 Android HAL** (硬件抽象层) *libhybris* 以支持 Android 驱动程序，然后拥有一套标准的用户空间组件。在那之后，高层的接口决策就留给了单个项目自己，但是低层的基础将被共享。

这种方法有相当多的好处，可以帮助所有非 Android、基于 GNU/Linux 的移动操作系统项目。共享移植工作将实现一个简化的 HAL，其他发行版将更容易在移动设备上运行。一旦建立了基础，各个项目之间的交流也就有了“共同点”。这是一个雄心勃勃的项目，分为几个阶段，首先是对 *libhybris* 的初步开发，然后是启用硬件(做好准备)，最后是启用设备(扩展并包括参考谷歌 Nexus 5、OnePlus One 和谷歌 Nexus 5X 之外的新设备)。

如果你想了解更多或参与这个项目，有各种方法可以联系。可以通过 freenode IRC 加入#halium 进行讨论；可以去看看 Halium Telegram [超群](https://t.me/halium)；或者最后可以用 Matrix (#halium:dishroot.org 或者#halium:matrix.org)聊天。虽然该项目仍处于早期阶段，但仍然值得一试。我们一定会密切关注它的进展，并希望它最终能惠及这些移动操作系统的替代品！