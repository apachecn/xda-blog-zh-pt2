# 未来的 Android 版本可能会及时支持新 PlayStation 应用程序的 DualShock 4 动作控制

> 原文：<https://www.xda-developers.com/android-may-support-dualshock-4-motion-controls-new-playstation-apps/>

在过去几年中，面向游戏的智能手机变得非常流行。华硕将其 ROG(玩家国度)品牌带入智能手机行业，雷蛇收购了一家名为 Nextbit 的 OEM 厂商并发布了雷蛇手机，努比亚发布了 Red Magic，小米发布了黑鲨，等等。即使一些手机的名称中不包含“游戏”品牌，但由于不断进步的片上系统和图形处理单元，所有最近的旗舰产品都完全能够玩图形密集型游戏。默认情况下，Android 并没有包括很多游戏优化功能来为用户提供更好的游戏体验。但是，这种情况已经改变了一段时间。

去年，Android Pie 为索尼 PlayStation 4 的 DualShock 4 带来了[原生键映射支持](https://www.xda-developers.com/android-pie-support-playstation-4-dualshock-4/)。以前，DualShock 控制器的默认按键映射只存在于索尼 Xperia 设备和其他设备中，这些设备的原始设备制造商懒得包括它们。该功能多年来被大量请求，因此谷歌和索尼的工程师最终在 Android Pie 中实现了我们的愿望。Android 开源项目中的一项新的[承诺](https://android-review.googlesource.com/c/platform/hardware/libhardware/+/571762/)(通过*9 to 5 谷歌的 [Stephen Hall](https://twitter.com/hallstephenj/status/1096168135785410560)* [)](https://twitter.com/hallstephenj/status/1096168135785410560) 表明原生 DualShock 4 控制器支持可能会变得更好。该承诺旨在让 Android 与 DualShock 4 的运动控制一起工作。

如果你还不知道，所有 DualShock 4 控制器都内置了陀螺仪和加速度计，它们足够敏感，可以检测控制器的倾斜、旋转和其他移动。我可以看到它在赛车游戏中有多有用，在游戏中，人们的自然反应是在转弯时倾斜身体。鉴于这个补丁是在 2017 年 12 月首次提交的，我们不想猜测它是否或何时会进入 Android。然而，该提交在过去一年中已更新了多次，最近一次评论是在 2019 年 2 月 8 日发表的。

最初，我们认为 Android Q 将支持 DualShock 4 的运动控制，但谷歌[的一名工程师表示](https://android-review.googlesource.com/c/platform/hardware/libhardware/+/571762/11#message-8925f9aa59300c689f08d3cf1b5584cab4118e73)关于实现这一功能还有待讨论。因此，提交不会被合并，因为 Android Q 没有批准该功能。

关于 Android Q，显然，索尼添加了一堆 DualShock 4 相关代码，包括“蓝牙修复、内核驱动、输入按钮/操纵杆映射。”还有关于控制器内部传感器性质的评论。PlayStation 硬件和系统工程总监 roderick Colenbrander[解释说](https://android-review.googlesource.com/c/platform/hardware/libhardware/+/571762/11#message-b72e3cefecab043a6ac6d01013c236d7f847d882)因为这些传感器是动态的，系统不应该提供它们的默认参数。相反，应用程序可以通过“getName()”和“getVendor()”函数检索所需的信息。

Colenbrander 先生还讨论了将输入传递到设备的可能方法。有两种可能的解决方案。第一个是官方的、原生支持的传感器框架，它已经内置在 Android 中。它帮助开发人员通过诸如“SensorEvent”、“SensorManager”等类和接口获取原始传感器数据。这些 API 允许开发人员访问传感器、监听器、方向信息、事件时间戳等列表。第二种方法是使用 evdev (event device)，这是 Linux 内核中的一个接口，其目的与读取和写入输入事件几乎相同。工程师说，在山景城的一次会议后，团队决定采用传感器框架，原因很明显，比如第一方的支持。他的评论还提到了索尼显然打算在今年推出的 PlayStation 应用程序，目前我们没有这方面的信息。

这就是我们能告诉你的关于索尼和谷歌正在研究的所有东西。DualShock 4 控制器对动作控制的支持很好，但我更感兴趣的是新 PlayStation 应用程序的可能性。考虑到工程师在索尼内部的职位(云游戏服务器和云基础设施的软硬件技术开发)，我们希望他们将这些平台用于 Android 上的 PlayStation 游戏流媒体。这只是猜测，因为没有关于 Android 上新的 PlayStation 应用程序的官方信息。如果有新消息，我们会及时通知你。