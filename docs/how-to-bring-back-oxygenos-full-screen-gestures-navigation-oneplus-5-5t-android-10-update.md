# 在运行 Android 10 的 OnePlus 5/5T 上还原一加的全屏手势

> 原文：<https://www.xda-developers.com/how-to-bring-back-oxygenos-full-screen-gestures-navigation-oneplus-5-5t-android-10-update/>

在[短暂的测试阶段](https://www.xda-developers.com/oneplus-5-oneplus-5t-android-10-oxygenos-open-beta-1/)之后，一加[最近以 OxygenOS 10 的形式推出了](https://www.xda-developers.com/oneplus-5-5t-stable-android-10-oxygenos-10-update/)稳定的 Android 10 更新，用于 2017 年的 OnePlus 5 和 OnePlus 5T。除了引入像[游戏空间](https://www.xda-developers.com/oneplus-game-space-google-playadds-game-statistics-instant-games/)这样的功能，该公司还引入了一个经过修改的手势机制。许多 OnePlus 5/5T 用户在 OxygenOS 10 更新后发现原来的一加全屏手势实现不见了，他们并不高兴。不要担心，因为 XDA 资深成员 [Pierre02](https://forum.xda-developers.com/member.php?u=7129658) 已经发现了一个简单的技巧来恢复 OnePlus 5 和 5T 上的旧手势。

**[一加 5 XDA 论坛](https://forum.xda-developers.com/oneplus-5) ||| [一加 5T XDA 论坛](https://forum.xda-developers.com/oneplus-5t)**

事实证明，一加对全屏手势的实现(最初是通过基于 Android Oreo 的 [OxygenOS Open Beta 5/3](https://www.xda-developers.com/oxygenos-open-beta-5-3-oneplus-5-5t/) 登陆的)仍然在新的固件中。它只是在常规设置中隐藏，但如果你启用隐藏首选项，它仍然是全功能的，这是我们论坛上的用户发现如何做的。好的一面是，root 访问不是执行这些步骤的强制条件。

你所需要做的就是得到一个允许你改变 Android 设置数据库中的值的应用程序，比如 [SetEdit](https://play.google.com/store/apps/details?id=by4a.setedit22) 。安装应用程序后，导航到“系统表”并搜索名为`op_gesture_button_side_enabled`的变量。这是一个布尔标志，因此将其值设置为`0`会立即恢复旧的全屏手势。如果您需要恢复新的实现，只需将值设置为`1`。

以下是那些老式一加风格的全屏幕手势的工作方式:

*   **返回:**从左下方/右侧向上滑动
*   **主页:**从底部(中间)向上滑动
*   **最近的应用:**向上滑动并从底部(中间)按住

**[在 OnePlus 5/5T 运行 OxygenOS 10 上还原一加手势——XDA 讨论线程](https://forum.xda-developers.com/oneplus-5t/how-to/how-to-oneplus-gestures-oneplus-5t-t4101311)**

快速回顾一下，谷歌确实在 Android 10 中引入了他们自己的全屏手势。他们甚至在 Android 10 中强制包含这些手势，但原始设备制造商仍被允许提供他们自己的手势。我们希望一加将来能在他们的 OxygenOS 皮肤中添加一个简单的开关，让最终用户能够自由地在不同的手势风格之间切换。

[app box Google play " by4a . setedit 22 "]