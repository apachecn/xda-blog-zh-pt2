# 骁龙三星 Galaxy Note 9 的 Root 方法已经找到

> 原文：<https://www.xda-developers.com/samsung-galaxy-note-9-proof-of-concept-root/>

# 骁龙三星 Galaxy Note 9 的概念验证根方法已经找到

感谢论坛主持人/公认的开发者 Elliwigy，我们现在有了骁龙三星 Galaxy Note 9 的概念证明。

北美的三星手机被锁定引导程序困扰的时间最长。这意味着没有 TWRP，没有稳定的根，没有只读存储器。幸运的是，过去一些伟大的开发人员已经能够找到解决办法，Galaxy S7、Galaxy S8 和 Galaxy Note 8 都有不稳定但工作正常的 root。这在 Galaxy S9 上停止了，因为三星对他们当时的三星体验系统做了很多改变，使它变得不可能。感谢论坛主持人/公认的开发者 [Elliwigy](https://forum.xda-developers.com/member.php?u=3812611) ，我们现在有了一个使用三星工厂二进制文件的骁龙 Galaxy Note 9 的概念证明。

大多数以前的三星设备都需要在引导加载程序中利用漏洞或漏洞，允许通过 Odin 刷新修改的文件。这个最新的根目录使用修改过的 init 脚本，这些脚本放在最新的 Samsung 工厂二进制文件中的一个可读/可写文件夹中。这允许 elliwigy 向系统中注入 SuperSU 和 busybox。本质上，这意味着您获得了一个完全根化的工厂二进制文件。这个问题是工厂二进制本身。

三星用于测试硬件和修复软件的工厂二进制固件。它没有一个完全正常工作的调制解调器、谷歌服务、电话拨号器、消息应用或任何其他使手机成为手机的应用。使用工厂二进制文件意味着您失去了使这个根目录有用的大多数特性。这就是为什么这是一个概念证明。Elliwigy 说他“发布它是希望一些更有经验的开发人员能够知道如何扎根于股票。”Elliwigy 希望开发人员在股票系统的这个根上工作，以便它可以变得实际有用，而不仅仅是概念证明。

北美三星用户的 Root 总是很难获得。任何接近完整根的东西都让我们对三星的发展前景充满希望。如果您愿意安装并测试这个根客户端，Elliwigy 有关于如何在您自己的设备上安装它的说明。有必要重申一下，这是不稳定的，不是日常使用的。这应该是专门用于开发的。

[**骁龙三星 Galaxy Note 9 根线**](https://forum.xda-developers.com/galaxy-note-9/samsung-galaxy-note-9-snapdragon-roms-kernels-recoveries--other-development/root-t3927413)