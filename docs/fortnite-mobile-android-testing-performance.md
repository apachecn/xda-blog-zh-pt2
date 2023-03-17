# 测试堡垒之夜移动在 Android 上的性能:你的设备能处理堡垒之夜吗？

> 原文：<https://www.xda-developers.com/fortnite-mobile-android-testing-performance/>

正如 Epic Games 承诺的那样，免费游戏《堡垒之夜》[终于在上周推出。在发布的前 3 天，这款游戏仅限于三星 Galaxy S7、Galaxy S8、Galaxy S9、Galaxy Note 8、Galaxy Note 9、Galaxy Tab S3 和 Galaxy Tab S4。我们预计独占期会长得多，可能仅限于](https://www.xda-developers.com/fortnite-mobile-android/)[Note 9](https://www.xda-developers.com/fortnite-mobile-on-android-samsung-galaxy-note-9-exclusive/)和 [Galaxy Tab S4](https://www.xda-developers.com/samsung-galaxy-tab-s4-fortnite-mobile-on-android/) ，但事实证明独占内容只是一个免费皮肤和 [15，000 V-Bucks](https://www.xda-developers.com/samsung-galaxy-note-9-pre-order-fortnite-mobile-promotion/) (游戏内货币。)现在游戏已经正式面向非三星设备，我们决定在[上尽可能多的支持设备](https://www.xda-developers.com/does-my-android-smartphone-support-fortnite-mobile-android/)上做一些快速游戏测试，并在 [*GameBench* 的朋友的帮助下获取性能数据。](https://www.gamebench.net/)我们测试了几款采用大多数受支持芯片组的设备——即高通骁龙 821、骁龙 835、骁龙 845、麒麟 970 和 exy nos 8895——只是为了感受一下 Android 上的堡垒之夜移动在当前大多数 Android 智能手机上的表现如何。

特别是，我们在以下设备上测试了 Android 平台上的堡垒之夜移动设备:

| 

设备

 | 

芯片组名称

 | 

国家政治保卫局。参见 OGPU

 | 

RAM

 | 

默认图形质量

 | 

默认帧速率限制

 |
| --- | --- | --- | --- | --- | --- |
| 荣誉 10 | 希西林 970 | 马里-72 国集团 MP12 | 6GB | 史诗 | 30fps |
| LG V30 | 高通骁龙 835 | 肾上腺素 540 | 4GB | 史诗 | 30fps |
| 一加 5 | 高通骁龙 835 | 肾上腺素 540 | 8GB | 史诗 | 30fps |
| 一加 6 | 高通骁龙 845 | 肾上腺素 630 | 8GB | 史诗 | 30fps |
| 三星 Galaxy S8 (Exynos) | Exynos 8895 | 马里-71 国集团 MP20 | 4GB | 中等 | 30fps |
| 三星 Galaxy S8(骁龙) | 高通骁龙 835 | 肾上腺素 540 | 4GB | 史诗 | 30fps |
| 三星 Galaxy S9+(骁龙) | 高通骁龙 845 | 肾上腺素 630 | 6GB | 史诗 | 30fps |
| 小米 Mi Note 2 | 高通骁龙 821 | 肾上腺素 530 | 4GB | 低的 | 20fps |
| 中兴 Axon M | 高通骁龙 821 | 肾上腺素 530 | 4GB | 低的 | 20fps |

*(注意:由于当前版本[游戏平台](https://www.gamebench.net/)的限制，我们无法在任何运行 Android Pie 的设备上进行测试，如谷歌 Pixel 2 或 Essential Phone。)*

自从游戏公开发行以来，我们只有很短的时间来测试这些设备，所以我们无法测试我们集合中的所有设备。此外，堡垒之夜目前不工作，如果你有一个解锁引导加载程序，这是我们的一个主要障碍，因为解锁引导加载程序是我们的事情。幸运的是，我们能够绕过 Epic Games 对 USB 调试的限制，因此我们可以毫无问题地启动并运行 [*GameBench*](https://www.gamebench.net/) 的桌面客户端。

在我们深入研究结果之前，我们想澄清这篇文章的目的和目的:

*   **我们没有在 Android 上对堡垒之夜移动进行基准测试**。我们玩游戏的每个测试者都不是在同样的条件下玩的。
    *   每位测试者都与其他玩家进行了一场现场比赛，以获取他们的设备在典型的堡垒之夜比赛中应该如何表现的数据。我们选择不只是坐在空无一人的操场上玩游戏，因为大多数用户将会体验到与多达 99 名其他玩家的真实交火，而不仅仅是沙盒构建体验。
    *   每个测试者玩的时间长度不一样。
    *   每个测试者在不同的时间穿过地图的不同区域，收集物品并在不同的时间与其他玩家战斗。
*   我们试图回答这样一个问题:“**我的设备能播放堡垒之夜吗？**“我们这么说是什么意思？
    *   我们想对一场典型的堡垒之夜移动比赛的中值帧速率、CPU/GPU/RAM 使用率和 FPS 稳定性(所有数据由 [*GameBench*](https://www.gamebench.net/) 提供)进行一些基本的数据收集，这样你就可以看看这款游戏是否值得在你的设备上试用。
    *   我们不会对我们测试的任何设备进行直接的性能比较。相反，我们将总结每个设备的性能，以便您可以自己决定(根据您的设备规格与我们测试的设备的相似程度)是否值得一玩。

现在，我们(希望)清楚了我们试图用这篇文章做什么，让我们看看每个设备在游戏中表现如何。

我们要特别感谢 [GameBench](https://www.gamebench.net/) 团队为我们提供的帮助。他们的工具使得任何人，无论是普通用户、记者还是工程师，都可以在 Android 设备上测试手机游戏的性能。他们有一个 Android 应用程序，你可以安装它来开始测试你的游戏，但请记住，堡垒之夜的反 USB 调试检测将阻止你使用 [GameBench](https://www.gamebench.net/) 的 Android 应用程序来分析堡垒之夜移动。

* * *

## 用 GameBench 测试堡垒之夜移动在 Android 上的性能

为了缩短文章和提高页面加载速度，所有图片都被缩小到缩略图大小。单击展开您有兴趣查看的图像。

### 荣誉 10

***总结:*** 玩家 TK 贝从 3 场比赛中采集样本。前 2 场比赛他大概 3 分钟就死了。在他的最后一场比赛中，他活了 10 分钟，看了 7 分钟。在他玩游戏的最初几分钟里，这款设备表现不错。然而，很明显，游戏的图形需求正在付出代价:Honor 10 开始经常出现丢帧现象，并变得非常热。

***数据:***

***结论:*** 它在短时间内玩得很好，但不一致的帧率可能会在长时间的游戏会话中困扰大多数玩家。Honor 10(可能还有其他麒麟 970 设备)将需要一些额外的优化，才能让堡垒之夜移动在最高的图形设置下获得愉快的体验。如果华为设法用堡垒之夜优化他们的 GPU Turbo 兼容设备，那么一旦更新推出，我们可能会看到性能的提升。

### LG V30

***概要:*** 玩家乔·费德瓦从 2 场比赛中收集样本。第一场比赛他死了大约 6 分钟。第二场比赛他坚持了大约 8 分钟，然后看了 2 分钟。与三星 Galaxy S8 或 OnePlus 5 不同，该设备无法在游戏的大部分时间内保持 30 fps。

***数据:***

***结论:*** 考虑到 OnePlus 5 和三星 Galaxy S8 这两款采用相同 CPU/GPU 的设备在相同设置下的表现，游戏中的表现相当令人失望。OnePlus 5 有两倍的内存，这应该有助于这样一个内存密集型游戏，但 Galaxy S8 也有同样的 4GB 内存。为了获得更高的性能，调低图形设置可能是值得的。

### 一加 5

***概要:*** 玩家(我自己)玩了一次 12 分钟的游戏，包括 9 分钟的游戏时间和 3 分钟的观看时间，直到比赛结束。OnePlus 5 在处理堡垒之夜移动方面没有任何问题。

***数据:***

***判决:*** 一加 5 像冠军一样处理堡垒之夜。这里没什么可抱怨的。

### 一加 6

***概要:*** 测试员丹尼尔·马尔凯纳打了 2 场比赛。在第一场比赛中，他持续了近 9 分钟，而在第二场比赛中，他持续了近 8 分钟。不出所料，OnePlus 6 在游戏中表现非常好。

***数据:***

***定论:*** 仿佛还有什么疑问，一加 6 能够轻松应对堡垒之夜移动。毕竟，这个游戏是用高通骁龙 845 上的设备优化的(比如三星 Galaxy Note 9)，所以任何带有最新高通芯片组*的设备在这里都应该*表现很好。

### 三星 Galaxy S8 (Exynos)

***概要:*** 测试者亚当·康威(Adam Conway)打了一场持续 12 分钟的单人赛。他的 Galaxy S8 在游戏中表现得令人难以置信的好，尽管记住游戏是在最高图形质量设置下运行的*而不是*。

***数据:***

***结论:*** 如果你愿意牺牲一些图形保真度，运行游戏应该没有问题。

### 三星 Galaxy S8(骁龙)

***Summary: ***The tester, XDA Junior Member thesbros, played a single session lasting nearly 12 minutes. While looting and running around, the game doesn't seem to struggle very much. However, during intense firefights, you may notice some dips in performance.

***数据:***

***判决:*** 如果你想在玩游戏的时候没有烦人的掉帧，就避免在最高的图形设置下玩游戏。

### 三星 Galaxy S9+(骁龙)

***概要:*** 测试者马克斯·温巴赫(Max Weinbach)进行了一场持续 11 分钟的单人游戏。不出所料，这款游戏表现不错，尽管有几个明显的激烈战斗区域导致了性能下降。我们被告知爆炸和某些特效是造成这种下降的主要原因。

***数据:***

***结论:*** 鉴于 Galaxy S9+与 Galaxy Note 9 共用相同的芯片组，我们预计 Galaxy S9+会相对轻松地处理堡垒之夜，尽管后者当然有液体冷却功能，以防止设备快速节流。一般来说，在 Epic 图形设置下玩游戏应该没什么问题。

### 小米 Mi Note 2

***总结:*** 我，测试者，玩了一单，持续 8 分钟。我没花多少时间就得出结论，这款设备上的游戏一塌糊涂。该设备甚至难以保持 20fps 的目标，并且在有许多建筑物或激烈交火的地方会崩溃。

***数据:***

***判决:*** 中止。请等待更新改善体验，然后在此设备或具有类似规格的设备上尝试。

### 中兴 Axon M

***总结:*** 我，测试者，玩了 8 分钟，才以游戏表现有多差而放弃(死亡后)。游戏在这个设备上是幻灯片，甚至比小米米 Note 2 还要多。

***数据:***

***判决:*** 中止！不要在 Axon M 上玩堡垒之夜，除非你打算烤棉花糖。

* * *

## 我的设备可以在 Android 上播放堡垒之夜手机吗？

我们已经发布了[最低硬件要求](https://www.xda-developers.com/minimum-requirements-fortnite-mobile-on-android/)、[确切硬件要求](https://www.xda-developers.com/is-my-phone-powerful-enough-for-fortnite/)以及[当前支持游戏的设备列表](https://www.xda-developers.com/does-my-android-smartphone-support-fortnite-mobile-android/)。以下是您需要了解的内容:

#### 最低要求

*   芯片组:Exynos 8890、8895、9810 或更新版本；海思麒麟 970 或更新；高通骁龙 820、821、835 或 845 或更新型号
*   内存:3GB 或更高
*   软件:安卓 5.0 棒棒糖或更高版本
*   OpenGL 版本:3.1 或更高版本(Vulkan 图形 API 支持是可选的)

#### 支持的设备

#### 目前不支持

### 单击以展开

*   HTC 10
*   HTC U Ultra
*   HTC U11
*   HTC U11+
*   HTC U12+
*   摩托罗拉摩托 Z
*   摩托罗拉摩托 Z 机器人
*   摩托罗拉摩托 Z2 部队
*   索尼 Xperia XZ
*   索尼 Xperia XZs
*   索尼 Xperia XZ1
*   索尼 Xperia XZ2

#### 去哪里下载？

如果你用的是三星设备，只需从三星 Galaxy 应用商店[这里](https://www.apps.samsung.com/appquery/appDetail.as?appId=com.epicgames.portal)下载游戏。如果你使用的是非三星设备，请按照 [Epic Games](https://www.epicgames.com/fortnite/en-US/mobile/android/new-device) 网站上的说明操作。

* * *

## Android 游戏上的堡垒之夜移动

如果你有兴趣看看在 Android 上处理堡垒之夜移动的设备上的实际游戏效果如何，请查看我们在三星 Galaxy S9+ 和骁龙 845 的 [OnePlus 6](https://www.xda-developers.com/fortnite-mobile-oneplus-6-razer-phone/) 上运行游戏[的视频。](https://www.xda-developers.com/fortnite-mobile-on-android-gameplay-samsung-galaxy-note-9/)