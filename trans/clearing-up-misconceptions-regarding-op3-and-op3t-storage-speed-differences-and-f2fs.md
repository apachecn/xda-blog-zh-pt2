# 澄清对 OnePlus 3T 存储和 F2FS 的误解

> 原文：<https://www.xda-developers.com/clearing-up-misconceptions-regarding-op3-and-op3t-storage-speed-differences-and-f2fs/>

在一加为其 OnePlus 3T 版本宣传的改进中，我们被告知该公司已经设法提高了应用程序的打开速度和一般加载时间，这在 3D 游戏等重度应用程序上尤其明显。

这让我们感到惊讶，因为这款设备最终与最初的 OnePlus 3 封装了相同的 UFS 2.0 存储，骁龙 821 CPU 的最小改进在很大程度上与这种使用场景无关。也就是说，当我们[带着 OnePlus 3T](https://www.xda-developers.com/oneplus-3t-xda-review-what-has-changed-and-by-how-much/) 进行应用程序打开速度测试时，我们*确实发现*这款设备的冷应用程序打开速度比它的前辈更快。最初我们感到困惑，但在禁运信息中有一个关键细节也是 Carl 在公告视频([时间戳](https://www.youtube.com/watch?v=MeEMKLYU2E0&t=18m49s))中非常平静而迅速地提到的:文件系统从 EXT4 变成了 F2FS，这就是应用程序打开速度存在差异的原因。F2FS 是一个不同的文件系统，专门利用这些手机的闪存存储，因此，将它与 OnePlus 3 和 3T 已经非常优秀的 UFS 2.0 存储解决方案相结合是有意义的。

存储是相同的，处理器的冲击是最小的，但仅这一文件系统的变化就足以给现实世界的性能带来重大改善，表现在日常应用程序的打开速度略有加快，以及加载大型游戏如沥青 8 的速度大幅提高，如上所示。鉴于我能够在发布前发现这一点，我写了一篇文章[解释了 OnePlus 3 的一些变化](https://www.xda-developers.com/exclusive-the-philosophy-behind-the-op3t-why-oneplus-released-this-device-and-what-it-means-for-the-future-of-your-oneplus-3/)，并在完整的评论中提到 F2FS 将在不久的将来进入 OnePlus 3。此外，一加告诉我，OnePlus 3 的社区版本已经支持 F2FS，并继承了其中的一些改进(在评测中，我们将 OnePlus 3T 与其前辈当时最新的稳定固件版本 OxygenOS 3.2.6 进行了比较)。

* * *

本周早些时候， [AnandTech](http://www.anandtech.com/) 发表了[一篇关于 OnePlus 3T 的优秀评论](http://www.anandtech.com/show/10836/the-oneplus-3t-mini-review)，其中他们列举了这款新设备相比其前代产品带来的[存储速度提升](http://www.anandtech.com/show/10836/the-oneplus-3t-mini-review/4)。他们的结果完全准确，并在某些方面显示出相当大的差异，我几乎能够完全复制他们(嗯，在同一球场，但我需要这个双关语)- **然而**，一个关键的细节被遗漏了，导致一些用户对哪个版本的 OnePlus 3T 是更好的选择做出不正确的声明。具体来说，由于评测中显示的极其良好的存储速度结果，128GB OnePlus 3T 将带来更好的真实性能的说法是不正确的。这是因为这些结果没有考虑到文件系统向 F2FS 的变化，这在评论的 NAND 部分最初并没有被提到是主要原因；虽然固态硬盘中更多的存储通常会提高性能的说法是正确的(除非使用更高容量的芯片而不是并行芯片，这可能是事实)，但我们发现，由 AndroBench 测量的存储速度的差异似乎仅来自文件系统的变化，而不是存储量的变化。

为了证实这一点，我们在 128GB 和 64GB 的 OnePlus 3T 上进行了一些测试，首先是并行的相同应用程序打开速度测试。这一次，我们发现 64GB OnePlus 3T 在相同的启动条件下(在干净的设置，没有恢复的应用程序，最少的后台进程，100MBps 互联网)与 128GB OnePlus 3T 表现几乎完全相同，使用 Discomark 对每个样本的每个应用程序运行 20 次(允许没有后台进程和不保持活动，以模拟冷启动)。方差的微小差异可以归因于设备上不同的谷歌账户(我并不拥有两台设备)，但两台设备都没有主动同步，总体而言，结果与四分位数范围的相似性相同。我们进一步测试了游戏加载速度:在我们的 OnePlus 3T 评测中，我们展示了一个视频，对 3 和 3T 加载沥青 8 进行了比较，3T 具有明显的多秒长的优势。64GB 和 128GB 的 OnePlus 3T 加载游戏的平均时间都在 10 秒左右，随机差异仅相隔毫秒。

当我们比较 64GB 和 128GB 版本的 AndroBench 结果时，我们还看到默认设置和 AnandTech 设置的分数非常相似(一个线程，顺序缓冲区大小设置为 256KB，随机缓冲区大小设置为 4KB)，后者是对真实场景下性能的更准确预测。总体而言，64GB 和 128GB 版本的存储速度似乎没有实际差异，即使我们也预计到了这种差异，因为我们认为会有更多的 NAND 芯片。(请记住，该测试具有相对较高的方差，屏幕截图中显示的差异并不一定意味着其中一个总是更好，即使只是一点点)。更有趣的是，当我们通过这些测试将 OnePlus 3 放在 F2FS 上时，我们得到了相同的结果。

正如我们之前提到的，该社区建立在 OnePlus 3 支持 F2FS 存储之上。我们首先在 Oxygen 3.2.6 上再次运行基准测试，以确认差异确实与 AnandTech 所显示的一样明显，并且我们在两种设置上获得了相同的结果。之后，我们加载了 Open Beta 7，并通过验证/data 确保它被正确格式化为 F2FS。

在使用 F2FS 文件系统的 64GB OnePlus 3 上运行测试，我们在默认的 AndroBench 设置和更精确的设置上获得了与 128GB OnePlus 3T 大致相同的结果。此外，我们发现应用程序的打开速度也差不多。最有说服力的线索来自沥青 8 加载速度测试，因为虽然最初的测试让 OnePlus 3 落后几秒钟，但我们看到它现在几乎同时跟上并加载。

* * *

那么这一切意味着什么呢？OnePlus 3T 在现实世界中性能的提高主要归功于 F2FS，它肯定会随着 Nougat 正式发布到 OnePlus 3 中(今天提供测试版！).一加用户对 F2FS 并不陌生，事实上出于同样的原因，这也是 OnePlus One 的一个常见模式。虽然你可以通过自定义恢复将存储格式化为 F2FS，但我建议你等到 OnePlus 3 正式更新时，或者尝试牛轧糖测试版。改进可能是实质性的，特别是我们在繁重的应用程序和 3D 游戏方面展示的，但在大多数情况下，OnePlus 3 已经做得很好了。OnePlus 3 的所有者肯定对牛轧糖的更新有很多期待，因为 F2FS 本身可能会确保他们在 UX 的特定地区获得更快的手机。

OnePlus 3T 的用户不应该指望仅从骁龙 821 就能提高应用程序的打开速度(但这是另一天的误解)，说实话，通过将性能集群降频回普通 OnePlus 3 和 Snapdragon 820 的 2.15GHz，你可能不会错过太多速度或流畅度。事实上，这可能会使 OnePlus 3T 的更大电池更加明亮，我相信开发人员将对内核进行智能更改，并提供有用的调节器，以便用户可以在低于 2.35GHz 峰值的情况下享受快速的性能和出色的电池寿命。

总而言之，OnePlus 3 和 OnePlus 3T 在 F2FS 下的表现基本相同，这很可能会随着官方牛轧糖的更新而出现在 OnePlus 3 上。根据 AndroBench 的测量，存储速度的差异似乎不是 128GB 版本中额外的 NAND 芯片的结果，而是对底层文件系统的改变。这对 OnePlus 3 用户和 OnePlus 3T 用户来说绝对是一件好事，他们真的不必担心用户体验不佳，因为他们宁愿选择更少的存储空间。一天结束时，两款手机都非常爽快，即使有[报道的](https://www.xda-developers.com/users-voice-concern-over-touch-screen-latency-issues-on-oneplus-3-3t/)(坦率地说，夸大了)触摸延迟问题。

* * *

[**查看 XDA OnePlus 3T 论坛> >**](http://forum.xda-developers.com/oneplus-3t)

[**查看 XDA OnePlus 3 论坛> >**](http://forum.xda-developers.com/oneplus-3)