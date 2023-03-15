# [更新:性能回归]在采用新的 Windows 10 功能后，谷歌 Chrome 的内存使用可能会显著下降

> 原文：<https://www.xda-developers.com/google-chrome-memory-use-drop-adopting-windows-10-feature/>

**更新 1(****07/14/2020****@****06:50am****ET):**由于其他性能问题，谷歌在 Chrome 85 中禁用了 SegmentHeap。滚动到底部了解更多信息。下面保留了 2020 年 6 月 18 日发表的文章。

谷歌 Chrome [RAM hog meme](https://knowyourmeme.com/memes/google-chrome-ram-hog) 可能很快就会成为过去，因为微软在 Windows 10 中引入了一个新功能，可以大幅减少 Chrome 的内存使用。根据最近来自 *Windows 最新*的报道，[Windows 10](https://www.xda-developers.com/tag/windows-10/)2020 年 5 月更新(20H1)已经开始向全球用户推出，它引入了 Windows 段堆内存改进，将减少谷歌 Chrome 等 Win32 应用的整体内存使用。

微软解释说，Windows 10 的最新更新为开发人员引入了一个新的“SegmentHeap”值，这是一个现代的堆实现，在 Windows 10 版本 2004 或更新版本上,*“通常会减少您的整体内存使用量”*。该公司证实，它已经开始在基于 Chromium 的 [Edge 浏览器](https://www.xda-developers.com/google-microsoft-collaborate-bringing-windows-spellcheck-chromium-based-browsers/)中使用新值，早期测试显示，Windows 10 2020 年 5 月更新后，内存减少高达 27%。

谷歌 Chrome 也可能受益于新的价值，根据最近在 Chrome Gerrit 上添加的承诺，变化可能很快就会到来。在提交中，一名 Chrome 开发人员指出，将“SegmentHeap”条目添加到 chrome.exe 清单将告诉 Windows 10 2004 或更新版本选择 chrome.exe 使用段堆而不是传统堆。开发人员进一步指出*“针对 chrome.exe 的每台机器选择段堆的实验表明，这可以在一些机器上的浏览器和网络服务实用程序进程等方面节省数百 MB。”*

虽然微软和谷歌都指出实际结果会有很大差异，但这一变化无疑会在一定程度上减少内存使用，并为用户提供更好的整体体验。截至目前，尚不清楚这些改进何时会在谷歌 Chrome 的稳定版本中发布。

**来源: [Windows 博客](https://blogs.windows.com/msedgedev/2020/06/17/improving-memory-usage/)，[微软应用清单](https://docs.microsoft.com/en-au/windows/win32/sbscs/application-manifests#heaptype)， [Chromium Gerrit](https://chromium-review.googlesource.com/c/chromium/src/+/2163163)**

**Via: [Windows 最新](https://www.windowslatest.com/2020/06/18/google-chrome-will-finally-use-less-memory-on-windows-10/)**

* * *

## 更新:由于性能问题，谷歌在 Chrome 85 上禁用了 Windows SegmentHeap

唉，铬鞣猪皮可能还会存活一段时间。正如谷歌在测试中指出的那样，Windows 上的 SegmentHeap 功能原本应该帮助谷歌 Chrome 减少内存使用，但现在发现它是以增加 CPU 使用量为代价的。谷歌观察到速度计 2.9 在启用该功能后速度下降了 10%，CPU 使用率和功耗增加了 13%。

因此，Chromium 团队现在已经禁用了 Chrome 85 的这个功能。但是，一旦获得足够积极的结果，该团队愿意在未来重新启用它。

**来源:[铬革里特](https://bugs.chromium.org/p/chromium/issues/detail?id=1102281)**

**故事 Via:[Techdows](https://techdows.com/2020/07/google-disables-windows-segment-heap-chrome-85-performance-issues.html)**