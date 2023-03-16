# 部分重新映射像素 4 的无根运动感应手势

> 原文：<https://www.xda-developers.com/google-pixel-4-motion-sense-partially-remap-gestures-without-root/>

谷歌 Pixel 4 和 Pixel 4 XL T1 是谷歌的最新旗舰产品，具有一些有价值的升级和一些尖端技术，如 T2 Soli T3。Soli 是一种基于雷达的手势识别技术，通过位于设备顶部挡板的传感器对 Pixel 4 起作用。Soli 可以感知设备周围的运动，谷歌利用这一点实现了运动感知功能，允许用户通过在像素上挥手来控制音乐、静音提醒或查看手机。如果你想做更多的事情，[你需要 root](https://www.xda-developers.com/remap-pixel-4-motion-sense-gestures/) ，这不是我们推荐给每个用户的。然而，你仍然可以在没有 root 的情况下重新映射 Pixel 4 的运动感应手势，尽管是以一种有限的方式，遵循下面提到的任何一种方法。

## 方法 1:按钮映射器

由 XDA 知名开发商[开发的](https://forum.xda-developers.com/member.php?u=4684315)按钮映射器[flar 2](https://forum.xda-developers.com/pixel-4-xl/themes/app-button-mapper-remap-motion-sense-t3999591)通过其最新的 v1.40 更新在新的 Pixel 4 和 Pixel 4 XL 上引入了对运动感应的支持。这个应用程序过滤 logcat，以检测何时发生了运动感应事件，然后允许您为这些事件设置操作。虽然你可以向任何方向滑动来执行这个动作，但开发者指出向左或向右滑动的成功率最高。请注意，您需要在系统设置中启用动作感应，并且还必须启用“伸手检查手机”选项。您还需要进行一次[ADB 设置](https://forum.xda-developers.com/showpost.php?p=80870069&postcount=15)，以允许应用程序读取 logcat 输出。此外，请记住，您需要该应用程序的高级版本来重新映射手势。

**[按钮映射器- XDA 讨论线程](https://forum.xda-developers.com/pixel-4-xl/themes/app-button-mapper-remap-motion-sense-t3999591)**

通过按钮映射器的运动感将在屏幕关闭、锁屏和主屏幕上工作；传感器在其他应用程序中不活跃。

* * *

## 方法 2: Tasker

另一种方法当然涉及到 [Tasker](https://www.xda-developers.com/tag/tasker/) 。虽然 Tasker 也是一个付费应用程序，但很可能你已经购买了它，或者因为它无与伦比的多功能性而可以进一步使用它。

要使用 Tasker 重新映射没有 root 的手势，需要最新版本的 Tasker[。然后，按顺序执行以下步骤:](https://www.xda-developers.com/tasker-update-logcat-detection-automation/)

1.  在 Tasker 中，创建一个新的配置文件并选择事件上下文。
2.  选择“Logcat Entry”作为事件。
3.  在“组件”字段中，输入不带引号的“ *Oslo/FlickGestureSensor* ，以重新映射向右/向左/向上/向下的笔势。
4.  然后在“Filter”字段中，输入“*南*”、“*北*”、“*东*”或“*西*”，不加引号，具体看你要监听的手势方向。不过，请注意，准确性是最好的两个侧滑。
5.  最后，设置您希望进行的重映射操作，您就可以开始了。

* * *

使用这两种非根方法来重新映射运动感觉会有一些限制。如果你想要运动感应手势的真实和完整的重新映射功能，使你能够采取任何你想要的行动，最好的方法是给你的手机安装 [OsloBridger Magisk 模块](https://www.xda-developers.com/remap-pixel-4-motion-sense-gestures/)。