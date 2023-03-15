# F2FS 对 EXT4 进行测试

> 原文：<https://www.xda-developers.com/f2fs-put-to-the-test-against-ext4/>

你可能还记得，本月早些时候，我们谈到了通过使用 F2FS 来加速最初的 Nexus 7 的内部内存。F2FS 是三星去年年初开发的，用于基于 Linux 的操作系统。顾名思义，闪存友好文件系统是一种专为满足基于 NAND 的存储设备的具体特征而设计的文件系统。

这种[日志结构的文件系统](http://en.wikipedia.org/wiki/Log-structured_file_system)被广泛认为比闪存上的 EXT4 等传统文件系统更快，但它真的更快吗？如果是，增加多少？XDA 公认的贡献者 [Androguide.fr](http://forum.xda-developers.com/member.php?u=4752917) 开始使用流行的合成基准测试来测量他的[索尼 Xperia Z1](http://forum.xda-developers.com/xperia-z1) 的性能差异，结果很可能会让你大吃一惊。

正如人们所料，在大多数情况下，F2FS 在 Z1 上比 EXT4 快。从数据库操作到 AnTuTu 和 Quadrant 中的高阶存储基准测试，各种不同类型的综合基准测试都证明了这一点。具体来看 AndroBench(右边的截图)，F2FS 上的数据库操作始终比 EXT4 快一个数量级。在这个综合性能指标评测中，顺序和随机写入的存储写入速度得到了更大程度的提高，在 F2FS 上两者都快了两个数量级以上。

但是在你出去把你的设备转换成 F2Fs 之前，有一些事情要记住。首先，看起来至少在 Z1 上，F2FS 的顺序读取速度比 EXT4 慢 20%。其次，也是更重要的一点，这些只是来自某个特定制造商的某个特定设备的某个特定样本的结果。换句话说，你的里程数几乎肯定会有所不同，特别是如果你没有在 Xperia Z1 上尝试这一点，因为真实世界的性能增益(或损失)将取决于你设备中的 NAND 芯片和闪存控制器，以及超出本文范围的各种其他因素。也就是说，如果你的结果显示类似的趋势，我们不会感到非常惊讶。

如果你想了解更多关于 Androguide.fr 的经验和他的测试中使用的方法，请前往[基准线程](http://forum.xda-developers.com/showthread.php?t=2697069)。你对 F2FS 有什么想法？他的结果和你的观察结果相似吗？你在转换到 F2FS 时遇到过什么问题吗？请在下面的评论中告诉我们！