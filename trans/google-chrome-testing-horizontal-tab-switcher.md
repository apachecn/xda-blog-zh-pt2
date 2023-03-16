# 谷歌正在测试 Chrome 浏览器中用于纵向模式的水平标签切换器

> 原文：<https://www.xda-developers.com/google-chrome-testing-horizontal-tab-switcher/>

# 谷歌正在测试 Chrome 浏览器中用于纵向模式的水平标签切换器

谷歌正在测试 Chrome for Android 中一个新的横向标签切换器，当设备处于纵向模式时。以前，标签切换器在纵向模式下垂直显示标签。

谷歌非常非常喜欢他们的 A/B 测试。虽然绝大多数用户可能在 Play Store 中看到一种绿色，但另一组用户可能会看到完全不同的颜色。不过，谷歌 Android Chrome 的工作方式略有不同，因为它的开源特性和功能标志允许任何人参与该公司的公开 A/B 测试。今天，Chromium gerrit 上出现了一个新的提交，旨在改造 Android 版 Chrome 中的标签切换器。

如上图所示，当用户处于横向模式时，标签切换器显示水平排列的卡片。另一方面，当设备处于纵向模式时，选项卡垂直排列。这个[新提交](https://chromium-review.googlesource.com/c/chromium/src/+/991400)增加了一个功能标志(`chrome://flags#enable-horizontal-tab-switcher`)，当手机处于纵向模式时，总是显示水平标签切换器。提交描述指出，未来的提交将完善选项卡 UI，为“公共实验”做准备，因此很明显，谷歌打算在一部分用户身上进行 A/B 测试。

如果我们可以推测一下，我认为这种变化很好地符合了 Android P 将提供导航手势的传言。据[*9 to 5 谷歌*](https://9to5google.com/2018/03/17/alphabet-scoop-001/) 报道，下一个主要的 Android 版本将像 iPhone X 一样提供手势导航界面。我们已经看到像 OnePlus 5T [这样的手机提供类似的手势](https://www.xda-developers.com/oxygenos-open-beta-5-3-oneplus-5-5t/)，随着最近向几乎完全无边框设备的推进，如果 Android 开始原生提供这样的功能，我们不会感到惊讶。如果这个传言是真的，Chrome 中改进的水平标签切换器可能会与 Android P 中的水平最近应用程序屏幕一起出现。

* * *

## 更新:提交合并，这里有一个截图

提交被合并了，所以我们安装了最新的 Chromium 版本，看看在纵向模式下水平标签切换会是什么样子。不出所料，有点局促。我们希望它在未来的版本中有所改进。