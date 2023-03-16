# 谷歌 Pixel 3 & Pixel 3 XL 问题清单:购买前了解

> 原文：<https://www.xda-developers.com/google-pixel-3-pixel-3-xl-issues-problems-help-list/>

自从谷歌 Pixel 3 及其更大的兄弟产品谷歌 Pixel 3 XL[发布](https://www.xda-developers.com/google-pixel-3-google-pixel-3-xl-specs-features-pricing-availability/)以来，我们一直在歌颂它们。在我在[对 Pixel 3 XL 的初次评测](https://www.xda-developers.com/google-pixel-3-xl-camera-software-design-pixel-stand/)中，我解释了最新的谷歌 Pixel 设备如何体现了让谷歌 Chrome 操作系统如此受人喜爱的三大原则:速度、简单和安全。但是，即使像谷歌 Pixel 这样精致的设备在到达消费者手中后也必然会有一些问题，今年的 Pixel 3 也不例外。

我通常采取保守的方法来报道新设备的问题，因为很难判断用户报告何时真正表明设备存在更大的问题。然而，在 Pixel 3 和 Pixel 3 XL 的案例中，我们论坛和 Reddit 上的 Pixel 用户社区已经提出了各种问题，这些问题已经进入了其他博客。因此，在你看到我们发布的令人难以置信的[夜视相机样品](https://www.xda-developers.com/google-pixel-night-sight-google-camera-review/)后，为一个新像素支付数百美元之前，我们认为你应该知道早期采用者面临的一些问题。

这些问题中的一些可能是交易的破坏者，而另一些可能对你来说是吹毛求疵。我们会注意到哪些问题可能会通过软件更新得到解决，以及谷歌是否已经就此事发表了声明。最后，由于我身边只有 Pixel 3 XL，所以我只能就只影响 3 XL 的问题发表我的看法。

**更新 1:** 增加了谷歌对刮痕、随机刻痕和网飞·HDR 部分的回应。

**更新 2:** 根据多用户报告，增加了“低音量时扬声器发出嗡嗡声/声音失真”和“粉红色着色”部分。

**更新 3:** 向“后台关闭的应用”部分添加了详细信息。

**更新 4:** 谷歌已就内存管理问题发表评论。

**更新 5:** 谷歌已就扬声器失真问题发表评论。

**更新 6:** 内存管理问题和扬声器嗡嗡声问题已经基本解决。

**更新 7:** 随着 2019 年 1 月的安全补丁更新，录制视频时的音频质量得到了改善。

* * *

## 内存管理

### 问题#1 -应用程序在后台关闭

考虑到我关于 XDA 的第一篇文章是为 Nexus 5X 只有 2GB 内存辩护，但 Pixel 3 可能没有足够的内存，我说这话感觉很奇怪。随着每个月更高质量的应用和游戏的发布，很明显，Android 设备现在只需要更多的内存。谷歌 Pixel、谷歌 Pixel 2 和谷歌 Pixel 3 都有 4GB 内存，而 OnePlus 6、Razer Phone 2、小米 POCO F1 等提供高达 8GB 的内存选项。4GB 内存*对于 Pixel 3 的大多数用户来说*应该足够了，但有许多用户报告该设备经常在后台关闭最近使用的应用程序。

这也不是一个孤立的问题。安 [*安卓中央*编辑](https://twitter.com/journeydan/status/1051988879874523137)，[编辑 *The Verge*](https://twitter.com/dcseifert/status/1051998376169021441) ， [*安卓警察*](https://twitter.com/ArtemR/status/1053708854498709504) ，[马克斯·布朗利](https://www.youtube.com/watch?v=E67Klqw2H-E&feature=youtu.be&t=562)， [Reddit](https://www.reddit.com/r/GooglePixel/comments/9qn20z/this_community_needs_a_reality_check/) 上无数其他人都有内存管理问题。(所有链接 via*安卓警察。我自己的 Pixel 3 XL 在保存应用程序方面比我的 OnePlus 6 差得多，当然，我认为这是因为我的 OnePlus 6 有 8GB 内存。虽然很少有用户会有与 Artem Russakovski(如下所示)相同的体验，但我敢打赌大多数用户每天至少会遇到几次 Pixel 3 的内存管理问题。我最近在看到像[堡垒之夜移动这样的游戏在 Pixel 2 XL 上的表现](https://www.xda-developers.com/fortnite-mobile-android-testing-performance/)后，开始倡导谷歌在他们的设备上提供至少 6GB 的 RAM，我认为像下面这样的视频显示了即使是基本的用户体验也会因为没有足够的 RAM 而受到影响。*

至于这个问题的潜在原因，我采访过的两位内核开发者将部分责任归咎于谷歌使用 LMKD 的举动。LMK 或低内存黑仔是一个监控内存使用情况的进程，它会杀死最不重要的进程，以释放内存用于更重要的任务。LMK 驱动通常驻留在内核中，但是从 Linux 内核 4.12 开始，现在有了一个[用户空间 LMK 守护进程](https://android.googlesource.com/platform/system/core/+/master/lmkd/)。谷歌选择的[默认值](https://twitter.com/topjohnwu/status/1054413331426172930)是否过于激进还有待观察，因为谷歌尚未就此事发表任何声明。但是现在[有可能确定像素 3](https://www.xda-developers.com/google-pixel-3-unlock-bootloader-root-magisk/) 的根，我们可以调整 LMK 值来自己看。

**严重程度:*高***

**谷歌回应:*谷歌在 12 月[发布了一个更新](https://www.xda-developers.com/december-android-security-update-memory-camera-pixel-3/)来解决这些问题。***

**补丁发布的可能性:*补丁随着 12 月份的安全补丁一起推出。***

* * *

### 问题#2 -有时，照片没有被保存

很难不滔滔不绝地谈论 Pixel 3 的摄像头有多棒。谷歌相机应用程序尽其所能确保即使像我这样简单地指向并拍摄一个主题的初学者也能拍摄出像样的照片。借助 Top Shot、动态照片和动态自动对焦等功能，捕捉精彩照片比以往任何时候都更容易——即使您的手不稳或拍摄对象在移动。也就是说，除非，你的像素实际上*保存了*你刚刚拍摄的照片。

对于一些用户来说，Pixel、Pixel 2 和 Pixel 3 根本无法捕捉照片或视频。你按下快门按钮，期望保存一张像样的照片，却发现图像或视频从未保存。我在测试 Pixel 3 是否可以录制带有立体声音频的视频时，在我的 Pixel 3 上发生过一次这种情况(它确实可以)，但此后再也没有发生过这种情况。我的 Pixel 2 XL 也从未出现过这种问题。尽管如此，很多人都遇到过这种情况，当这种情况发生时，感觉真的很糟糕。这个问题背后的主流理论是，它与内存管理有关，但没有人真正知道为什么会发生这种情况。

**严重程度:*高***

**谷歌回应: [*针对所有像素的修复即将到来*](https://www.engadget.com/2018/10/22/google-camera-save-photos/)**

**修复到来的可能性:*已经确认***

* * *

## 音频和视频

### 问题#3 -视频录制的音频质量差

鉴于谷歌在计算摄影方面的过往记录，人们对新款 Pixel 3 拍照能力的关注就不足为奇了。但我们不应该忘记，Pixel 在录制视频方面也很棒，或者说应该很棒。Pixel 2 的[融合了视频稳定](https://www.xda-developers.com/google-explains-the-fused-video-stabilization-technique-used-in-the-pixel-2/)技术，其算法结合了硬件的光学图像稳定器和谷歌的电子图像稳定技术，实现了令人难以置信的稳定视频。谷歌没有做任何像华为 Mate 20 的视频散景或人工智能影院效果那样疯狂的事情，但我们预计 Pixel 3 的视频记录至少可以与最新的苹果 iPhone 媲美...对吗？

不幸的是，情况似乎并非如此，主要是因为 Pixel 3 的录音质量相对较差。当你离开设备几英尺远时，录音质量会明显下降，近距离听起来仍然很遥远。这个问题是由 YouTuber SuperSaf TV 首次曝光的，我们认为你最好听听他视频的第一部分，听听 Pixel 3 和 iPhone Xs Max 之间的区别。

有意思的是，有人发现前景有游乐场 AR 贴纸视频录制时的音频输出[明显好于](https://youtu.be/Mj6r5CpTC1o?t=52)。Pixel 3 可以录制相当不错的音频，但谷歌的调整似乎明显降低了质量。为什么？我们让谷歌来解释:

> #### “我们在 Pixel 3 的音频录制功能方面取得了几项进步，包括在风景模式下实现立体声录制。当在户外录音时，我们的调音是专门设计来减少背景噪音，如风和道路噪音以及过大的声音，并优化可听语音。为了实现这一点，我们有选择地削弱一些频率，从而最大限度地减少干扰噪声，优化最终音频。我们对我们的产品进行了广泛的用户测试，以确保它们针对现实世界的使用进行了调整，我们一直在根据用户反馈寻找其他调整机会。”——谷歌发言人在发给 *Android Police* 的声明中

**严重程度:*中等***

**谷歌回应:** ~~[***按计划工作***](https://www.androidpolice.com/2018/10/19/deja-vu-pixel-3-3-xl-video-recordings-poor-audio/)~~***[2019 年 1 月更新](https://www.xda-developers.com/january-2019-android-security-google-pixel/)***

**修复到来的可能性:*改进推出***

* * *

### 问题#4 -扬声器不平衡

当你处理 Pixel 3 和 Pixel 3 XL 上的立体声扬声器时，你会期望两者在音量输出方面平衡。然而，Pixel 3 XL 的情况并非如此。正如[许多用户](https://www.reddit.com/r/GooglePixel/comments/9na0jz/pixel_3_xl_sound_imbalance/)在 [Reddit](https://www.reddit.com/r/GooglePixel/comments/9ntil1/unbalanced_speakers_on_the_pixel_3_xl/) 上首次发现的，以及 [*Android Police*](https://www.androidpolice.com/2018/10/18/one-pixel-3-xls-front-facing-speakers-much-louder/) 在视频中捕捉到的，Pixel 3 XL 上的扬声器在音量输出方面有着相当明显的差异。

当我在我的 Pixel 3 XL 评测装置上测试扬声器质量时，我发现与去年的 Pixel 2 XL 相比，它的低音很好，失真最小，输出声音相当大。谷歌声称，Pixel 3 的扬声器声音比 Pixel 2 大 40%，同时具有更好的低频响应。我相信 Pixel 3 使用的是 Waves Audio 的 MaxxAudio 技术，但谷歌还没有详细说明他们在音频方面的改进。无论如何，以下是谷歌对立体声扬声器音量差异的官方声明:

> #### “大家好，这是特意设计的。我们特别设计了扬声器，允许更大的声音(比去年大 40%)和更好的低频响应。我们使用新的放大器技术和先进的扬声器保护算法来推动这些扬声器，真正发挥它们的每一点性能。我们还与格莱美获奖音乐制作人的专家调音密切合作，以发挥硬件系统优势的方式增强音频。”-/u/[Reddit 上的 pixel community](https://www.reddit.com/r/GooglePixel/comments/9na0jz/pixel_3_xl_sound_imbalance/e80cz41/)

**严重性:*低***

**谷歌回应:*工作正常***

**修复到来的可能性:*低***

* * *

### 问题#5 -过度振动

我不知道你们中有多少人在手持手机的同时听着扬声器中的音乐，但如果这描述了你，那么你可能会被 Pixel 3 的振动马达所困扰。虽然 Pixel 3 和 Pixel 3 XL 在任何 Android 设备上都提供了最好的触觉反馈(我不是那种通常会在意的人，但我可以说它是例外)，但一些评论者指出，当扬声器播放大声的音乐时，设备会过度振动。这个问题最早是由BGR 提出来的，但是我怀疑这个问题到底有多大。不过，如果你有机会在购买之前演示一台设备，你应该亲自测试一下。以下是来自 *BGR* 的评论的摘录，描述了他们的问题:

> #### “谷歌的新 Pixel 手机有前置立体声扬声器，听起来很棒，声音非常大。不幸的是，使用它们意味着处理一个不想要的副作用:手机背面疯狂的振动...音量小的时候，真的很烦。手机的背面会随着你播放的音乐的每一拍而震动。即使在视频对话过程中，你仍然可以感觉到手机背面不断震动。如果有声音，那就是振动。
> 
> #### 然后如果你把音量调大到 50%左右，震动就从讨厌变成加重。在 80%或更高的水平上，这简直太可怕了。手机背面的振动强度与谷歌用于通知的手机内部的振动马达一样大，甚至更大。想象一下，播放音乐时，手机的通知马达一直在震动。它如此暴力，以至于谷歌的 fabric Pixel cases 几乎没有丝毫减弱它。”——[扎克·爱泼斯坦](https://bgr.com/2018/10/15/pixel-3-review-top-10-surprises-in-google-pixel-3-xl/)，为 *BGR* 撰稿

值得一提的是，我不认为这个问题像扎克说的那样明显。当然，当我以最大音量播放音乐时，我的 Pixel 3 XL *确实会震动，但这并没有让我放下手机。官方的 Pixel Fabric 外壳*也为我显著地减弱了振动。这又是一个问题，在决定它是否困扰你之前，你必须尝试复制你自己。这里有一个视频，可能会让你知道 Pixel 3 的背部振动有多大。**

**严重性:*低***

**谷歌回应:*无***

**修复到来的可能性:*低***

* * *

### 问题#6 -低音量时扬声器发出嗡嗡声/声音失真

[大量](https://www.reddit.com/r/GooglePixel/comments/9p1hwn/my_new_pixel_3_xl_has_a_very_buzzy_bottom_speaker/)[用户](https://www.reddit.com/r/GooglePixel/comments/9pfz12/pixel_3_xl_speaker_distortion/)[Reddit](https://www.reddit.com/r/GooglePixel/comments/9q9lug/update_on_speaker_issue_my_experience_with_pixel/)报告 Pixel 3 XL 在低音量下出现嗡嗡声、失真声音。据 [*安卓警察*](https://www.androidpolice.com/2018/10/22/pixel-3-xl-owners-complaining-buzzing-distorted-speakers/) 报道，去年 Pixel 2 XL 的部分机主经历了这个问题。 *Android Police* 报道，以下[两段](https://www.youtube.com/watch?v=Re88NCvwo8Q) [视频](https://www.nbcnews.com/news/amp/ncna921471)展示了 Pixel 3 XL 上的问题。

**严重性:** ***低***

**谷歌回应:用户在 Reddit 上报告称，Pixel 的【2018 年 12 月安全更新也改善了嗡嗡作响的扬声器问题。**

**出现修复的可能性:*此问题已在 2018 年 12 月的安全更新中解决。***

* * *

### 问题#7 -无法以 60 帧/秒的速度录制 4K 视频

在谷歌制造活动的官方演示期间，谷歌真的不想谈论技术规格。直到 *iFixit* 进行硬件拆解*后，我们才发现是谁制造了 [Pixel 3 的](https://www.xda-developers.com/google-pixel-3-lg-oled-pixel-2-xl/)和 [Pixel 3 XL 的显示屏](https://www.xda-developers.com/google-pixel-3-xl-oled-display/)(分别是 LG 和三星)。*此外，我们知道 Pixel 3 和 Pixel 3 XL 使用索尼 IMX363 作为单后置摄像头的唯一原因是我[翻了一些供应商文件](https://www.xda-developers.com/google-pixel-3-sony-imx355-imx363-camera-sensor/)。自从这两款设备都装有索尼 IMX363 以来，为什么这两款 Pixel 3s 都不支持 60 FPS 的 4K 视频录制的谜团一直没有解决。事实上，这只会变得更加混乱。

高通骁龙 845 中的 ISP 当然能够处理 4K@60FPS，其他带有 IMX363 的设备，如华硕 Zenfone 5Z、Razer Phone 2 以及即将推出的 POCO F1 都支持 4K@60FPS。因此，我们只能猜测为什么这些设备不支持 4K@60FPS 录制。一些谷歌相机改装者认为这是因为谷歌的融合视频稳定功能无法与 4K@60FPS 兼容。不管是什么原因，其他设备能够做到这一点，而谷歌没有提供这一选项，这有点令人失望。说到缺乏选项，谷歌取消了手动设置 60FPS 以 1080p 录制的功能，转而采用了[自动 FPS 切换模式](https://www.xda-developers.com/google-pixel-3-google-pixel-3-xl-minor-features/)。

**严重性:*低***

**谷歌回应:*无***

**修复到来的可能性:*低***

* * *

## 问题#8 -划痕

我们终于在谷歌设备上再次实现了无线充电(有一些注意事项——下面会有更多说明),但这意味着我们必须处理玻璃背面。玻璃背面涂有触感柔软的涂层，使其感觉更像塑料，并有一层 Gorilla Glass 5 进行保护。我爱惜我的设备，从不把它们从箱子里拿出来，而且几乎从不在放手机的同一个口袋里放其他东西，所以我很少处理设备上的划痕。然而，也有一些像来自 ArsTechnica 的罗恩·阿马迪奥和马克斯·布朗利这样的评论家处理过他们的评论单元上的划痕。然而，Pixel 3 是否容易被划伤仍是个未知数。

这里有两个视频，一个是 Erica Griffin，另一个是 JerryRigEverything 的 Zack Nelson，测试 Pixel 3 的耐用性。

**严重程度:*中等***

**谷歌回应:*谷歌向 [The Verge](https://www.theverge.com/2018/10/15/17973484/google-pixel-3-xl-review-camera-features-screen-battery-price-photos) 提交了一份声明供其审查。***

> #### “我们将 Pixel 3 设计成手感极佳的产品。我们使用 Gorilla Glass 5 设计了正面和背面，以增强强度和保护。在背面，我们添加了一种特殊的纹理，使你的 Pixel 3 握起来很舒服，不太滑，比其他玻璃背手机更不容易留下指纹。我们在纹理背面玻璃的制造过程中增加了一个额外的强化步骤，以增强对标记和划痕的抵抗力。我们对手机的每个部件都进行了广泛的可靠性测试。”

* * *

## 无线充电

### 问题#9 - 10W，非合格中介机构，专有收费

因为谷歌对 Pixel 3 中的无线充电技术极其含糊，所以我不想通过假设 Pixel 3 支持通过 Qi 无线充电标准进行 10W 无线充电来填补空白。看到谷歌的 18W 有线充电符合 USB 供电标准，我不会责怪你做出这种假设。然而，事实证明，Pixel 3 的无线充电技术是专有的——你不能随便使用亚马逊或易贝的任何 10W 无线充电器。

一位 Reddit 用户得到了这个教训，当他们购买了一个宣传 10W 无线充电的 Anker 无线充电支架时，却发现它并没有以宣传的功率充电。他使用[安培](https://play.google.com/store/apps/details?id=com.gombosdev.ampere)应用程序发现了这一点，尽管不科学。用户并不认为他们的老式 Qi 无线充电器提供了最大 10W 的功率，因为手机告诉他们它正在“快速充电”，然而，即使谷歌确定充电器是否“快速”的阈值是 T4 是否提供了 7.5W 的功率。不过，这似乎是 SystemUI 的一个缺陷。

在您购买无线充电配件之前，以下是您需要了解的一些内容:

*   谷歌 Pixel 3 和 Pixel 3 XL **仅支持通过谷歌 Pixel 支架进行 10W 无线充电，以及通过“[为谷歌](https://get.google.com/madefor/)制造”计划销售的认证充电器**。到目前为止，似乎只有[这款 Belkin 无线充电器](https://www.belkin.com/us/p/P-F7U050-MG/)被认证支持 Pixel 3 的专有无线充电技术。然而，只有 Pixel 支架可以让你访问新的谷歌助手集成。
*   谷歌 Pixel 3 和 Pixel 3 XL 仅支持通过支持 Qi 的无线充电器进行 **5W 无线充电。**

**严重程度:*中等***

**谷歌回应: [*按计划进行*](https://arstechnica.com/gadgets/2018/10/drm-for-chargers-google-pixel-3-locks-fast-qi-charging-to-its-own-79-stand/)**

* * *

### 问题#10 -像素支架奇怪

是的，你可以将 Pixel 3 或 Pixel 3 XL 水平放置在 Pixel 支架上，但当锁屏、环境显示和始终显示**不支持横向模式**时，你为什么要这样做？事实上，他们有，但谷歌从未启用它。这是他们需要更改的[单行代码](https://android.googlesource.com/platform/frameworks/base/+/master/core/res/res/values/config.xml#1210)，我可以理解切换布尔值并将其发布给用户可能不是一个好主意，因为环境显示 UI 尚未针对横向进行优化。然而，我觉得这是谷歌的一个大疏忽，因为当手机垂直停靠在 Pixel 支架上时，你不能插入任何像 Pixel USB-C 耳塞一样的 USB Type-C 耳塞。见鬼，如果 Android Pie 没有[移除安装自定义覆盖图的功能](https://www.xda-developers.com/rootless-custom-themes-android-p/)，社区可以在几分钟内修复这个问题。

接下来是在 Pixel 支架上解锁设备的能力。如果你需要在你的设备上访问谷歌助手无法做到的东西，你需要解锁你的手机。由于没有面部解锁功能，最快的解锁方式是通过背面的指纹扫描仪。不幸的是，Pixel Stand*刚好*高，足以部分遮挡后面的指纹扫描仪。在把手指放在上面之前，你必须把设备向前抬起一点——在我看来有点尴尬。

**严重程度:*中等***

**谷歌回应:*无***

**修复到来的可能性:*前一个问题中等，后一个问题不可能***

* * *

## 软件

### 问题#11 -随机刻痕

我觉得这个问题很搞笑，因为它很荒谬。当中兴通讯为一款有两个凹槽的设备提出了一个[设计概念](https://www.xda-developers.com/zte-iceberg-two-display-notch/)时，当谷歌通过在开发者选项中添加一个“双显示屏剪切”覆盖层承认了一款有两个凹槽的设备的可能性时，我们都笑了。这个问题首先被 [*PiunikaWeb*](https://piunikaweb.com/2018/10/20/pixel-3-user-notices-two-additional-notches-with-unusual-placement/) 发现，在 Reddit 上有[少数](https://www.reddit.com/r/GooglePixel/comments/9puj6k/one_notch_wasnt_enough_phone_is_randomly_adding/) [用户](https://www.reddit.com/r/GooglePixel/comments/9pu2qa/google_decided_i_needed_to_notch_that_ass_up/)报告屏幕上出现了一个神秘的第二刻痕覆盖图。我们不确定为什么有些用户会出现这种情况，但这可能与改变 Android 方向的问题有关。

要解决此问题，您只需重新启动设备。幸运的是，这个 bug 非常罕见(我从未遇到过)，而且非常容易修复。

**严重程度:*非常低***

**谷歌回应:*一个修复即将到来***

**修复到来的可能性:*已确认***

* * *

### 问题# 12——YouTube 视频没有居中，还有其他一些奇怪的地方

如果你是第一次使用带凹槽的设备，你应该知道大多数视频应用程序*并不真正在凹槽区域显示内容。如果你放大视频使其全屏，他们*可以*这样做，但否则，大多数 16:9 纵横比的视频不会占据整个屏幕。在 YouTube 应用中，视频是偏离中心的，如下图 [MKBHD 的视频](https://youtu.be/Lg9N8XAZ6u4?t=459)所示。在 Instagram 的 Stories、Yahoo Fantasy 和 YouTube Studio 等应用程序的其他部分，凹口区域[没有得到有效利用](https://youtu.be/E67Klqw2H-E?t=551)。*

虽然这些都是应用程序本身的问题，但这些问题仍然会影响 Pixel 3 XL 的用户体验。例如，OnePlus 6 上的 OxygenOS 可以让你选择应用程序在每个应用程序的基础上如何使用 notch。我们知道谷歌不喜欢干涉应用程序的工作方式，除非它是新平台限制或命令的一部分，但依赖应用程序为有缺口的设备更新自己需要一些时间。

**严重程度:*非常低***

**谷歌回应: [*一个修正即将到来*](https://youtu.be/E67Klqw2H-E?t=540) ，至少对于 YouTube 应用**

**修复到来的可能性:*仅适用于 YouTube***

* * *

### 问题#13 -语音匹配解锁消失

Android 5.0 Lollipop 引入了一套名为“智能锁”的功能，当你拿着设备时，当你在受信任的位置时，当你连接到受信任的设备时，或者当你的声音通过语音匹配被识别时，你可以自动解锁设备。最早由 *[PiunikaWeb](https://piunikaweb.com/2018/10/19/psa-you-cant-unlock-pixel-3-by-saying-ok-google/) 报道的通过语音匹配解锁你的设备已经被移除。*我们不确定谷歌为什么取消了这项功能，但根据我的经验，解锁设备的方式总是不一致。我并不怀念这个特性，但如果你经常使用它，我不会责怪你感到不安。不过，我确实认为这将是一个有用的功能，尤其是因为谷歌正在推动用户获得 Pixel 支架。

**严重性:*低***

**谷歌回应:*无***

**修复到来的可能性:*低***

* * *

### 问题# 14-Android Auto 没有音频

对于那些使用 Android Auto head 单元的人来说，你可能以前处理过一些错误。据 [*PiunkaWeb*](https://piunikaweb.com/2018/10/22/pixel-3-users-reporting-audio-issues-with-android-auto/) 援引安卓汽车用户社区和 Reddit 上的多个论坛帖子报道，Pixel 3 的音频输出存在缺陷，导致连接到安卓汽车设备时无法播放音乐。幸运的是，谷歌已经承认了这个问题，并已经计划推出 Google Play 服务的更新来解决这个问题。

**严重程度:*中等***

**谷歌回应: [*一个修复即将到来*](https://productforums.google.com/forum/#!topic/android-auto/4dxwjPxHuKo;context-place=topicsearch/%22pixel%24203%22%2420%22Android%2420auto%22%7Csort:date)**

**修复到来的可能性:*已经确认***

* * *

### 问题# 15-O2、Three 或英国沃达丰没有 Wi-Fi 通话，但美国美国电话电报公司获得了支持

[O2](https://twitter.com/O2/status/1052609868471898112) 、 [Three](https://twitter.com/ThreeUKSupport/status/1052162000531410945) 、英国[沃达丰](https://twitter.com/VodafoneUK/status/1051840444706025472)都已经确认(通过[*PiunikaWeb*](https://piunikaweb.com/2018/10/19/pixel-3-wifi-calling-support-heres-what-we-know-so-far/))Pixel 3 还不支持 Wi-Fi 通话。运营商认证总是很混乱，但我们希望谷歌与更多运营商合作，以确保 Pixel 3 在支持的运营商上提供所有连接选项。不过，美国的 Pixel 粉丝也有一线希望，他们希望有更好的连接。Pixel 3 [支持 Wi-Fi 通话 via AT & T](https://www.reddit.com/r/GooglePixel/comments/9p8cds/pixel_3_xl_supports_wifi_calling_on_att/) 最后。

**严重程度:*中低***

**谷歌回应:*无***

**修复到来的可能性:*中-* *AT & T Wi-Fi 通话支持是一个好迹象，表明谷歌正在努力改善连接功能***

* * *

## 显示

### 第 16 期-还没有网飞·HDR

由于“高度优化的软件解码器和定制渲染堆栈”，去年的谷歌 Pixel 2 能够以高达 1080p 的速度播放 YouTube 上的 HDR 视频[。今年的 Pixel 3 能够在 YouTube 上播放 1440p HDR 视频(通过](https://www.xda-developers.com/google-youtube-hdr-support-pixel/) [*Reddit*](https://www.reddit.com/r/GooglePixel/comments/9ple4o/fyi_on_the_pixel_3_xl_you_can_now_watch_1440p_hdr/) )，因为显示器符合 HDR 输出的必要指标，同时该设备的高通骁龙 845 芯片组具有原生 HDR 解码支持。Pixel 3 和 Pixel 3 XL 符合 [UHD 联盟](https://alliance.experienceuhd.com/uhd-mobile-hdr-premium-features)对 HDR10 的指导方针，是 Y [ouTube 签名设备](https://devicereport.youtube.com/)。然而，这些设备还没有得到网飞的认证，所以它们不能播放网飞·HDR 的视频，尽管它们在技术上是有能力的。

**严重性:*低***

**谷歌回应:*网飞 HDR 支持即将到来***

**修复到来的可能性:*已确认***

* * *

### 问题#17 -黑色粉碎

如果你去年听说过 Pixel 2 XL 的显示困境，你可能听说过暂时的图像残留(通过偶尔改变导航栏背景色来解决)，暗淡的颜色(通过添加更饱和的显示模式来解决)，以及“黑色挤压”根据我们的显示器分析师 [Dylan Raga](https://www.xda-developers.com/author/dylan-raga/) 的说法，black crush 问题简单地说就是“使更深的灰色阴影看起来与黑色相同，没有提供视觉区别，并且对更暗的场景提供低对比度”。许多人将这个问题归因于去年 Pixel 2 XL 中 LG OLED 面板的使用，就个人而言，这是我的 Pixel 2 XL 的一个大问题。黑屏问题使得该设备在低亮度水平下使用非常不舒服。虽然我的 Pixel 3 XL 审查单元没有像我的 Pixel 2 XL 那样明显地显示黑色挤压问题，但我们的显示器分析师和几位早期采用者确实报告说它仍然存在。您的里程可能会有所不同。

**严重程度:*中低***

**谷歌回应:*无***

**修复到来的可能性:*无***

* * *

### 问题#18 -某些用户的“粉红色着色”

一些用户报告说，非 XL Pixel 3 显示器的底部带有粉红色。[多个](https://www.reddit.com/r/GooglePixel/comments/9pkhsn/google_says_half_pink_screen_is_normal/) [线程](https://www.reddit.com/r/GooglePixel/comments/9pd2np/pixel_3_screen_quality_uniformity_issues_and_pink/) [关于](https://www.reddit.com/r/GooglePixel/comments/9pf31q/pixel_3_smaller_terrible_screen_quality_darkpink/) [Reddit](https://www.reddit.com/r/GooglePixel/comments/9ppsom/display_backlight_brighter_on_lower_half_of/) [有](https://www.reddit.com/r/GooglePixel/comments/9qr7qa/another_my_experience_with_the_pixel_3_nonxl_not/) [被](https://www.reddit.com/r/GooglePixel/comments/9pe7n6/got_my_pixel_3_love_it_but_screen_uniformity/) [发表过](https://www.reddit.com/r/GooglePixel/comments/9p3zao/people_reporting_that_the_top_half_of_the_pixel_3/)的问题。我们的显示器分析师表示，他们在看到的两款 Pixel 3 设备上都没有看到任何粉红色，因此这可能是某些面板的个别问题。

**严重程度:** ***中低***

**谷歌回应:** ***无***

**一个修正来临的可能性:** ***无***

*感谢[d staley](https://disqus.com/by/dstaley/)*

* * *

## 如何向 Google 发送反馈

所以，你发现你的谷歌像素 3 或谷歌像素 3 XL 的问题，你想让你的声音被听到。你可以在 Reddit 或 XDA 上发表帖子，然后*希望*来自谷歌的人会回复，但是有更好的方式给谷歌反馈。

### 直接反馈

[**谷歌推特账号**发推文](https://twitter.com/madebygoogle)

[**在像素用户社区产品论坛上发帖**](https://productforums.google.com/forum/#!forum/phone-by-google)

您也可以直接从您的设备发送反馈报告。谷歌甚至[制作了一个视频](https://www.youtube.com/watch?v=mlGSrsYhhk4)向你展示如何做！

### 间接反馈

如果你真的想在风中呼喊，你可以在我们下面的论坛上这样做。有许多有用的、知识渊博的用户可能会回答你的问题，或者教你如何自己解决问题。

[**加入谷歌 Pixel 3 论坛**](https://forum.xda-developers.com/pixel-3)

[**加入谷歌 Pixel 3 XL 论坛**](https://forum.xda-developers.com/pixel-3-xl)

### 杂项问题

最后，如果你遇到一个你认为可能是 Android Pie 问题的软件问题，使用 Google 问题跟踪器并在正确的组件下提交错误报告。

[**在 Google Issue Tracker 上提交 Bug 报告**](https://issuetracker.google.com/components)