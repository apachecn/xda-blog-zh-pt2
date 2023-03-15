# 索尼 Xperia XA 超简单生根指南

> 原文：<https://www.xda-developers.com/sony-xperia-xa-ultra-simple-rooting-guide/>

还记得那些日子吗？那时，寻根是一组简单的步骤，任何具有基本计算知识的人都可以遵循。XDA 开发者记得，尤其是 XDA 资深成员 [rrvuhpg](https://forum.xda-developers.com/member.php?u=1461342) 为索尼平板手机 [Xperia XA Ultra](https://forum.xda-developers.com/xa-ultra) 编写了一份非常简单易懂的根操作指南。

每个设备制造商在解放其软件时都有自己的一套怪癖和障碍。虽然索尼在许多场合被贴上了市场上对开发者最友好的原始设备制造商的标签，但它的产品并非没有复杂性。在索尼设备的特殊情况下(大多数/所有设备都是在 2012 年 Xperia Z 之后发布的)，当涉及到解锁时，它们都有一个小小的缺点:虽然大多数设备在解锁时都会失去保修，但索尼更进一步，通过删除 [DRM 密钥](https://android.stackexchange.com/questions/27042/what-exactly-are-drm-keys)，有效地禁用了一些功能(索尼移动专有)。这是我们网站的早期开发者发现的，尽管与索尼移动员工进行了讨论，但这是一种保护公司知识产权的手段。更具体地说，

> 解锁您的 BootLoader 将使您的保修无效，破坏您的设备 DRM，并在拍照时丢失 X-Reality 和弱光下的图像优化。

 <picture>![](img/601516c5f3f3c8a8a609058f756f31e0.png)</picture> 

Device Image Credit: http://cdn2.gsmarena.com/vv/pics/sony/sony-xperia-xa-ultra-3.jpg

自然，root 需要解锁 bootloader，会有擦前述键的副作用。然而，在介绍简单的寻根方法的指南之上，它还包括为了保存 DRM 密钥而要采取的具体步骤，以防有人想要恢复到库存软件配置(出于保修目的或任何其他原因)。这一过程非常简单，它包括在实际解锁之前通过一个名为 TA Backup 的过程备份所述密钥，该过程通过一个由 XDA 公认的开发者 [rayman](https://forum.xda-developers.com/member.php?u=962182) 创建的工具进行。

另一个在寻根过程中遇到的困难是，根据你购买的设备的不同版本，这个指南可能会也可能不会提供寻根功能。背后的原因是，并不是所有的索尼设备都是平等的，因为它们可能带有不可解锁的引导加载程序。所以，给你一个建议，如果你想买一个，并且需要 root，在你花掉你的血汗钱之前，读一读我们的论坛和谷歌一下。

请记住，这个链接的指南只适用于 Android 牛轧糖。如果你还在你的 XA Ultra 上玩棉花糖游戏，如果你需要 root，你需要遵循这个指南。如果你已经阅读了所有的警告，备份了任何重要的东西，并且准备好了，那么就开始吧！

* * *

[**看看这个 Noob 友好的 Xperia XA Ultra 生根指南吧！**](https://forum.xda-developers.com/xa-ultra/how-to/f32xx-how-to-root-xperia-xa-ultra-noob-t3639729)