# 一个可疑的任天堂 Switch 安卓模拟器已经在网上出现，而且它出奇的有效

> 原文：<https://www.xda-developers.com/shady-nintendo-switch-emulator-android/>

Android 智能手机是多功能的，你可以为现代和复古系统获得的仿真器的数量是令人难以置信的。从古老的系统如 NES 到[任天堂 3DS](https://www.xda-developers.com/official-citra-for-android-released/) ，你都可以在你的智能手机上舒适地玩。显然，模拟更现代的系统可能有点困难，迄今为止唯一的任天堂 Switch Android 模拟器是仅仅概念上的[。然而，一个新的任天堂 Switch 安卓模拟器刚刚在网上出现(via](https://www.xda-developers.com/mononx-nintendo-switch-emulator-android/) [*Wololo*](http://wololo.net/2020/09/01/the-odd-case-of-egg-ns-a-seemingly-working-switch-emulator-for-android-with-playable-performance-comes-with-stolen-code-from-yuzu-and-seems-to-require-a-specific-controller/) ...它出奇的有效。不过，也有一些注意事项。

## 是的，这个任天堂 Switch 模拟器是可疑的

所以，首先也是最重要的，这个任天堂 Switch 模拟器是*黑幕*。我们在谈论被盗的代码，不可靠的翻译，强行登录-这些工作。背景知识:Yuzu 是 PC 上最受欢迎和最著名的任天堂 Switch 模拟器，它工作得非常好。细则， [Android for 任天堂 Switch 港](https://www.xda-developers.com/switchroot-lineageos-android-nintendo-switch/)，[的开发者在 *GBATemp* 上说](https://gbatemp.net/threads/egg-ns-a-switch-emulator-for-android-devices.572915/#post-9185054)这款 Switch emu for Android 使用了 Yuzu 的部分 GPU 仿真代码；他还告诉我们，他发现了“大量”使用 Yuzu 代码的证据。顺便说一下，Yuzu 是在 GPLv2 下授权的，这个新的仿真器是闭源的。最重要的是，这个新项目背后的团队声称是一个美国工作室，他们已经在模拟器上工作了两年多，但他们的网站和模拟器本身仍然有中文文本，英文翻译很差。最后，要使用模拟器，您需要创建一个帐户并登录。

## 哦，你还需要一个特定的控制器

即使你已经设法克服了这个模拟器的可疑之处，还有一个重要的警告。**只能配合特定控制器**使用。这款控制器目前仅面向评测人员，预购才刚刚开始，售价 99.99 美元。这是一个控制器，看起来非常类似于任天堂 Switch 的 Joycons，这确实有道理。

如果你真的可以在没有控制器的情况下使用模拟器，那是一回事，但是如果没有控制器的连接，模拟器甚至不能启动。我们与章程交谈，他们告诉我们，控制器的检查理论上可以被欺骗以支持其他控制器，但我们已经付出了很多努力来混淆和保护应用程序免受调试和修补。有理论认为这个模拟器是由这个控制器背后的团队开发的，这是一个营销活动，尽管这些理论目前还没有得到证实。

## 尽管很多任天堂 Switch 游戏都在运行

展示这种特殊模拟器工作的最可信的视频之一可能是由塔基乌龙面制作的，他在 [Realme X50 Pro 5G](https://forum.xda-developers.com/realme-x50-pro) 上测试了它。最大的专注于仿真的 YouTube 频道之一【ETAPrime 也证实了它是真实的。塔基乌龙面展示了模拟器运行任天堂 Switch 经典，如神奇宝贝剑/盾，超级马里奥奥德赛，塞尔达传说:链接的觉醒，和神奇宝贝让我们去。它运行口袋妖怪游戏令人惊讶地好，虽然它确实承认有时表现出一些缓慢。

该模拟器只能在装有高通骁龙 855/855+/865/865+旗舰 SOC 的设备上运行良好，在较弱的智能手机上模拟真的不会有任何运气。模拟器本身拥有与 81 个标题的兼容性，尽管有 73 个被列为崩溃或只能进入菜单。

## 绝对值得等待

虽然这个模拟器令人震惊地工作，我们建议暂时不要寻找它。没有专有的 100 美元控制器是不可能使用它的，而且它违反了开源许可。出于这些原因，我们在本文中没有提到模拟器的名称或控制器的名称，但这并不难找到。如果我们对这个项目有更多的了解，或者有其他不可疑的事情出现，我们会让你知道的。这个消息无疑激起了我们的好奇心，因为它为那些也拥有被黑掉的交换机的人打开了手机游戏的新领域。