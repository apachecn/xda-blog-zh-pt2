# Chrome OS 80 将开始在新的 Linux 系统上使用 Debian 10 Buster

> 原文：<https://www.xda-developers.com/chrome-os-80-debian-10-buster-linux-installations/>

# Chrome OS 80 将开始在新的 Linux 系统上使用 Debian 10 Buster

从 Chrome OS 80 开始，Chromebooks 上新的 Linux 容器安装将部署 Debian 10 Buster，而不是 Debian 9 Stretch。

在去年的谷歌 I/O 大会上，谷歌[宣布](https://www.xda-developers.com/chrome-os-linux-app-support-google-pixelbook/) Linux 应用支持 Chrome OS。这要归功于在 Linux 容器中安装了 GNU/Linux 发行版，特别是 Debian 9“Stretch”。今年早些时候，Debian 项目[宣布](https://www.debian.org/News/2019/20190706) Debian 10“克星”，但是谷歌[还没有准备好](https://bugs.chromium.org/p/chromium/issues/detail?id=930901)升级 Chromebooks 上的默认 Linux 容器。现在，经过几个月的测试和漏洞修复，谷歌准备将 Debian 10“Buster”作为 Chrome OS 中的默认 Linux 容器。

根据我们在 Chromium Gerrit 中发现的最近合并的提交文件,新的 Crostini(Chrome OS 上 Linux 应用程序的代号)安装将默认获得 Debian 10。该承诺没有提到现有 Debian 9“伸展”安装的 Chromebooks 将如何迁移到新版本，但用户可以通过运行几个命令[轻松升级](https://gitlab.com/ppulfer-random-stuff/debian-buster-in-crostini/blob/master/upgrade_container.sh)容器。升级到 Debian [的新版本会带来新的特性](https://www.reddit.com/r/chromeos/comments/dw9rdi/upgrading_crostini_to_debian_buster_allows_you_to/)，也会带来更好的应用支持。对于真正有进取心的人来说，甚至有可能用 Arch Linux 来代替 Debian 容器。

Chromebooks 上的 Linux 应用支持是谷歌推动 Chrome OS 对开发者更有用的一部分。例如，它使拥有高端 Chromebooks 的开发者能够在 Android Studio 中开发 Android 应用程序。

Chrome OS 80 还将带来对开发者有用的其他变化，如[不启用开发者模式的 Android 应用侧装](https://www.xda-developers.com/google-chrome-os-80-easier-android-app-sideload/)。80 版本目前在金丝雀频道，预计 2020 年 2 月面向所有用户发布。