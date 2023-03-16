# Android 11 将引入“应用兼容性”开发者选项，以帮助测试平台变化

> 原文：<https://www.xda-developers.com/android-11-new-app-compatibility-developer-option-dev-test-new-platform-changes/>

每年在谷歌 I/O 大会上，谷歌都会强调下一版本 Android 的一些最激动人心的变化。虽然大多数用户通过影响他们体验的视觉变化来判断 Android 版本，但每个 Android 更新也带来了大量 API 和[平台行为](https://www.xda-developers.com/android-q-storage-access-framework-scoped-storage/)的[变化。这些变化对于应用程序开发人员来说非常重要，他们需要注意并准备好应用程序，因为它们可以从根本上改变最终用户使用应用程序的方式。随着下一个版本的 Android，Android 11，谷歌将通过开发者选项中新的“应用兼容性”设置，让开发者更容易测试和准备他们的应用程序，以适应即将到来的变化。](https://www.xda-developers.com/android-q-record-audio-monitor-device-temperature/)

每当谷歌发布一个新的 Android 版本时，那些有兴趣积极维护他们的应用程序的应用程序开发人员需要仔细阅读新的变化以及伴随这些变化而来的文档。然后，他们可以决定更新他们的应用程序，以添加这些新的 API 功能，如果他们想要或将现有 API 的使用迁移到新的 API，这是一个可选或不可选的途径。应用程序开发人员不必立即更新他们应用程序的目标 API，但他们最终必须这样做，以满足谷歌 Play 商店的[移动目标 API 要求。在此之后，开发人员还需要在新的 Android 版本上实际测试他们的应用程序，这可以在模拟设备、云托管设备或本地设备上完成。测试是开发例程的一部分，但是当涉及到重大变更时，测试变得更加重要。](https://www.xda-developers.com/all-apps-require-target-android-pie-play-store/)

此外，当谷歌想要引入重大的平台行为变化时，他们不会立即在新的 Android 版本发布中实现这一变化。这是为了保护用户避免他们的应用程序崩溃和失去功能，同时也给了开发者更多的时间来更新他们的应用程序。比如在 Android 7 牛轧糖中，谷歌为了节省电池寿命，决定[限制一些隐式广播](https://www.xda-developers.com/how-android-n-will-improve-battery-and-memory-management/)。有了 Android 8 Oreo，谷歌[完全限制应用程序注册隐式广播接收器](https://developer.android.com/guide/components/broadcast-exceptions)。但在 Android 8 Oreo 发布之前，谷歌希望开发者为他们的应用程序不再能够注册隐式广播接收器的情况做好准备。为此，开发者可以[在 Android 7 Nougat 中使用 ADB 命令来模拟隐式广播不可用的情况](https://developer.android.com/topic/performance/background-optimization#further-optimization):

```
 adb shell cmd appops set RUN_IN_BACKGROUND ignore 
```

像上面这样的 ADB 命令是一个例子，说明了 Google 如何允许应用程序开发人员测试他们的应用程序在 Android 平台行为变化下的行为。

另一个最近的例子是，在 Android Q Beta 2 中， [Google 要求开发人员通过运行 ADB 命令在他们的应用程序上测试作用域存储](https://android-developers.googleblog.com/2019/04/android-q-beta-2-update.html):

```
 adb shell cmd appops set your-package-name android:legacy_storage default && \ 
```

作为一名应用程序开发人员，可以假定您熟悉 ADB 命令，并且不反对使用它们来测试这些平台变化。但总有改进的空间，谷歌通过引入一个简单的用户界面来控制这些变化，使这个测试过程变得更容易。

有了新的 [PlatformCompat 项目](https://android-review.googlesource.com/q/platformcompat)，开发者不再需要为每个新的平台行为变化运行 ADB 命令。在 Android 11 中，Android 将在开发者选项中有一个新的子菜单，可以在每个应用程序的基础上快速切换新的平台行为变化，而无需发送任何 ADB shell 命令。每个目标 API 级别将有不同的部分，例如，API 级别> 29 将有其自己的一组可以切换的行为改变，而 API 级别> 30 将有其自己的一组改变。

在上面展示应用程序兼容性部分的截图中(来自运行在仿真器上的源代码构建的 AOSP)，“默认启用的更改”部分包括 Android 11 API 更改，这些更改将默认在所有应用程序上启用，而不管其目标 SDK。“针对 targetSDKversion > 29 启用”部分是 Android 11 API 更改，仅针对针对 Android 11/API 级别 30 的应用启用。

虽然这种特殊的变化不会直接让最终用户兴奋，但它确实让应用程序开发人员的工作变得更容易，这总是一件好事。

* * *

*感谢 XDA 知名开发商 [luca020400](https://forum.xda-developers.com/member.php?u=5778309) 提供的提示和随附的截图。*

关于 Android 11 的更多报道: