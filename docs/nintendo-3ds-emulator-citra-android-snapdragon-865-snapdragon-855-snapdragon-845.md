# 任天堂 3DS 模拟器 Citra 在骁龙 865，855 和 845 上测试

> 原文：<https://www.xda-developers.com/nintendo-3ds-emulator-citra-android-snapdragon-865-snapdragon-855-snapdragon-845/>

Citra 是任天堂最受欢迎的 3DS 模拟器，[上周在谷歌 Play 商店正式发布，其性能一直是人们谈论的焦点。我相信任何看过它发布的人都想知道他们是否可以在他们的 Android 智能手机或平板电脑上玩他们最喜欢的任天堂 3DS 游戏，所以我在过去几天里在由多个不同 SOC 驱动的各种不同设备上玩游戏，看看你可以从你的设备上获得什么样的性能。](https://www.xda-developers.com/official-citra-for-android-released/)

我测试了以下热门的任天堂 3DS 游戏:

*   动物穿越:新的一页
*   马里奥赛车 7
*   口袋妖怪 X/Y
*   塞尔达传说:世界之间的链接
*   火的象征:命运
*   超级马里奥 3D 世界

...在以下 Android 智能手机上:

...结果相当复杂。我用非官方的雪铁龙 MMJ 版本和刚刚在谷歌 Play 商店发布的官方雪铁龙 3DS 模拟器测试了这些 3DS 游戏。一些结果令人惊讶。请注意，所有这些测试都是在禁用音频拉伸的情况下进行的，因为我发现启用音频拉伸时，性能会受到相当大的影响，但好处却很少。请记住，不同的 GPU 驱动程序版本也可能会影响性能，因此一台采用特定芯片组的设备的性能可能不同于另一台采用相同芯片组的设备。

 <picture>![Citra for Android Nintendo 3DS emulator](img/5ec1ca908cee6de73270c17dd7355b95.png)</picture> 

Nintendo 3DS emulation using the official Citra for Android port. Left to right: OnePlus 8 Pro, OnePlus 6, Realme 6 Pro.

**注:通过转储和解密你自己的任天堂 3DS 游戏，你可以合法地为你的智能手机获取 3DS ROMs。为此，你需要一个被黑掉的任天堂 3DS 和一个你想玩的合法购买的 3DS 游戏。**

* * *

## 目前的性能问题与任天堂 3DS 仿真通过 Citra 为 Android(和潜在的修复)

在详细介绍前面提到的任天堂 3DS 游戏在各种 Android 智能手机上的性能之前，值得一提的是，目前，Citra 3DS emulator port for Android 不支持着色器缓存。着色器缓存只是一个文件缓存，用于跟踪游戏中显示的已编译着色器，拥有一个着色器缓存可以大大降低 CPU 和 GPU 的负载。当在 Citra 中遇到新的着色器时，它们会被编译，而不会保存到存储中。这意味着它们不能被缓存，而是每次遇到都必须重新编译。这就是为什么目前 Android 上的 Citra 在玩一些 3DS 游戏时会相当口吃。PC 上的 Citra 支持着色器缓存，用户想要下载预编译的着色器缓存以避免缓慢而费力地生成自己的着色器缓存是很常见的。此外，我发现禁用音频拉伸对性能有一点帮助。

* * *

## **任天堂 3DS 仿真性能——高通骁龙 865、855、845、720G、麒麟 980**

### **高通骁龙 865**

**动物穿越:新叶-一加 8 Pro**

*官方雪铁龙*

*   大多是 60 帧/秒
*   经常丢帧，尤其是摇晃树木掉落果实时
*   音频通常会暂停一秒左右，当音频暂停时，游戏也会暂停一秒

*MMJ/非官方的雪铁龙*

*   30 FPS 到 45 FPS，偶尔峰值达到 60 FPS
*   没有音频挂起
*   整体体验更加一致，尽管速度较慢
*   试图出售物品将冻结游戏，这不会发生在官方的雪铁龙建设

**马里奥赛车 7 -一加 8 职业版**

*   以每秒 60 帧的速度完美运行
*   偶尔的音频提示会导致轻微的口吃
*   官方建筑和 MMJ 建筑在性能上没有区别

**口袋妖怪 X/Y -一加 8 Pro**

*   不是一个非常密集的游戏，完美地运行在 30 帧/秒(这个游戏运行在 30 帧/秒的超负荷)
*   战斗完美进行
*   音频听起来很棒，音乐是 AAC 格式的，现在可以解码了
*   官方建筑和 MMJ 建筑在性能上没有区别

*注意:上面视频中看到的闪烁只发生在我进行屏幕录制时。*

**塞尔达传说:世界之间的链接——OPPO Find X2 Pro/一加 8 Pro**

*   运行完美，没有减速
*   音频很棒
*   战斗中偶尔口吃
*   过场动画作品
*   官方建筑和 MMJ 建筑在性能上没有区别

**火徽缘分- OPPO 找 X2 Pro**

*   进入战斗时有些减速
*   一些战斗中的音频口吃
*   音频效果很好
*   过场动画作品
*   这款游戏大部分时间都在全速运行，而在 MMJ 的版本中却没有

* * *

### **高通骁龙 855**

**动物穿越:新叶- OPPO Reno 10x 变焦**

*官方雪铁龙*

*   运行近乎完美
*   很少口吃
*   几乎没有音频延迟

*MMJ/非官方的雪铁龙*

*   从 30 到 60 帧/秒的任何地方，虽然大多是向高端发展
*   很少口吃
*   几乎没有音频延迟
*   试图出售物品将冻结游戏，这不会发生在官方的雪铁龙建设

**马里奥赛车 7 - OPPO 雷诺 10x 变焦/一加 7 Pro**

*   运行近乎完美
*   几乎没有音频延迟
*   几乎没有口吃
*   官方版本和 MMJ 版本之间没有性能差异

**口袋妖怪 X/Y - OPPO Reno 10x 变焦**

*   不是一个非常密集的游戏，完美地运行在 30 帧/秒(这个游戏运行在 30 帧/秒的超负荷)
*   战斗完美进行
*   音频听起来很棒，音乐是 AAC 格式的，现在可以解码了
*   官方建筑和 MMJ 建筑在性能上没有区别

**塞尔达传说:世界之间的链接——OPPO Reno 10x 变焦**

*   运行近乎完美
*   几乎没有音频延迟
*   战斗中偶尔口吃
*   官方版本和 MMJ 版本之间没有性能差异

* * *

### **高通骁龙 845**

**动物穿越:新叶-一加 6**

*官方雪铁龙*

*   大多是 50-60 帧/秒
*   非常频繁地掉落框架，特别是在摇晃树木掉落果实时，但在许多其他情况下也是如此
*   音频通常会暂停一秒左右，当音频暂停时，游戏也会暂停一秒

*MMJ/非官方的雪铁龙*

*   大约 30-60 FPS，大部分时间停留在 45 FPS 左右
*   减少丢帧的频率
*   音频偶尔会断断续续

**马里奥赛车 7 -一加 6**

*   导航菜单时口吃
*   在比赛中 50-60 FPS，尽管波动很大，有时低至 30 FPS
*   偶尔出现音频口吃

**口袋妖怪 X/Y - OnePlus 6**

*   不是一个非常密集的游戏，完美地运行在 30 帧/秒(这个游戏运行在 30 帧/秒的超负荷)
*   战斗完美进行
*   音频听起来很棒，音乐是 AAC 格式的，现在可以解码了
*   官方建筑和 MMJ 建筑在性能上没有区别

**塞尔达传说:世界之间的链接——一加 6**

*   在 40-60 FPS 范围内保持一致
*   战斗中有很多口吃
*   MMJ 版本的性能比官方版本稍好

* * *

### **高通骁龙 720G**

**动物穿越:新叶- Realme 6 Pro**

*官方雪铁龙*

*   大多是 50-60 帧/秒
*   偶尔会掉帧，特别是摇晃树木掉落果实时，但在许多其他情况下也是如此
*   音频通常会暂停一秒左右，当音频暂停时，游戏也会暂停一秒
*   MMJ 和官方建筑在这里或多或少表现相同

**口袋妖怪 X/Y - Realme 6 Pro**

*   以 30 FPS 的速度运行基本上是完美的，尽管偶尔性能会下降
*   战斗完美进行
*   音频听起来很棒，音乐是 AAC 格式，现在可以解码，最少的口吃
*   官方建筑和 MMJ 建筑在性能上没有区别

**塞尔达传说:世界之间的链接——一加 6**

*   在 40-60 FPS 范围内保持一致
*   战斗中有很多口吃
*   MMJ 版本的性能比官方版本稍好

* * *

### **麒麟 980**

Honor 20 Pro 及其海思麒麟 980 无法运行我在任何可玩帧率下测试的任何任天堂 3DS 游戏。由于驱动程序问题，官方和非官方的 Citra 3DS 模拟器并不真正支持采用非骁龙芯片组的设备，因此，这意味着采用 Exynos 处理器的三星智能手机在玩这里列出的任何 3DS 游戏时也可能会遇到问题。

* * *

## 结论-任天堂 3DS 仿真是非常可行的(对于大多数旗舰)

奇怪的是，我发现性能最好的不是高通骁龙 865，而是高通骁龙 855。有可能 Citra 主要是在高通骁龙 855 设备上开发的，因为高通骁龙 865 [是一个相对较新的版本](https://www.xda-developers.com/qualcomm-snapdragon-865-processor-specifications-features/)，但这只是我的猜测。一加 7T Pro 和 OPPO Reno 10x Zoom 中的骁龙 855 可以完美地处理我扔给它的几乎所有任天堂 3DS 游戏，这给我留下了深刻的印象，游戏本身非常可玩。高通骁龙 720G 的表现也令人难以置信，与骁龙 845 的结果大致相同。

[**Citra(任天堂 3DS 模拟器)网站**](https://citra-emu.org/)