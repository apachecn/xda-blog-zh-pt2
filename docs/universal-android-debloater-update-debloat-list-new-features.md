# 通用 Android 去模糊器获得了主要的去模糊列表更新和一些新功能

> 原文：<https://www.xda-developers.com/universal-android-debloater-update-debloat-list-new-features/>

# 通用 Android 去模糊器获得了主要的去模糊列表更新和一些新功能

通用 Android 去模糊器的最新更新带来了一个主要的去模糊列表更新，一些新功能和一些 UI 变化。

在二月份推出通用 Android 解包程序 v0.4.0 后，XDA 成员 [w1nst0n_fr](https://forum.xda-developers.com/m/w1nst0n_fr.10413801/) 现在发布了 shell 脚本的最新更新。最新的更新(v0.5)带来了一个主要的去模糊列表更新，一些新功能，以及几个较小的 UI 更改和改进。

对于不知情的人来说，Universal Android Debloater 是一个 shell 脚本，它利用社区维护的 OEM 和特定于运营商的膨胀软件列表来实现无缝解包。这是一个方便的工具，对于那些希望通过一次点击清除所有 OEM 和运营商特定的膨胀软件的 Android 手机。

随着最新的更新，Universal Android Debloater 的 debloat 列表已经获得了对一系列新软件包的支持。此次更新还带来了一些微小的用户界面变化，新的取消全选和重启按钮，以及对取消声明列表的远程下载支持。请查看以下部分，了解完整的通用 Android 版本 0.5 变更日志。

**通用安卓解包器 v0.5 变更日志**

*   **应用程序**:
    *   在推荐列表中添加了 com.tblenovo.lenovotips。
    *   将 Google 键盘移至高级列表(默认键盘不应在推荐列表中)
    *   将 com.android.htmlviewer 移至专家列表。移除它引导 MIUI 12.5.4+上的设备。
*   **去块列表更新**:
    *   添加了一堆新包
    *   大量的描述更新和修正
    *   根据更加一致的标准对建议进行重大修订
*   **增加了**:
    *   取消全选按钮:让您取消选择您在屏幕上看到的所有软件包(即在当前过滤列表中)。
    *   重新启动按钮:让您快速重新启动当前选定的设备。
    *   远程 uad_lists.json 下载:现在，当您启动 uad 时，可以直接从这个 repo 的主分支获取解包列表。这意味着不再需要发布新版本的 UAD 来更新去保列表！
    *   UAD 自我更新:UAD 现在会在发布时检查是否有自己的新版本，并让您直接从应用程序执行更新！
*   **变更**:
    *   UAD 现在每 500 毫秒(1 分钟)尝试启动一次 ADB 连接，直到在查找电话加载状态期间找到设备。
    *   所有的初始化过程都被重写，并且在每个阶段(下载列表、查找电话、加载包、更新语言和就绪)都显示一条状态消息，这样你就知道发生了什么。
    *   较小的用户界面更改
*   **包装**:
    *   为 MacOS 和 Linux 添加非自更新版本。如果 UAD 分布在存储库中，这将非常有用。更新过程将由包管理器管理。
    *   MacOS 构建现在也以压缩的 tarball 形式发布(像 Linux 一样)。您不再需要手动添加可执行权限。

如果你刚刚给自己买了一部新手机，并想让它摆脱所有预装的膨胀软件，你可以按照下面链接的 XDA 论坛帖子中提供的说明，尝试一下通用的 Android 解封层脚本。尽管该脚本为您提供了一个单击即可从设备中删除所有膨胀软件的选项，但我们建议您在使用该脚本删除软件包时谨慎行事，否则您可能会遇到一些不必要的问题。

**[通用安卓解封器 XDA 线程](https://forum.xda-developers.com/t/script-2021-01-30-v2-9-universal-android-debloater.4069209/)**

如果你不习惯使用这个脚本，你可以按照我们的指南中提供的说明[卸载运营商/OEM 膨胀软件，而不需要 root 访问权限](https://www.xda-developers.com/uninstall-carrier-oem-bloatware-without-root-access/)从你的手机中删除预装的应用程序。

* * *

**来源:** [GitHub](https://github.com/0x192/universal-android-debloater/releases/tag/0.5)

**Via:**Reddit