# Android Pie 为 Xbox One 的无线控制器添加了控制器映射

> 原文：<https://www.xda-developers.com/android-pie-controller-mapping-fix-xbox-one-s/>

# Android Pie 为 Xbox One 的无线控制器添加了控制器映射

Xbox One S 控制器的蓝牙确实可以连接到 Android 设备，但它在按钮映射方面存在问题。Android Pie 解决了这个问题。

如果你看看 Play Store 和 iOS App Store 中的类别，你会注意到一件事:游戏类别在这两个平台上都是最受欢迎的。这是事实，原因有很多，但它们都必须以第一代 iPhone 和第一代 Android 智能手机发布时没有人想到的方式成熟。Android 上的下一级游戏的一个大缺点是缺乏控制器支持，但现在 Android 9 Pie 终于为 Xbox One S 的无线控制器添加了控制器映射支持。

几年前，微软发布了 Xbox One 控制器，它实际上包含了蓝牙，而不是一些专有的无线技术。这让许多移动 Android 游戏玩家感到高兴，因为这是他们离开有线电缆改编的答案。就我个人而言，我一直在使用一种 Nyko 塑料夹，它可以让你卡入控制器，并在其上插入智能手机。然后你需要插上这两个设备，它才能工作。虽然它在受支持的游戏中确实有效，但它远非完美。

Xbox One S 控制器增加的蓝牙功能确实可以连接到 Android 设备，但[一些游戏的按钮映射存在问题](https://www.androidpolice.com/2016/08/11/psa-the-new-bluetooth-enabled-xbox-one-controller-works-with-android-but-not-very-well/)。在游戏 *Android Police* 测试中，按钮映射似乎无处不在，没有任何意义。所以安卓爱好者很快就去了谷歌的问题追踪器[让公司知道发生了什么](https://issuetracker.google.com/issues/37115804#comment41)。这个 bug 报告从 2016 年 8 月一直持续到昨天，2018 年 8 月 22 日，一名谷歌工程师最终将其标记为已修复。

开发人员说“这个 bug 应该在 P 中修复”，因此他们将这个 bug 报告标记为已修复。在 AOSP 更新的这个新的按键布局的[提交应该会出现在 Android 9 的所有版本中。派。你的 Android 设备使用 Xbox One S 控制器吗？Android Pie 中的按钮映射效果更好吗？](https://android.googlesource.com/platform/frameworks/base/+/46429ecd938b4b87dd8d05294fd5b267bd8871e5)