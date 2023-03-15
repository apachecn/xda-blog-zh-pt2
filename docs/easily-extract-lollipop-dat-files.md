# 轻松提取棒棒糖 Dat 文件

> 原文：<https://www.xda-developers.com/easily-extract-lollipop-dat-files/>

# 轻松提取棒棒糖 Dat 文件

本指南向您展示了如何以最简单的方式提取棒棒糖文件。

随着 Android 的每一次迭代，我们最喜欢的移动操作系统不断扩展，ROM 大小也逐渐增加。除此之外，原始设备制造商添加的膨胀软件通常会将 rom 的大小增加到千兆字节或更多。下载这么大的固件是有问题的，尤其是在数据传输速度有限的国家。为了让最终用户的生活更轻松，Google 决定使用可压缩的 EXT4 文件系统，它取代了提取的分区。虽然它在许多方面被证明是有益的，但对某些用户来说也有一些潜在的缺点。

在 Android 5.0 之前，像 OmniROM 和 AOKP 这样的定制 ROM 都是以 ZIP 存档的形式发布的。它们很容易修改，每个对 ROM 改造感兴趣的人都可以添加一个应用程序，bootanimation，或者几乎任何不需要太多工作的东西。Lollipop 更难修改，因为开发人员需要闪存 ROM 并进行 NAND 备份以获得 img 文件，或者使用 sdat2img 等外部工具。Linux 用户可以使用中国开发者 howellzhu 创建的 sdat2img 工具轻松提取 DAT 文件。这个二进制文件允许用户将 DAT 文件提取到 EXT4 映像中，然后可以轻松地挂载或提取。

XDA 公认的贡献者 [xpirt](http://forum.xda-developers.com/member.php?u=5132229) 写了一个指南，详细解释了棒棒糖 rom 的解压过程。该指南包含关于使用 sdat2img 工具的有用信息，并解释了 Google 在相关源文件中使用的技术术语。希望这个指南将帮助开发者更容易地提取 rom，从而创建你正在使用的固件的修改版本。

要阅读这条有用的信息，请前往[【如何】解压棒棒糖。dat 文件论坛线程](http://forum.xda-developers.com/android/software-hacking/how-to-conver-lollipop-dat-files-to-t2978952)的相关位。