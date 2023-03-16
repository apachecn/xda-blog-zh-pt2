# Unity 19.1 带来了移动自适应性能，以提高三星 Galaxy S10 的游戏性能

> 原文：<https://www.xda-developers.com/unity-20191-mobile-adaptive-performance-samsung-galaxy-s10-fold/>

Unity 是游戏开发者用来为 Android 和其他平台创建游戏的最流行的 IDE 和游戏引擎之一。虽然游戏开发本身实际上是一门艺术，但 Unity 提供了工具和功能来构建 2D 和 3D 环境以及跨多个平台的复杂机制，从而使过程更加简单。Unity 2019.1(简称 19.1)现已面向游戏开发者推出，以稳定的形式为游戏开发者带来了几个“预览”功能，以便在他们的游戏中实现这些功能，以及自己的新预览功能。

## 适应性性能

此次 Android 版本的亮点之一是为三星 Galaxy 旗舰产品提供了一个预览版的自适应性能。与 PC 和游戏机不同，移动设备上的游戏有热量管理和功耗的固有限制。外观精美、运行流畅的游戏具有密集的处理需求，会使您的设备快速升温。PC 和控制台通过它们的主动冷却系统来解决这个问题，但由于手机没有主动冷却硬件(还没有)，手机最终会调节性能以保持温度在可控范围内。考虑到可用硬件的广泛范围，以及不同的性能和节流情况，这个问题变得更加棘手。

游戏开发者通过两种主要方法来解决这个问题:通过牺牲图形保真度和帧速率来确保最大的兼容性，或者通过预测硬件行为，这很难执行。

Unity 和三星合作开发了一项名为“ [Adaptive Performance](https://blogs.unity3d.com/2019/04/01/higher-fidelity-and-smoother-frame-rates-with-adaptive-performance/) ”的功能，该功能提供了一种更好的方法来实时管理游戏的热量和性能。通过 Unity Package Manager 安装 Adaptive Performance 后，Unity 会自动将 Samsung GameSDK 子系统添加到您的项目中。在运行期间和受支持的设备上，Unity 将创建并启动自适应性能管理器，该管理器将提供关于设备热状态的反馈。然后，开发人员可以选择订阅事件或在运行时从 Adaptive Performance Manager 中查询信息，以创建有关热量趋势的实时反应。例如，当设备在早期阶段开始节流时，游戏可以调整质量设置、目标帧速率和其他参数，以确保游戏能够保持更持续的性能。一旦温度再次开始下降，参数可以再次调整，以提供更好的游戏性能。通过密切关注热性能，人们可以通过基于实时反馈调整性能来避免一起节流。这将导致更可预测的帧速率和游戏体验以及更低的热量累积。

自适应性能的预览版可用于 Unity 2019.1，支持 [Galaxy S10](https://www.xda-developers.com/samsung-galaxy-s10-s10-and-s10e-launch-with-the-snapdragon-855-ultrasonic-in-display-fingerprint-scanners-reverse-wireless-charging-and-a-whole-lot-more/) 和 [Galaxy Fold](https://www.xda-developers.com/samsung-galaxy-fold-specifications-pricing-availability/) 。对更多 Galaxy 设备的支持将在今年晚些时候推出，一名代表[向 *Android 权威*](https://www.androidauthority.com/unity-19-1-update-979501/) 提到，Unity 也在与其他制造商进行谈判。

## 移动通知

[移动通知预览包](https://docs.unity3d.com/Packages/com.unity.mobile.notifications@1.0/manual/index.html)将通过在 Android 4.1 及更高版本上添加对调度本地可重复或一次性通知的支持，帮助开发人员实现保留机制和基于计时器的游戏。

## 通过 Unity Hub 安装 Android SDK 和 NDK

Unity Hub 现在允许开发人员安装 Android 所需的所有组件，作为 Android 构建支持选项的一部分，确保他们获得正确的依赖关系。您也可以选择手动安装和配置组件，并使用 Android Studio。

## Android Logcat 集成

Unity 2019.1 现在集成了 logcat 功能，通过控制和过滤来自 Unity 内部的消息，使调试更容易。

## 更快的脚本迭代仅在 Android 上构建补丁

现在，您可以使用仅脚本构建选项跳过构建过程中的几个步骤，因为它仅重新编译脚本并修补设备上已存在的应用程序包。当您选择“生成并运行”时，最终的包将被生成并部署。

## 更多独立于平台的特性

上面列出的特性是针对 Android 上的游戏开发的。Unity 2019.1 还打包了更多适用于整个游戏引擎的更改，将好处扩展到 Android 和其他平台。Unity 发布了一个广泛的更改列表，重点是突发编译器、轻量级渲染管道、着色器图形等更多功能。

如果你在游戏中使用 Unity 或者有兴趣了解引擎的进一步变化，我们建议[阅读完整的变化列表](https://blogs.unity3d.com/2019/04/16/introducing-unity-2019-1/#mobile)。

[**下载 Unity 2019.1**](https://unity3d.com/get-unity/update)

* * *

[**来源:团结博客**](https://blogs.unity3d.com/2019/04/16/introducing-unity-2019-1/) [**故事 Via:安卓权威**](https://www.androidauthority.com/unity-19-1-update-979501/)