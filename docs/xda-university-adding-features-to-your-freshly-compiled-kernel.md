# XDA 大学:向新编译的内核添加特性

> 原文：<https://www.xda-developers.com/xda-university-adding-features-to-your-freshly-compiled-kernel/>

我们之前已经介绍了如何从源代码[编译自己的内核](http://www.xda-developers.com/android/step-by-step-tutorial-on-how-to-compile-kernels-from-source/)的分步指南。简单地编译一些现成的源代码只是成功的一半。为了编译和刷新你自己的内核，你需要做一些修改。当然，你做出哪些具体的改变完全取决于你，在内核级别可以做出大量的改进来提高任何给定设备的性能。如果你正处于编译你自己的内核的阶段，但是有点不确定从哪里开始，XDA 大学有一个你会感兴趣的指南。

本教程涵盖了添加 CPU 管理器、I/O 调度程序的过程，以及将设备的 CPU 超频到内核的能力。这些是您可以进行的一些更基本的修改，但也是用户最想做的一些修改。所有需要的步骤都有清晰的概述，并附有简单易懂的代码示例，可以让你立刻修改并准备好编译。你当然需要熟悉 Github ，以便记录你的变更并保持 GPL 兼容。如果你需要进修课程，一定要看看这篇[成为 Git 向导的优秀指南](http://www.xda-developers.com/android/comprehensive-guide-to-using-github/)。

如果你想让自己的内核更上一层楼，请务必前往 [XDA 大学，看看这个](http://xda-university.com/as-a-developer/adding-features-to-your-kernel),因为这为更高级的开发提供了一个很好的起点。