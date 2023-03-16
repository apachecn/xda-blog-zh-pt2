# Android Jetpack 凭借摄像头和生物识别技术向前推进

> 原文：<https://www.xda-developers.com/android-jetpack-camerax-biometrics/>

实际上，从第一天开始，开发的速度和简易性就已经成为 Android 平台的核心焦点。从一开始，谷歌就着手为如何在现有手机硬件上以最简单的方式支持最大数量的设备奠定基础。去年在 Google I/O 2018 上，谷歌用 Android Jetpack 为下一代 Android 支持库[奠定了基础。在 Google I/O 2019 上，Google 将他们的支持库提升到了一个新的水平，推出了一系列新版本，从更易于使用的 CameraX 相机库到将用户选择的生物识别身份验证与生物识别提示相集成的简单方法。](https://www.xda-developers.com/android-jetpack-components-kotlin-android-studio-3-2/)

## 科特林第一

Kotlin 编程语言自首次亮相以来就迅速流行起来。在宣布 Kotlin 将获得谷歌的一流支持后，谷歌现在宣布 Android 开发将越来越成为 Kotlin-first。许多新的 Jetpack 库将首先在 Kotlin 中提供。为了帮助开发者开始使用 Kotlin，谷歌鼓励开发者参加 [Kotlin/Everywhere](https://events.withgoogle.com/kotlin-everywhere/) 活动，并参加 [Udacity 课程](https://www.udacity.com/course/developing-android-apps-with-kotlin--ud9012)。

## 照相机

虽然 [Camera2](https://medium.com/google-developers/detecting-camera-features-with-camera2-61675bb7d1bf) 在功能、易用性和跨 Android 相机功能的标准化方面向前迈进了一大步，但它仍然非常复杂，不同设备上的[功能](https://www.xda-developers.com/android-pie-camera-hal3/)各不相同。这对于一个专业的相机应用程序开发者来说可能没什么问题(尽管甚至一些[十亿美元的公司](https://www.xda-developers.com/snapchat-executives-want-their-application-to-run-better-on-android/)都在为它而奋斗)，但它比一般应用程序想要包含的内容更有深度。大多数相机应用程序都可以瞄准一个标准化的 API，并允许设备完成繁重的工作，CameraX 使这成为可能。通过在任何 Camera2 设备上完全向后兼容，一直到 Android Lollipop，CameraX 为开发人员提供了一个更简单的库，并允许他们保持与支持 Camera2 的任何当前或未来设备或 CameraX 集成的任何未来继任者的向后和向前兼容性。这也不仅仅是基础功能。CameraX 充分利用了谷歌在 Camera2 和 CameraX 之间集成的任何功能，包括 HDR、人像模式、广角、单镜头多摄像头，甚至谷歌广受好评的夜间模式。

## 生物识别提示

生物识别提示消除了生物识别认证的复杂性，消除了与任何安全功能直接交互的需要。开发人员只需要调用 Biometrics Prompt，它就会将请求交给系统的默认生物认证系统，无论是指纹、虹膜、人脸还是其他任何东西。随着新的创新生物认证方法在手机中的实施，这个 Android Jetpack 库将变得越来越有用，从而更容易支持用户现在和未来选择的系统。

## 包含协同例程的 LiveData 和生命周期

Jetpack 的新生命周期和 LiveData KTX 将允许您使用具有生命周期意识的 Kotlin 协同程序，以便您可以支持常见的一次性异步操作。Jetpack 将通过“提供与生命周期相关的协程作用域、感知生命周期的协程调度程序，以及新的 LiveData builder 对简单异步链的支持”，以更简单的方式进一步处理并发性。

## 基准

Android Jetpack 旨在更容易地确保您的应用程序按照您希望的方式运行，现在它将为您提供必要的工具来使用 Benchmark 测试性能。这个库允许你在不离开 Android Studio 的情况下检查你的应用程序的延迟、数据库查询、视图膨胀和 RecyclerView 滚动。

## 安全性

安全性是一个即使是大型开发人员也很容易犯错误的领域，本库旨在减少这方面的麻烦。从管理硬件支持的密钥库到生成和验证密钥，安全库将焦点从样板文件移开，并允许您将它放在实际保护应用程序上。

## 企业

Android Jetpack Enterprise library 简化了与企业移动管理提供商的集成，允许应用程序发送键控应用程序状态，而不必担心跨版本匹配托管配置。

## 具有保存状态的视图模型

ViewModel 和 SavedInstanceState 使得在不丢失 UI 配置数据的情况下从崩溃中恢复变得更加容易，但是仍然需要大量的样板代码。通过将 SavedState 集成到 ViewModel 中，Google 去掉了样板文件，使两者的使用变得更加容易。

ViewPager 使得在 Android 应用中实现水平页面滚动变得更加容易。ViewPager2 是下一个发展，增加了对垂直滚动和 RTL 布局的支持。

## 汽车用安卓系统

Android for Cars 与谷歌目前推进的 Android Automotive OS 紧密相关。它可以让你创建一个汽车设计版本的应用程序，供你的用户在他们选择的 Android Auto head 单元(或手机)上使用。

## 工作管理器

后台任务可能难以正确实现。Workmanager 通过以一种与手边设备良好配合的方式为您处理后台调度，让您不再感到沮丧。

## 航行

不，不是物理导航。浏览您的应用程序！Android Jetpack Navigation 库提供了关于如何在你的应用程序中布局移动的指导，以避免崩溃、死胡同和不可预测的导航。

## 构成

把最好的留到最后，谷歌还宣布了 Android Jetpack Compose 的早期预览，这是一个非捆绑工具包。基于 Google 从 Flutter 学到的东西，Compose 旨在为 Kotlin UI 开发带来更具反应性和声明性的编程方法，其原则与让 Flutter 成为社区最爱的原则相同。构建 Compose 的核心原则如下:

*   包括 Kotlin 的优点——简洁且可与 Java 互操作。
*   完全声明性地定义 UI 组件。该框架在幕后处理 UI 优化和视图层次结构更新——您所要做的就是将您的 UI 描述为可组合的函数。
*   使用可重复使用的构建块构建自定义小部件。
*   使用现有视图。
*   支持开箱即用的材料设计。
*   支持实时预览和应用更改等工具。

谷歌不会发布 Compose 的测试版甚至是 alpha 版，但该公司将开放整个项目的源代码，这样开发者就可以在制作过程中检查它。如果你在早期测试中遇到任何 bug，你可以在这里提交 bug[。](https://issuetracker.google.com/issues/new?component=612128&template=1253476)