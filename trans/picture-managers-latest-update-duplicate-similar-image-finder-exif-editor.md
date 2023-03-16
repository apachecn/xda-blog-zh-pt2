# 图片管理器的最新更新添加了重复和相似的图像查找器，EXIF 编辑器，等等

> 原文：<https://www.xda-developers.com/picture-managers-latest-update-duplicate-similar-image-finder-exif-editor/>

# 图片管理器的最新更新添加了重复和相似的图像查找器，EXIF 编辑器，等等

图片管理器已经更新的功能，如能够找到重复和类似的照片，一个 EXIF 编辑器与单一和批处理模式，等等！

像 Google Photos 这样的应用程序很大程度上减轻了那些不介意与 Google 分享照片的用户整理照片的痛苦。但是有些用户更喜欢将他们的记忆保存在本地。这就是像 [Picture Manager](https://www.xda-developers.com/auto-timestamp-photos-picture-manager/) 这样的应用程序的用武之地，它允许用户通过自动标记时间戳和以几种不同的方式组织照片来升级他们的组织游戏。我们之前在 2018 年 4 月报道了这款应用，从那以后，这款由 XDA 知名开发商 [j 到 4n](https://forum.xda-developers.com/member.php?u=4905624) 开发的应用已经获得了更新，增加了更多关键功能。

Picture Manager 最近几次更新的变更日志如下:

*   2.0.0 版:
    *   介绍重复和相似图像查找器
        *   使用 crc32 计算查找重复图像
        *   使用 PHash 和 AverageHash 查找相似的图像
        *   计算图像模糊度的选项
    *   为组织者添加了复制而不是移动文件的选项
    *   计数器现在接受要定义的前导零
    *   一些用户界面的变化和修复
*   3.0.0 版:
    *   EXIF 编辑补充道:
        *   单个和批处理模式可用于编辑 149 个 EXIF 属性
        *   有条件的批处理模式
        *   删除所有 EXIF 属性
    *   增加了备份和恢复图片管理器设置的选项
    *   一些用户界面的变化。试图让新用户更容易
    *   更新了 android-gif-drawable 库以修复 CVE-2019-11932

最近更新的主要亮点是找到重复图像和相似图像的能力，以及 Exif 编辑器，它可以在单个编辑模式和批量编辑模式下对多达 149 个 EXIF 属性进行编辑。此次更新还修复了 [CVE-2019-11932](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2019-11932) 中定义的“双免 bug”。

**[图片管理器- XDA 讨论线程](https://forum.xda-developers.com/android/apps-games/app-picture-manager-timestamp-pictures-t3783796)** **[从谷歌 Play 商店下载图片管理器](https://play.google.com/store/apps/details?id=eu.duong.picturemanager)**

* * *