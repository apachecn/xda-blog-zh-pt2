# 谷歌 Pixel 智能手机 Android 11 开发者预览版 2 发布

> 原文：<https://www.xda-developers.com/android-11-developer-preview-2-google-pixel-announcement-changelog/>

# Android 11 开发人员预览版 2 增加了应用程序首选的帧速率支持，重启时恢复，等等

谷歌已经宣布了适用于谷歌 Pixel 2017 和更高版本智能手机的 Android 11 开发者预览版 2。下面是对用户和开发人员来说的新内容。

尽管由新型冠状病毒引起的新冠肺炎病的传播减缓了全球经济，但许多科技公司已经让员工在家工作(WFH)。谷歌就是这样一家公司，今天，他们承认了我们世界上许多人面临的困难。今天，该公司宣布了下一个主要 Android 操作系统的新开发者预览版:Android 11。Android 11 开发人员预览版 2 和第一个开发人员预览版一样，仍然只面向开发人员，博文中提到的变化列表专注于开发人员将不得不适应的新 API 和平台行为变化。这是最新消息。

## Android 11 API 的新变化

*   **5G 状态 API:** 在 Android 11 开发者预览版 2 中，开发者可以检查用户是否在 5G 新无线电(NR)或非独立(NSA)网络上。如果你不熟悉，NSA 网络上的 5G 意味着 5G 网络是基于现有的 4G 基础设施，而 NR 网络上的 5G 网络是独立的。NR 上的 5G 通常会快得多，尽管其当前的可用性非常有限。您可以检查此状态，以更改您的应用在较低或较高网络连接下的行为。
*   可折叠设备的铰链角度:像即将推出的微软 Surface Duo、摩托罗拉 Razr、三星 Galaxy Fold/Z Flip 和华为 Mate X/Xs 这样的可折叠设备通常不止有两种状态。大多数情况下，它们要么是折叠的，要么是完全展开的，但偶尔，用户会将它们放在某个角度。Android 11 开发者预览版 2 增加了对[铰链角度传感器](https://developer.android.com/reference/android/hardware/Sensor#STRING_TYPE_HINGE_ANGLE)的支持，允许应用程序直接或通过 AndroidX 库查询铰链角度。
*   **来电过滤服务改进:**来电过滤应用现在可以报告来电拒绝原因，以通知用户该服务拒绝来电的原因。此外，来电过滤应用还可以查看来电是否来自用户联系人中的号码，当然，前提是来电过滤应用有权读取联系人。最后，呼叫筛选应用现在可以定制一个由系统提供的[后呼叫筛选对话框](https://developer.android.com/reference/android/telecom/TelecomManager.html#ACTION_POST_CALL)，让用户执行诸如将呼叫标记为垃圾邮件或将号码添加到他们的联系人等操作。
*   **对神经网络 API 的更新:**谷歌增加了一个“计算高效版本”的 [swish 激活函数](https://arxiv.org/pdf/1710.05941.pdf)(警告:PDF 链接)，允许“更快的训练时间和更高的跨各种任务的准确性”另一个补充是 Control ops“实现支持分支和循环的更高级的机器学习模型。”最后，Google 增加了“新的执行控制”来最小化常见用例的延迟。

## 隐私和安全

*   在 Android 11 中，想要从前台服务访问摄像头或麦克风数据的应用程序必须声明 manifest 属性 foregroundServiceType。
*   [作用域存储](https://developer.android.com/preview/privacy/storage)在这个新的预览版本中已经更新。现在，开发人员可以将文件“从遗留模型迁移到新的范围存储模型”还增加了“更好的缓存文件管理”

## 抛光和质量

*   ****同步 IME 转场:**** 增加了新的 API，允许开发人员在制作动画时，将应用程序的内容与输入法编辑器或 IME 和系统栏同步。这允许您创建比以前更加流畅的 IME 过渡。新的[插入动画监听器](https://developer.android.com/reference/android/view/WindowInsetsAnimation.Callback)允许人们创建“完美的帧过渡”，因为它通知应用程序每帧插入的变化。另一方面，新的[windowinsetanimationcontroller](https://developer.android.com/reference/android/view/WindowInsetsAnimationController)API 让应用程序控制 IME 和系统栏的转换。在右下角显示的例子中，应用程序使用 windowinsetanimationcontroller API 来控制过度滚动应用程序 UI 时的 IME 过渡。
*   **App 首选刷新率:**现在有几十款安卓设备都有高刷新率显示，比如 90Hz，120Hz，或者 144Hz。在 Android 11 中，应用程序和游戏现在可以为自己的窗口设置首选帧速率。运行应用程序时，系统将使用应用程序的首选帧速率来选择显示刷新率。
*   **重启恢复:**正如我们在之前强调的[，Android 11 改善了隔夜 OTA 更新的体验。重启后，应用程序可以访问凭证加密(CE)存储，而无需用户解锁设备。因此，当用户不在解锁手机时，应用程序可以在 OTA 后恢复正常功能。](https://www.xda-developers.com/resume-reboot-make-ota-updates-more-seamless-pixel-4/)
*   **Android 模拟器中的摄像头支持:**Android Studio 中的 Android 模拟器现在支持前后仿真摄像头。后置摄像头支持 Camera2 API 中的 [HW Level 3](https://source.android.com/devices/camera/versioning#camera_api2) ，而前置摄像头支持带有逻辑摄像头支持的完整级别。

## 开始

四月份将会有一个开发者预览版，随后是两个测试版。如果一切按计划进行，稳定的 Android 11 版本将于 2020 年第三季度发布。

要在 Pixel 设备上安装 Android 11 开发者预览版 2，您必须拥有 Pixel 2、Pixel 2 XL、Pixel 3、Pixel 3 XL、Pixel 3a、Pixel 3a XL、Pixel 4 或 Pixel 4 XL。你可以[手动刷新预览版本](https://developer.android.com/preview/download.html)或者你可以使用 [Android 刷新工具](https://source.android.com/setup/contribute/flash)来为你刷新。如果您没有 Pixel 设备，您可以通过 Project Treble 兼容设备上的[通用系统映像](https://developer.android.com/topic/generic-system-image/releases) (GSI)安装最新的开发者预览版，这包括使用 Android 9 Pie 或更高版本启动的设备。不过，您的里程可能会有所不同。最后，您可以在 Android Studio 的 Android 模拟器中启动最新版本。这些方法中的每一种都为您提供了一种在新环境中测试应用的方式。一定要彻底测试你的应用程序，因为谷歌最终会将 Android 11 作为你的应用程序纳入谷歌 Play 商店的一个要求。

试用最新版本，如果遇到任何问题，给谷歌[反馈](https://developer.android.com/preview/feedback)。

**[安卓 11 XDA 新闻](https://www.xda-developers.com/tag/android-11/)**