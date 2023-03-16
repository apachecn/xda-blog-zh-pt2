# 有可能在 Chromebooks 上安装 Android 子系统

> 原文：<https://www.xda-developers.com/root-android-subsystem-chromebooks/>

几年前，Chrome OS 获得了对 Android 应用程序的支持。因此，Chromebooks 有一个功能正常的 Android 子系统，可以运行 Android 应用程序，运行 ADB shell 等。(这与允许 [Linux 应用在 chrome book](https://www.xda-developers.com/stable-linux-apps-chrome-os-69/)上运行的新功能是分开的。)Android 最著名的一个特点就是可以 root，允许用户获得/system 的完全访问权限。由于 Github 上的 aroc 项目，也可以将 Android 子系统植根于 Chromebooks 上。

开发者 nolirium 的 aroc 项目在 Chrome OS 上带来了 Android root。它通过提供 Chrome OS shell 脚本来制作 Android 容器的读/写副本，并在其中复制 su。这意味着 root 应用现在可以在 Chromebooks 上的 Android 子系统中工作，Xposed 也可以工作。

开发人员指出，这些脚本已经在 Chrome OS 版本 54-67 上进行了测试。运行脚本的先决条件是:

*   Chrome OS 设备，支持 Android 应用程序，在/usr/local 中有大约 2GB 的存储空间。设备必须处于开发者模式。此外，Chrome OS 系统分区需要是可写的，也就是说，需要禁用 rootfs 验证。
*   可以通过运行以下命令，然后重新启动来禁用 Rootfs 验证:

```
 sudo /usr/share/vboot/bin/make_dev_ssd.sh --remove_rootfs_verification --partitions $(( $(rootdev -s | sed -r 's/.*(.)$/\1/') - 1)) 
```

## **运行脚本的指令**

用户需要在 Chrome OS shell 中运行一个组合脚本，它会自动下载并提取所需的文件。运行脚本后需要重新启动。

```
 curl -Ls https: 
```

然后，用户应该重新启动，并打开 Root Checker 等应用程序来验证 Root 的存在。如果组合脚本不起作用，他们可以手动运行命令来运行脚本 1 和脚本 2。在这种情况下，运行脚本 1 和脚本 2 后都需要重新启动。

```
 curl -Ls https: 
```

```
 curl -Ls https: 
```

开发者指出，Chrome OS 版本的更新通常会覆盖任何 rootfs 定制，包括那些由脚本执行的定制。从 SuperSU GUI 应用程序中更新 su 二进制文件也可能不起作用。

该脚本的当前版本用一个符号链接替换了原始的 Android 系统映像。如果用户需要恢复到原始(非根)映像，他们将不得不手动恢复备份(据开发人员称，这是最简单的选项)，或者强制更新，例如更换频道，或者从 USB 恢复。

用户可以参考[开发者在这里的说明](https://nolirium.blogspot.com/)使用这个脚本在 Chrome OS 上安装 Xposed。

* * *

[**来源:nolirium 的 Github**](https://github.com/nolirium/aroc) [**来源二:开发者博客**](https://nolirium.blogspot.com/2016/12/android-on-chrome-os-rooting-shell.html)