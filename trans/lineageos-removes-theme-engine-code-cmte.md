# LineageOS 开始删除主题引擎相关代码，基本上确认 CMTE 的灭亡

> 原文：<https://www.xda-developers.com/lineageos-removes-theme-engine-code-cmte/>

# LineageOS 开始删除主题引擎相关代码，基本上确认 CMTE 的灭亡

作为 LineageOS 15 bringup 的一部分，旧的 CyanogenMod 主题引擎(CMTE)在大多数提及被从代码中删除后最终被永久删除。

在底层崛起之前，就有了 CyanogenMod 主题引擎(CMTE)。早在 CyanogenMod 9(基于 Android 冰淇淋三明治)中就引入了，它为 CyanogenMod 版本添加了系统范围的主题功能。随着 CyanogenMod 14(后来成为[linegeos](https://www.xda-developers.com/the-death-of-cyangenmod-and-whats-in-store-for-the-future/))的发布，CMTE 无处可寻。与此同时，许多其他流行的定制 rom 开始青睐基于 OMs 的底层主题引擎。随着 Android 8.0 奥利奥现在包括[本地 OMS 支持](https://www.xda-developers.com/andromeda-substratum-custom-themes-oreo/)，LineageOS 团队似乎已经永远退出了 CMTE。

我们早些时候就已经从一个消息来源那里听说 CMTE 基本上已经死了，但是一些用户仍然有一丝希望，有一天它会以线性地理的形式回归。唉，事实似乎并非如此:作为 LineageOS 15.0 bringup 的一部分，CyanogenMod 主题引擎的核心，以及所有提到的主题引擎都在从源代码中移除的过程中[。这个改动终于在 10 月 12 日提交了，基本标志着 CyanogenMod 主题引擎的死亡。](https://review.lineageos.org/#/c/190239/)

对于那些希望给自己的设备添加主题的人来说，下一步会是什么？LineageOS 团队完全有可能开发他们自己的主题引擎，但可能性不大。毕竟，甚至一些原始设备制造商([三星，例如](https://www.xda-developers.com/sungstratum-samsung-substratum-touchwiz/))也支持 RRO 或 OMS。

Substratum 在过去几年里越来越受欢迎，自从索尼从运行时资源覆盖(RRO)转移到[覆盖管理器服务](https://www.xda-developers.com/layers-manager-is-being-deprecated-in-favor-of-substratum/) (OMS)以来，它的主题框架变得越来越好。因此，底层现在已经取代了 CMTE 的大部分定制 rom。更重要的是，如果你想给你的安卓奥利奥设备添加主题，你很幸运，因为奥利奥本身就支持 OMS。这意味着你将能够在任何设备上[使用没有根的底层](https://www.xda-developers.com/custom-themes-android-oreo-substratum/)——包括 LineageOS 15。