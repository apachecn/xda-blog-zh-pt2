# 如何修复 OnePlus 3 的内存管理问题

> 原文：<https://www.xda-developers.com/how-to-fix-the-oneplus-3s-memory-management-almost-double-the-apps-in-memory/>

OnePlus 3 最近因遭遇与去年 Galaxy 手机类似的内存管理问题而受到批评，这个问题导致许多用户推迟购买这些设备。幸运的是，我们现在对 OnePlus 3 的问题以及如何修复它们有了更多的了解。

首先，有几件事必须说清楚:OnePlus 3 中的内存管理是*设计的*这么激进，而且据我们所知并不是 bug。我检查了 LMK 值和后台应用程序的限制，它们并没有超出寻常，即使它们没有充分利用 OnePlus 3 的 6GB 内存。此外， [Carl Pei 在 twitter](https://twitter.com/getpeid/status/743721729948737536) 上提到“他们有一个有利于电池的不同 RAM 管理策略”，并表示那些不同意他们决定的人可以修改参数。因此，定制 ROM 制造商可能会带来他们自己对 RAM 管理的看法(值得注意的是，我们测试的[非官方 CM13](http://www.xda-developers.com/oneplus-3-gets-cyanogenmod-13-recovery-right-after-launch/) 并没有看到显著的改进)。

https://twitter.com/getpeid/status/743721729948737536

注意:我们在审查单元中成功地尝试了这一点，但没有彻底测试性能或电池寿命问题。更好的解决方案可能就在眼前。

尝试自担风险！

保证开发社区会找到优化内存管理的方法，更好地利用 OnePlus 3 的 6GB 内存。虽然我们可能没有找到最佳的解决方案，但是我们研究了 build.prop 并找到了一行代码，您可以更改它的值来轻松地改进您的 RAM 管理。编辑 build.prop 的方法有很多，包括通过 ADB 无 root 拉[或者使用专门为](https://www.quora.com/How-do-I-edit-the-build-prop-file-in-Android-without-Rooting-it) [build.prop 编辑](https://play.google.com/store/apps/details?id=com.jrummy.apps.build.prop.editor&hl=en)设计的 root apps。这一次我个人使用了 Root Explorer，但是所有方法都应该可以工作。

找到 build.prop(根文件夹中的/system/build.prop)后，找到显示`ro.sys.fw.bg_apps_limit=20`的行，将末尾的值改为一个更大的数字。我测试了 36 和 42，都返回了相似的结果。**请记住，我们没有在这种设置下测试电池寿命或广泛的性能，所以只有在您愿意尝试并自担风险的情况下，才使用这种设置。**话虽如此，我们还是发现了巨大的成果:

这一调整几乎将 OnePlus 3 可以容纳的应用数量增加了一倍。我测试的方法是打开我在应用抽屉里的所有应用程序，循环往复，直到我找到第一个应用程序(在这种情况下，Android Pay)被踢出内存的点。在默认设置下，Android Pay 的 **12** 个应用只需要重绘。值设为 42，Android Pay 直到我打开 **22 个**应用才重画。同样，你的里程可能会有所不同，但我们已经看到了这个调整的重大改善。来自 C4ETech 的 Ash 甚至使用新的设置重新进行了测试，并发现了以下令人印象深刻的结果:

对于一加限制后台应用程序数量并有效降低 OnePlus 3 多任务处理潜力的决定，我们有着复杂的感受。令人失望的是，这款手机拥有的应用程序与我们的 3GB 和 4GB RAM 设备一样多，但最终我们相信一加这样做是有原因的，而且这是少数几家鼓励用户调整和定制自己喜欢的内容的公司之一。因此，尽管我们觉得 OnePlus 3 的内存在默认情况下严重利用不足，但我们知道 XDA 社区永远不会安定下来，它会找到一个最佳平衡，以满足那些希望从 OnePlus 3 的多任务处理中获得更多的人。

我们将继续我们的评估期，不改变多任务处理。我鼓励用户尝试这些和其他设置，找到好的平衡，并测试电池寿命，寻找任何奇怪之处。