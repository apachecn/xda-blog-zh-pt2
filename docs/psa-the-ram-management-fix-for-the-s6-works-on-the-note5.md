# 以下是如何修复 Note5 的内存管理

> 原文：<https://www.xda-developers.com/psa-the-ram-management-fix-for-the-s6-works-on-the-note5/>

你讨厌你的 Note5 的 RAM 管理吗？好吧，事实证明，如果你有根，你可以把它变得更好。昨天，当我完成我的[笔记 5 回顾](http://www.xda-developers.com/failed-potential-the-note5-xda-review/)后，我决定四处寻找解决方案，结果发现它一直就在那里。

让 S6 和 Note 4 表现更好的相同 build.prop 编辑[](http://www.xda-developers.com/psa-you-can-optimize-your-note-4s-recents-menu-ram/)似乎也适用于 Note5。

修复包括编辑 build.prop 的 DHA 属性。我亲自试过，可以确认它部分工作，如下面的视频所示。然而，请小心谨慎，**这不是一个彻底的修复**，它很可能需要一些额外的调整，才能在每个设备上完美地工作。我只能测试它几个小时，我没有发现性能问题，额外的电池消耗也没有错误。然而，仍然可能有意想不到的后果，所以应用该修复程序需要您自担风险。也就是说，在实际使用过程中，它似乎确实使内存管理变得更好。然而，当手机闲置时间过长时，繁重的应用程序似乎会像往常一样被踢出内存。

在继续之前，确保你[了解修复](http://forum.xda-developers.com/showpost.php?p=61260005&postcount=80)并且**备份你的 ROM 和 build.prop 文件。**这需要 root 编辑 build.prop，你可以用一个简单的文本编辑器或者一个专用的应用程序来完成。为了应用该修复，用本文中的[或本线程中的](http://www.xda-developers.com/psa-you-can-optimize-your-note-4s-recents-menu-ram/) 中的 [替换 build.prop 的 DHA 属性。如果你漏掉了一些，就在你有的后面加上它们。如果你缺少 *全部* ，把它们加到最下面可能行得通(至少，我的注 4 是这么做的)。](http://forum.xda-developers.com/showpost.php?p=61260005&postcount=80)

我在我的 Note5 上试了一下，到目前为止我还没有遇到任何问题。然而，还需要更多的测试，所以如果你够大胆的话，应用这个补丁并告诉我们你的结果。这似乎没有风险，但请注意，这并不是针对 Note5 的特定修复，而且似乎也没有完全解决问题。更明智的做法可能是等待更好的解决方案，因为长时间的测试可能会暴露出意想不到的后果。也就是说，Note5 的 RAM 管理肯定可以改进，所以 XDA 会有办法的！

[**查看 XDA 笔记 5 论坛> >**](http://forum.xda-developers.com/note5)