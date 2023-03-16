# Android 任天堂 3DS 模拟器的非官方 Citra 实践

> 原文：<https://www.xda-developers.com/nintendo-3ds-emulator-android-citra/>

任天堂 DS 是最好的模仿 Android 的便携式游戏机之一，这是有充分理由的。DS 游戏对触摸屏控制的强调很好地转化为智能手机游戏，Android 手机上缺乏按钮可以通过使用蓝牙或有线游戏控制器来纠正。我一直在思考这个问题，这让我很好奇...任天堂 3DS 怎么样？3DS 是另一个具有相同特征的手持游戏机，我在 GitHub 上搜索，发现那里的*实际上是一个用于 Android 智能手机的任天堂 3DS 模拟器。满足高度实验性的 Citra for Android port。*

## 非官方的安卓版 Citra 本身就令人印象深刻

让这个非官方的 Citra for Android port 如此令人印象深刻的不是它是一个完美的功能模拟器，没有任何人发现的问题。事实上，远非如此。它有它的问题，它有它的缺陷，当然它甚至不能为更密集的标题提供远程功能。说了这么多，有些游戏绝对完美，或者接近完美，这取决于你的设备。所有这些事实有助于如何令人印象深刻的模拟器，但有一个事实需要蛋糕。Citra for Android 使用 Dolphin Emulator 的前端作为 GUI，但 Citra 的整个后端都移植在它的后面。

不会玩游戏也无所谓仿真吧？我们尝试了*火徽回声:瓦伦蒂亚的阴影*，虽然它在游戏的第一个对话就崩溃了。一些谷歌搜索发现，这实际上是一个老版本的 Citra 的问题，这个端口似乎是基于，而不是端口本身。接下来是*路易吉的豪宅*，效果出奇的好。在那之后，我们尝试了*超级马里奥 3D 大陆*，简直是一团糟。*铲骑士*和 *Crashmo/Pullblox* 表现也很完美，所以简而言之，你的里程可能会有所不同。不要指望这能在任何低于高通骁龙 845 的智能手机上运行。事实上，我们使用由[高通骁龙 855](https://www.xda-developers.com/qualcomm-snapdragon-855-snapdragon-845-kirin-980-cpu-gpu-ai-benchmarks/) 移动平台驱动的[小米 9](https://www.xda-developers.com/xiaomi-mi-9-specifications-launch/) 进行了测试。

不过有一个警告，这是 Citra 自发布以来的一个要求。3DS 游戏在模拟器中使用之前需要被解密，唯一的方法就是用一个真正被黑的任天堂 3DS。你可以转储你自己的游戏并解密以在 Citra 中使用，但是如果游戏仍然是加密的，它们甚至不会被识别。在我上面的截图中，你可以看到*口袋妖怪 Y* (EK2A.3ds)仍然是加密的。这是因为我转储了我的墨盒，在复制之前没有解密。还有一个问题也影响了一些游戏，要解决这个问题，你需要从一个真实的 3DS 中转储系统文件。

## Android 游戏性能的非官方 Citra

对你来说最重要的事情可能是游戏中的表现，对某些人来说，这是...耐用。*铲子骑士*和 *Crashmo* 相当不可思议，*超级马里奥 3D 陆地*糟糕透顶，*路易吉的豪宅*和*动物穿越*管用。你可以看看我在下面制作的视频，这应该会让你有所期待。

这还不包括其他游戏中出现的图形故障。*超级马里奥 3D 陆地*最差，其次是 *Crashmo* 。 *Crashmo* 至少还可以玩，*超级马里奥 3D 陆地*甚至没有让你在游戏区走动。跟*火徽*也是一样的故事，只是在最初的对话中崩溃了。

*这个非官方的 Citra for Android 端口，在这一点上，充满了图形错误和崩溃*

对于一些游戏，你也需要转储系统档案(和其中包含的系统字体)来运行它们。口袋妖怪 X 和*口袋妖怪 Y* 就是两个这样的游戏，因为它们需要游戏中没有预打包的系统字体。这不是一个困难的过程，你可以在 Citra 的网站[这里](https://citra-emu.org/wiki/dumping-system-archives-and-the-shared-fonts-from-a-3ds-console/)找到指南。无论如何，要解密你的游戏，你需要一台任天堂 3DS，所以这不应该是一个巨大的准入门槛。下面来看看*口袋妖怪 Y* 的一些截图。较慢的游戏，如回合制游戏，如*口袋妖怪*效果非常好。

## 请记住，这个端口的 Citra 的 Android 是非官方的

在 Citra 论坛上，许多用户询问了这款 Citra for Android port，因为他们认为这是官方的。虽然 Citra 的开发者还没有给予支持(很明显)，但他们[已经表示](https://community.citra-emu.org/t/pokemon-x-not-working-only-showing-white-screen-on-android/60611)他们正在与该端口的开发者合作，以使 Android 设备的官方端口成为现实。Citra 的 FAQ 也是这么说的，这可以解释为什么这个项目的最后一次提交是在大约两个月前。Citra 的开发者绝对没有参与这个应用程序的创建，但是我们分享了它，因为有些游戏确实运行得很好。不仅如此，这也是对 Android 仿真未来的一瞥。任天堂 3DS 在一个由电脑版 Citra 和 Dolphin Emulator 拼凑而成的程序中几乎处于可玩状态。这本身就是一个壮举，表明未来在 Android 上开发任天堂 3DS 模拟器肯定是正确的。

[**下载非官方的 Citra for Android 端口**](https://ci.appveyor.com/api/buildjobs/4qfbf5dm5n47tiyf/artifacts/app%2Fbuild%2Foutputs%2Fapk%2Frelease%2Fapp-release.apk) [**源代码**](https://github.com/SachinVin/citra_android)