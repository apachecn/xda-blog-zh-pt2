# 轻按，轻按端口 iOS 14/Android 11 的后退轻按手势到任何 Android 设备

> 原文：<https://www.xda-developers.com/tap-tap-brings-ios-14-android-11-back-tap-gesture-any-android-device/>

**更新 1 (08/02/2020 @ 04:27 PM ET)** :自从我们最初报道以来，Tap，Tap 应用程序已经收到了两次更新，带来了许多新功能。滚动到底部了解更多信息。下面保留了 2020 年 7 月 30 日发表的文章。

在二月份发布第一个 Android 11 开发者预览版后，我们得知谷歌正在开发一套代号为“哥伦布”的新手势。这项功能让你可以在 Pixel 手机的背面双击[来执行诸如启动谷歌助手、启动谷歌相机应用程序、控制媒体播放等操作。在 Android 11 开发者预览版 2 中，谷歌继续对这些手势进行研究，增加了](https://www.xda-developers.com/google-pixel-android-11-double-tap-rear-gestures/)[新动作](https://www.xda-developers.com/google-pixel-3-pixel-4-double-tap-gestures-android-11-screenshots-recents/)，用于截图和打开最近的应用概述。然而，这些手势仍然对 Pixel 用户隐藏，在随后的 Android 11 测试版中，这些手势被完全删除。令人欣慰的是，开发者 Kieron Quinn，在我们的论坛上也被称为 [Quinny899](https://forum.xda-developers.com/member.php?u=3563640) ，设法移植了这个功能，所以它基本上可以在任何 Android 设备上工作。

他的新应用名为 Tap，Tap，为任何运行 Android 7.0 Nougat 及更高版本的 ARMv8 设备带来了双背轻击手势。在我上面嵌入的演示视频中，我双击了我的 [Pixel 4](https://forum.xda-developers.com/pixel-4) 的背面来启动相机应用程序。[在这个视频](https://streamable.com/4jd1mu)中，开发者 Kieron Quinn 通过双击他的[一加 7T Pro](https://forum.xda-developers.com/7t-pro) 的背部来启动一加相机应用。然而，启动相机应用程序并不是 Tap 的全部功能。使用辅助功能服务，Tap，Tap 可以识别您何时点击 Android 手机的背面，然后执行某些操作，如模拟家庭、最近的应用程序或后退按钮。

Tap，Tap 使用与谷歌训练的相同的机器学习模型来识别 [Pixel 3 XL](https://forum.xda-developers.com/pixel-3-xl) 、 [Pixel 4](https://forum.xda-developers.com/pixel-4) 和 [Pixel 4 XL](https://forum.xda-developers.com/pixel-4-xl) 背面的双击。这意味着当使用这三款手机中的任何一款或尺寸相似的设备时，它都会工作得最好。因此，你的里程数可能会因 Tap 的识别效果而异，Tap 识别双击(特别是当你戴着厚厚的外壳时)，但我已经设法在华硕 ROG 手机 3 和华为 P40 Pro 上完成了这项工作。这款应用不需要特殊的硬件或软件版本，因为它所做的只是读取设备的加速度计和陀螺仪传感器的变化。谷歌训练了机器学习模型，以识别当你点击设备后部时发生的加速度计和陀螺仪传感器读数，同时高通和低通滤波器用于进一步提高灵敏度。那么，理论上，这项功能或类似的功能将在任何具有 ML 模型的设备上运行良好，这很可能是它在运行 iOS 14 的[苹果设备上的工作方式，以及当](https://www.theverge.com/2020/6/23/21300157/ios-14-hidden-feature-back-tap-accessibility-custom-commands)[小米在 MIUI 12](https://www.xda-developers.com/xiaomi-miui-12-back-double-triple-tap-gestures-apple-ios-14-google-pixel-phones/) 中为一些设备推出它时的工作方式。

## 轻按，轻按-任何安卓手机的安卓 11/iOS 14 后退轻按手势！

安装应用程序后，您必须在“设置”中启用辅助功能服务。启用后，你必须在手势设置中选择一个设备型号。有 3 个设备模型对应于 Google 为 Pixel 3 XL、Pixel 4 和 Pixel 4 XL 训练的 3 个 TensorFlow Lite 模型。该应用的手势设置中显示了一个灵敏度设置，但这将在该应用的未来版本中完全实现。

在“操作”下，你可以选择双击设备背面时会发生什么。您可以在此列出多个操作，但点击只会优先运行最上面的操作。如果该操作由于某种原因未能运行，则运行列表中的下一个操作。开发人员计划给动作添加入口，这样当某些动作被执行时，你就可以阻塞。他还计划在未来的版本中添加 Tasker 集成。

在“门”部分，您可以选择哪些条件会阻止双击手势执行动作。例如，如果启用了“显示关闭”的门，那么当屏幕关闭时，Tap 将不会执行操作。最后，反馈设置让您可以控制设备是否振动，以及设备是否在执行某个操作时被唤醒。

Tap，Tap 是一个开源的 app，所以你可以在 GitHub 上关注它的开发。第一个 alpha 版本现在可以在下面链接的 XDA 论坛上下载。试用一下，让我们知道它在您的设备上的效果如何！

**[轻点，轻点 XDA 论坛线程](https://forum.xda-developers.com/android/apps-games/app-tap-tap-double-tap-device-gesture-t4140573)| |**|**[GitHub 上的源代码](https://github.com/KieronQuinn/TapTap)**

* * *

## 更新:版本 0.2 和 0.3 增加了音乐控制，Tasker 集成，等等

自从我们几天前报道 Tap，Tap 应用程序以来，读者对它的反应非常积极。结果，开发人员被鼓励添加一些高度要求的和计划的特性。版本 0.2 阿尔法和 0.3 阿尔法增加的行动，包括音乐控制，音量控制，唤醒设备，快捷方式，直接拨打联系人，并触发任务事件。最后一个允许你用 Tap 做任何你想做的事情，因为 Tasker 是一个非常强大的自动化应用程序。这里有一个来自 Tasker 开发者的简短演示，展示了你可以用它做的一些事情。

### **轻点，轻点更新变更日志**

版本 0.2 Alpha 变更日志:

*   增加了 Tasker 集成，将事件类型作为一个插件(感谢 joaomgcd)和启动特定任务(需要许可，应用程序会带你通过)-这些都在高级类别下
*   增加了音乐控制动作:播放/暂停，快进快退(感谢 timfedo)
*   改进了 MD2 风格的用户界面(感谢 gcantoni)
*   修正了相机启动捕捉界面而不是普通界面的问题(你现在可能会看到一个选择器，如果你想这样做而不想这样做，请将操作改为启动应用程序>你最喜欢的相机应用程序)
*   当不可配置的门已经在列表中时，防止添加
*   增加了屏幕打开时的门
*   增加了音量调高、调低、切换静音和音量面板动作
*   添加了唤醒设备操作
*   修复了 Android 7 和 8 的崩溃问题，希望如此

版本 0.3 Alpha 变更日志:

*   实际上将 Tasker 移到了高级，任务选项现在应该可用了。很抱歉在 alpha 0.2 中出现这种情况。
*   更多 MD2 风格的用户界面变化(感谢乔治·坎通尼)
*   当安装了 XDA 应用程序时，除了 XDA 链接，切换到 Chrome 自定义标签的链接(感谢乔治·坎通尼)
*   简体中文(感谢 hjthjthjt)、俄语(感谢费多尔·沙托欣)、巴西葡萄牙语(感谢罗德里戈·索萨)、中文(感谢 Kevin Kung)和乌克兰语(Petro Bilyi)的翻译
*   添加了一个启动“传统”启动器快捷方式的动作，例如谷歌地图方向
*   添加 CALL_PHONE 权限作为一个完全可选的权限，纯粹是为了支持一个绝对疯狂的人将手势映射到“直拨”启动器快捷方式的能力，这需要该权限。如果你真的想这么做，你必须手动授权，应用程序通常不会**请求授权。**

你可以从之前链接的 XDA 论坛帖子或者开发者的 GitHub 页面下载 Tap。