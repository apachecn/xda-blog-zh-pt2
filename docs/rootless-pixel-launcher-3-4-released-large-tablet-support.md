# 无根 Pixel Launcher 3.4 发布，支持大型平板电脑，支持 Android for Work 功能，增加了 Android Go 优化版本，等等

> 原文：<https://www.xda-developers.com/rootless-pixel-launcher-3-4-released-large-tablet-support/>

Pixel Launcher 于 2016 年与谷歌 Pixel 和 Pixel XL 一起推出。官方称，该启动器仅在谷歌 Nexus 和 Pixel 设备上受支持，但其 APK 可以安装在许多其他设备上。然而，问题是，如果启动器安装在不支持的设备上，最左侧屏幕上的 Google feed 面板就无法工作。为了解决这个问题，一位名叫阿米尔·扎伊迪的开发人员将 Pixel Launcher 功能移植到了 AOSP launcher (Launcher3)上。

开发人员重复了他的工作,他发布了无根 Pixel Launcher 3.0，带有谷歌 feed 面板和谷歌 Pixel 2 更新版 Pixel Launcher 的功能。XDA 资深成员 [paphonb](https://forum.xda-developers.com/member.php?u=6018897) 也发布了无根 Pixel Launcher，但两个端口的区别在于，Amir 从 AOSP 移植了 Pixel Launcher 特性到 Launcher3，而不是将 Launcher 建立在原始 Pixel Launcher APK 的基础上。

不同的实现意味着新的特性可以很容易地在 Amir Zaidi 的端口上实现。开发者还在无根 Pixel Launcher 3.0 中加入了大量额外功能。

现在，Amir 发布了无根 Pixel Launcher 3.4(已经测试了一个月)，列出了一大堆错误修复。值得注意的是，版本更新带来了更大的图标和搜索栏，使用 Pixel C 配置文件的大屏幕支持。Android for Work 现在支持应用程序隐藏、启用或禁用图标包以及应用程序搜索。还有一个特殊的 Android Go 版本，可以使用 Android Studio 或使用自定义 ROM 构建脚本来构建。开发者提到，应用预测将“更少切换”，默认的主屏幕设置现在与真正的像素启动器具有相同的设置。此外，如果系统上没有安装 Google 应用程序，但找到了 Google Go，用户可以通过点击搜索栏来启动 Google Go 搜索。

完整的变更日志详述如下:

### 变更日志

**特性**

*   使用 Pixel C 配置文件，通过更大的图标和搜索栏增加了对大平板屏幕的支持
*   麦克风图标在与真实像素启动器相同的条件下显示:当使用 Now on Tap 时
*   如果没有安装 Google 应用程序，但找到了 Google Go，单击搜索栏将会启动搜索
*   重音符号从搜索中去除，因此在应用程序抽屉中搜索应用程序更容易
*   小部件可以在网格上任何大于 1 的方向上调整大小
*   应用程序预测将更少变化
*   默认的主屏幕设置反映了真正的 Pixel Launcher 现在的设置:电话、信息、Gmail、商店、浏览器、相机
*   Android Work 支持应用程序隐藏、图标包启用/禁用和应用程序搜索
*   文本更新至 8.1 版本一览
*   在 Lollipop 上，应用程序抽屉状态栏的背景略暗，以便更容易看到白色图标
*   构建工具经过更新，构建时性能稍有提高
*   Android Go 版本可以使用 Android Studio 或使用自定义 ROM 构建脚本来构建

**Bug 修复**

*   当几乎所有应用程序都隐藏时搜索应用程序不会导致崩溃
*   当拖动一个图标出来，然后悬停在它上面一瞬间，hotseat 中的文件夹会正确关闭
*   后端口应用程序快捷方式(7.1 之前)仅在快捷方式真正工作时显示
*   后端口应用程序快捷方式可以放在主屏幕上而不会消失
*   打开应用程序抽屉总是会淡出主屏幕，即使在切换页面时也是如此
*   向下滑动应用抽屉搜索时，键盘会立即关闭
*   从搜索中拖动图标时，棒棒糖键盘关闭
*   在没有安装谷歌应用程序和浏览器的情况下点击搜索栏时，将显示“应用程序未安装”的消息
*   Google Feed 无法从应用抽屉的左上角打开
*   当长按文件夹中的应用程序时，文件夹不会导致所有应用程序都扭曲到屏幕的左上角
*   直播壁纸不能让主题选择算法崩溃
*   上下拖动应用程序抽屉时，按下主屏幕按钮不会出现故障
*   上下拖动应用抽屉时，它不会消失
*   图标包中的图标不会在更新过程中暂时消失
*   当搜索栏为空时，按下搜索时，键盘隐藏
*   无需先打开设置即可启用应用预测
*   停用所有应用程序的用户帐户不会导致其他帐户的应用程序抽屉变空
*   启动隐藏的应用程序不会计入应用程序建议算法
*   启用/禁用隐藏应用程序的图标包将立即显示结果
*   具有多个启动程序快捷方式的应用程序显示每个快捷方式的正确图标(例如 XDA 实验室)

开发者警告说，最近版本的谷歌应用程序已经破坏了随机功能，如谷歌饲料。为了避免东西被破坏，他建议用户获得 7.22 稳定版。重复的应用程序建议现在可能会显示为添加 Android 工作兼容性的副作用，但用户可以通过在启动器设置中禁用和启用他们的应用程序建议来永久修复这一问题。同样，用户需要重新隐藏他们想要隐藏的应用程序，因为隐藏需要改变存储。最后，开发人员指出，最近的华为手机似乎在启动时崩溃，因为用户没有给启动器存储权限。如果发生这种情况，建议用户通过进入设置来手动授予权限。

用户可以从 Github 下载无根 Pixel Launcher 3.4 [。谷歌 Pixel 用户必须刷新官方资料库中的“无根 Pixel Launcher”Magisk 模块。发射器的来源可在](https://github.com/amirzaidi/launcher3/releases)[这里](https://github.com/amirzaidi/Launcher3/commits/o-mr1)获得。

* * *

[**来源:/u/AmirZ**](https://www.reddit.com/r/AndroidLauncher/comments/88cdrh/rootless_pixel_launcher_34_bug_fixes_and/)