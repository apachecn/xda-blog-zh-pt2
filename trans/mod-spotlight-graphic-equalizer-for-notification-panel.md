# 通知面板上的图形均衡器

> 原文：<https://www.xda-developers.com/mod-spotlight-graphic-equalizer-for-notification-panel/>

XDA 上每天都会出现大量令人惊讶的 mod。有些很有创意，有些很漂亮，但通常吸引我们眼球的是创新的贡献和巧妙的改编。这个由 XDA 资深会员[阿迪·艾斯特瑞重生](http://forum.xda-developers.com/member.php?u=5204709)制作的[图形均衡器模块](http://forum.xda-developers.com/android/themes/guide-how-to-add-music-visualizerview-t3062114)是两者的混合。他已经找到了一种在其他 rom 上获得 CM 11 Tiles 均衡器显示模式的方法，其结果一定会吸引很多人！

这是给你的通知面板底部一个均衡器，就像这里看到的。每当你拿出手机切换歌曲时，均衡器还会出现在音乐控制键上方的锁屏中，让你眼花缭乱。最好的部分是，就支持而言，它是一个广泛的 mod，因为它据称可以在 KitKat 和 Lollipop 的 CM 和 AOSP rom 上工作——这两者都已经在包括最新的 Android 5.1 在内的线程中成功测试。其他皮肤也可以有这种 mod 工作，但线程中的指令没有考虑 OEM UI 目录或代码中可能的变化，只是提到了您可能在特定 ROM 中遇到的不同 XML。

在我的笔记中，我无法让它在 Lollipop TouchWiz 上工作，但在 AOSP 和 CM ROMs 上的成功率似乎很高，因为这些指令很详细，也不是非常复杂:你需要反编译和编译 apk 以及修改 SystemUI.apk 中的文件的经验，但一旦你有了系统的相应工具( [Apktool](http://ibotpeaches.github.io/Apktool/) 和记事本将被证明是有用的)以及所需的 JRE， 这就是打开源代码，将线程中的代码粘贴到相应的位置，并在顶部加上签名。 如果你真的尝试这样做，**我们建议你要非常耐心**，因为弄乱你不应该弄乱的地方会导致不稳定的系统界面，包括强制关闭和其他讨厌的东西。

话虽如此，这绝对是一个惊人的添加，即使它以前被做过。事实上，它现在可以应用于如此多的软件版本，这意味着那些从来没有遇到过或考虑过它的人，或者那些喜欢股票的人，现在可以看到均衡器随着他们最喜欢的音乐跳舞，不管他们使用的是什么特定的 ROM，每当他们想浏览通知或管理他们的音乐时。像这样的 mod 和端口是我们一直希望看到的，所以如果你听到其他很酷的调整或者你想看到的特色，给我们一个提示，我们会检查一下。

**[访问线程](http://forum.xda-developers.com/android/themes/guide-how-to-add-music-visualizerview-t3062114)获得你的图形均衡器模块。如果你正在为你的手机寻找一个新的视觉调整，这个肯定会给你的用户界面带来一些节奏！**