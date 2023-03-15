# 放大，曝光模块阻止唤醒锁/警报和节省电池，为牛轧糖更新

> 原文：<https://www.xda-developers.com/amplify-xposed-module-block-wakelocks-save-battery/>

在 Android 7.0 牛轧糖推出之前，Xposed 框架最受欢迎的模块之一是 Amplify。简而言之，Amplify 是一个开放的模块，允许用户完全控制 Android 设备上的唤醒锁和闹钟。由于它能够控制一些最糟糕的系统唤醒锁，如 NlpWakelock 和 NlpCollectorWakeLock，Amplify 已被证明可以显著提高电池寿命。当用户升级到 Android Nougat 并留下 Xposed 时，它和 GravityBox 是最令人遗憾的功能之一。现在 [Xposed 框架已经更新为完全支持 Android Nougat (7.0/7.1)的](https://www.xda-developers.com/official-xposed-framework-android-nougat/)，不过，Amplify 现在也这样做了，并与 Xposed 的最新版本兼容。

这个由 XDA 资深成员 cryptyk 开发的工具已经升级到 4.0.0，因为它带来了两个关键的变化。首先，它现在已经获得了 Android Nougat 的官方支持，这意味着 7.0/7.1 Xposed 用户现在可以利用 Amplify 来优化手机的电池性能。此外，SELinux 对唤醒锁、服务和警报的支持也在此更新中提供。开发者表示，不会放弃对 Lollipop 和 Marshmallow 的支持，因为这款应用旨在为所有人服务，这意味着那些仍在使用旧版本 Android 的人不必担心他们的设备会随着这一版本而被放弃。

如果你正在使用棒棒糖、棉花糖或牛轧糖，你应该前往[XDA 官方论坛线程](https://forum.xda-developers.com/showpost.php?p=74244791&postcount=7715)下载最新版本，并找出你可能想要阻止的唤醒锁、闹钟和服务。开发人员也活跃在那个线程上，所以一定要留下来！请注意，为了在您的设备上使用 Amplify，您显然需要最新版本的 Xposed 框架和 Xposed 安装程序。我们在 YouTube 频道上有一个关于如何安装 Xposed 的教程。

此外，这是第一次官方牛轧糖发布，它确实可能会有错误。然而，这些问题将随着时间的推移得到解决。这是当年使用最广泛的 Xposed 模块之一，所以我们很高兴看到它全面回归。