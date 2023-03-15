# Galaxy 设备上的外部麦克风仅一个电阻之遥

> 原文：<https://www.xda-developers.com/external-mics-on-galaxy-devices-just-one-resistor-away/>

Android 设备支持大量外部设备。从蓝牙扬声器到外置硬盘，真的没有什么是你不能再连接到 Android 设备上的。然而，用户可能会遇到的一个问题是外部麦克风。

XDA 精英公认的开发者阿达穆特勒和 T2 雷贝洛又来了。这一次，硬件模块将允许在大多数三星 Galaxy 设备上更好地支持外部麦克风。这包括 [Galaxy Note II](http://forum.xda-developers.com/forumdisplay.php?f=1790) 和 [Galaxy 相机](http://www.xda-developers.com/tag/samsung-galaxy-camera/)。AdamOutler 更详细地解释了 mod:

> Elite Recognized 开发人员 Rebellos 搜索了代码，我们发现该设备不会识别我的麦克风，因为它的欧姆太低了。WolfsonMicro 芯片使用 1000 欧姆以下的任何值来表示按钮按下。1000 欧姆以上，表示麦克风。我的麦克风是一个 900 欧姆的麦克风，所以实际上，考虑到大多数都在 100-500 欧姆左右，这是相当高的。然而，我和雷贝罗斯设法破解了它。我想分享这个方法。

结果是硬件模块允许使用更大的外部麦克风。有几件事需要注意。正如亚当所说，为了被检测到，麦克风必须提供 1000 欧姆的电阻。如果没有，那么设备不会将其注册为麦克风，而是注册为按钮按压。由于我们大多数人都不想购买全新的麦克风，一个诱人的解决方案是创建一个适配器，使您已经拥有的设备能够工作。

根据 Adam 的说法，您将构建一个“三星 4 极至 1/4”麦克风适配器，内置 200 欧姆电阻。“这个过程本身并不太难，对于经常修改硬件的人来说，这应该是件轻而易举的事。因为你没有在你的设备上焊接任何东西，你很可能没有把它直接置于危险之中。小心别被烙铁烫伤了。

如果这看起来值得一试，那就去看看[原始线程](http://forum.xda-developers.com/showthread.php?p=36038426)。