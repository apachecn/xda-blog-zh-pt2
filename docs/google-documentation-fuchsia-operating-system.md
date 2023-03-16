# 谷歌发布了解释 Fuchsia 操作系统的文档

> 原文：<https://www.xda-developers.com/google-documentation-fuchsia-operating-system/>

# 谷歌发布了解释 Fuchsia 操作系统的文档

谷歌终于开始整理关于其神秘的 Fuchsia 操作系统是什么以及如何工作的文档，包括对其引导序列、文件系统和锆石微内核的解释。

显然，这个页面并不新鲜，尽管这是我们第一次听说它。该页面以前被命名为“book.md ”,最近才被重命名，这就是它看起来很新的原因。

自从 Fuchsia 操作系统已经开发了将近 2 年以来，你可能已经在很多地方看到过它的名字。许多人猜测，谷歌并不神秘的操作系统将最终取代安卓。我们已经看到它从一个应用程序形式的[几乎没有功能的模拟用户界面](https://www.xda-developers.com/googles-fuchsia-is-a-smartphone-os-with-a-new-ui-but-no-linux-kernel/)成长为一个实际上可以在现有硬件上引导的版本[。我们已经看到谷歌对这个项目的重视程度，因为经验丰富的 Android 项目经理已经开始着手这项工作。但是这么长时间以来，我们从来没有收到过谷歌关于这个项目的官方声明或任何相关文档——迄今为止所有的信息都是人们钻研源代码的结果。](https://www.xda-developers.com/google-fuchsia-os-pixelbook-video/)

现在，这种情况似乎正在改变，因为谷歌发布了一个名为“ [The Book](https://fuchsia.googlesource.com/docs/+/master/the-book/) ”的文档页面。该页面旨在解释 Fuchsia，即“模块化的、基于功能的操作系统”是什么，不是什么。该页面上最突出的文字是解释 Fuchsia 不是 Linux 的一大部分，以防这还不清楚。上面是几个 readme 页面，解释 Fuchsia 的文件系统、引导序列、核心库、沙箱等等。页面的其余部分解释了什么是锆石微内核，以及如何实现框架、存储、网络、图形、媒体、用户界面等等。

在本文发表时，许多信息还没有被填充。额外的文档将被添加到这个页面，随着时间的推移，这个页面将会增加您需要了解的关于新操作系统及其微内核如何工作的所有信息。如果或当谷歌最终正式宣布 Fuchsia，他们可能会迁移到一个更专用的网页，更容易找到，但目前，这份文件是开发人员开始了解即将到来的操作系统如何运行的最佳方式。

*感谢 [@TelNetPort](https://twitter.com/telnetport) 的提示！*