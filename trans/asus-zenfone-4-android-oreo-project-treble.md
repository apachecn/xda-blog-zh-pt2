# 华硕 Zenfone 4 Android Oreo 更新带来项目三重支持，无需单独的供应商分区

> 原文：<https://www.xda-developers.com/asus-zenfone-4-android-oreo-project-treble/>

# 华硕 Zenfone 4 Android Oreo 更新带来项目三重支持，无需单独的供应商分区

华硕 Zenfone 4 已经获得了 Project Treble 支持，但华硕的实现并没有使用单独的供应商分区来存储设备 BLOBs。

自 Android Oreo 推出以来，对 Android 手机制造商的一个主要批评是未能支持 Project Treble，这是谷歌的模块化升级计划，有可能以以前无法想象的方式帮助定制 ROM 的开发。有了 Project Treble，[单个系统映像可以跨多个设备引导](https://www.xda-developers.com/stock-android-oreo-huawei-mate-9-project-treble/)，所以有些人对并非所有 OEM 都支持它感到失望也就不足为奇了。诺基亚和一加都声称他们的设备没有必要的分区——这是一个合理的借口，因为 Project Treble 要求 a /vendor 分区来容纳所有的设备[**B**inary**L**arge**Ob**object(blob)](https://developer.android.com/reference/java/sql/Blob.html)。但是华硕没有让这阻止它为华硕 Zenfone 4 发布基于 Android Oreo 的更新，该更新带来了 Project Treble 支持**而没有**单独的供应商分区。

现在，它不是迄今为止出现在其他设备上的同类项目 Treble。事实上，对于定制 ROM 开发来说，它远不如华为 Mate 9 的 Project Treble 实现有用。由于华硕选择不使用/vendor 分区，设备 BLOBS 存储在/system 分区中，这意味着不可能在 Zenfone 4 上创建一个可以在其他华硕设备上引导的单一系统映像。不过，这并不意味着定制 ROM 开发者不会从中受益——华硕 Zenfone 4 设备 BLOBS 现在已经标准化，定制 ROM 开发者现在可以采用与创建单一系统映像相同的方法来开发 ROM——他们只是将二进制对象合并到系统分区中。

虽然华硕对 ZenFone 4 的 Project Treble 支持不会帮助开发人员为所有设备创建通用的系统映像，但它将有助于手机的定制 ROM 开发，并使华硕在未来更容易升级。

## 更新:更多上下文

对于定制 ROM 开发者来说，华硕的 Project Treble 支持在某些方面应该会让事情变得容易很多。虽然 Project Treble 的最佳部分将允许相同的系统映像在任何设备上启动，但没有此分区但仍然“三倍化”其 BLOBs 的设备，也就是说，仍然可以在任何 Project Treble 支持的 Android 版本上使用，无论是否有/vendor 分区，只要进行必要的调整。

* * *

[**来源:ZenTalk 论坛**](https://www.asus.com/zentalk/forum.php?mod=viewthread&tid=192112&page=2#pid746921)