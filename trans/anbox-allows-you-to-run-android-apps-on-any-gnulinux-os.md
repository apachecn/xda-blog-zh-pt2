# Anbox 允许你在任何 GNU/Linux 操作系统上运行 Android 应用

> 原文：<https://www.xda-developers.com/anbox-allows-you-to-run-android-apps-on-any-gnulinux-os/>

由于谷歌 Android 的广泛扩散，开发人员蜂拥至该平台，为其创建了数百万个应用程序。尽管 Android 基于 Linux 内核，很像桌面 GNU/Linux 操作系统，但是桌面操作系统并没有吸引到类似的开发工作。这并不是说 GNU/Linux 操作系统是失败的(我在自己的机器上运行 Ubuntu 16.04)，但有时你希望可以在另一个平台上快速访问适用于一个平台的应用程序。我说的快速是指无需设置虚拟机，通过 [Android-x86](http://www.android-x86.org/) 项目进行双引导设置，或者使用那些远程桌面解决方案之一。谢天谢地， **Anbox** 是[来解决那个](https://mm.gravedo.de/blog/posts/2017-04-10-introducing-anbox/)的。

代表“Android in a Box”的 Anbox 是一个[开源项目](https://github.com/anbox/anbox)，它允许你在 Linux 桌面上运行 Android 应用，而没有虚拟机、双引导或远程桌面的麻烦。它通过将 Android 操作系统放入一个 [Linux 容器(LXC)](https://linuxcontainers.org/) 来实现这一点，这允许它共享内核(这意味着没有仿真)，但使用 Linux 名称空间将主机环境与 Android 操作系统隔离开来。因此，Anbox 不允许任何直接的硬件访问，而是将开放的 GL ES 桥接到主机，例如图形子系统。

目前处于 alpha 状态，Anbox 并非没有漏洞和崩溃，但从上面的视频中，你可以清楚地看到，它允许快速轻松地访问基于 Android 7.1.1 牛轧糖平台的 Android 应用程序。如您所料，谷歌 Play 商店没有附带该软件，但是可以通过运行`adb install /path/to/.apk command`从主机环境安装应用程序。

安装 Anbox 非常简单，因为它可以在任何支持安装[快照](https://snapcraft.io/)的 GNU/Linux 发行版上工作。Snaps 允许 Anbox 将所有依赖项打包到一个 zip 文件中，这样您就不必担心自己手动安装所有东西。然而，你需要在你的机器上有超级用户权限，因为安装程序脚本需要安装某些内核模块，比如 [DKMS](https://en.wikipedia.org/wiki/Dynamic_Kernel_Module_Support) 。

* * *

### 安装机箱

如果您的计算机支持安装快照，那么您只需运行以下命令:

```
 sudo snap install  
```

* * *

### 支持 Anbox

由于这是一个开源项目，任何开发者都可以通过关注项目的 [Github 页面](https://github.com/anbox/anbox/blob/master/README.md)为项目做出贡献。可以在 [FreeNode](https://freenode.net/) 网络的#anbox IRC 频道或者他们的 [Telegram 聊天群](https://t.me/joinchat/AAAAAEIxawINNSiXmEMdGg)上找到 Anbox 开发者。bug 可以在他们的 [Github 问题页面](https://github.com/anbox/anbox/issues/new)上报告。