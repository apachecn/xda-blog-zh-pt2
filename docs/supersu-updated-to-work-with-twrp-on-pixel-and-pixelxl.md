# SuperSU 已更新，可与 TWRP 一起处理 Pixel 和 Pixel XL

> 原文：<https://www.xda-developers.com/supersu-updated-to-work-with-twrp-on-pixel-and-pixelxl/>

# SuperSU 已更新，可与 TWRP 一起处理 Pixel 和 Pixel XL

根据 Chainfire 的 Google+帖子，SuperSU 刚刚更新，可以与谷歌 Pixel 和 Pixel XL 上的最新 TWRP alpha 一起工作。

昨晚，谷歌 [Pixel](http://forum.xda-developers.com/pixel) 和 [Pixel XL](http://forum.xda-developers.com/pixel-xl) 发布了 TWRP 的第一个 [alpha 版本。我们深入研究了该版本的许多细节，包括安装过程的变化以及新的和坏的内容。我们在文章中提到的一个警告是，安装 TWRP 会导致 SuperSU 不再运行。](http://www.xda-developers.com/twrp-has-been-released-for-the-google-pixel-and-pixel-xl/)

> #### 如果您目前是根用户，此时安装 TWRP 将删除根用户。需要升级超级苏才能让 TWRP 和超级苏共存。

正如我们在文章的附录中解释的那样，安装 TWRP 将删除 root 的原因是因为 Dees_Troy 允许 TWRP 解密数据分区的方法涉及修改由 Chainfire 修改的相同的 init 二进制文件以实现无系统 root。因此，通过安装 TWRP，SuperSU 对 init 二进制文件所做的更改将被覆盖。为了不引起任何冲突，Chainfire 自己建议，如果你目前运行 SuperSU 并计划安装 TWRP，你需要首先从工厂镜像刷新股票引导镜像。两家开发商一直在就如何解决这一冲突进行接触，今天 Chainfire 发布了 **SuperSU v.278 SR4** ，其中**为两款谷歌 Pixel 手机修复了这一问题**。

在更新中，Chainfire 提到这次更新将允许 SuperSU 在 TWRP(T1)的上面闪现(而不是在 T3 的上面闪现 T2)。他的引导至根脚本现在将不再与 TWRP 所做的 init 二进制更改相冲突，但在 TWRP 更新之前，相反的情况不会发生。所以现在，你将需要**首先安装 TWRP** 和**，然后一旦你在恢复环境中闪存 SuperSU** 。当然，这是假设你想同时拥有超级苏和 TWRP。重申一下，如果你已经安装了 SuperSU，并且现在也想安装 TWRP，你需要首先刷新引导镜像，然后安装 TWRP，最后在 TWRP 重新安装 SuperSU。

* * *

这就是此次更新的主要内容。请点击下面的链接查看 Chainfire 的完整安装说明以及下载链接。

[**来源:Chainfire (Google+)**](https://plus.google.com/+Chainfire/posts/CBL8pnKtA8F)