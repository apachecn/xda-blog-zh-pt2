# ARCore for All 为不受支持的设备带来了谷歌的新 AR 平台

> 原文：<https://www.xda-developers.com/arcore-for-all-google-augmented-reality/>

# ARCore for All 为不受支持的设备带来了谷歌的新增强现实平台

由于开发人员社区的一些工作，我们可以通过 ARCore for All 项目尝试谷歌的新增强现实平台。

谷歌最近[宣布了一个名为 ARCore](https://www.xda-developers.com/arcore-new-augmented-reality-google/) 的新平台，使没有特定摄像头和传感器的智能手机能够享受增强现实的乐趣。就像谷歌对其 Daydream 平台有硬件要求一样，他们的增强现实平台也有一些硬件要求。然而，一个社区开发者想出了一种方法，通过一个新的项目，他们称之为 ARCore for All，在不支持的设备上实现这一功能。

当谷歌推出 Daydream 时，我们看到了同样的工作，因为它需要一定水平的硬件来通过该公司的认证测试。同为 XDA 作家的亚当·康威甚至写了一份详细的逐步指南，告诉你如何自己做到这一点。问题是，谷歌设置这些限制是有原因的，这通常也是原始设备制造商限制他们设备的其他硬件功能的原因。即使像这样的工作和性能可以接受，也可能有其他原因限制了它(电池消耗、发热、特定的性能水平等)。).

不管原因是什么，我们中的一些人愿意失去一点点性能，或者比正常情况下消耗更多的电池寿命，只是为了让我们可以自己尝试新功能。这就是 ARCore for All 项目发挥作用的地方，因为它正是为 Android 社区爱好者做的。开发人员能够在他们的 G955F Galaxy S8+上使用这种方法，虽然它应该在其他人身上工作，但您的里程数可能会有所不同。

首先，你需要下载并[安装这里提供的 APK](https://drive.google.com/open?id=0B6YRx5-YRIlld2dlX1EtdDBLYlk)。因为这需要谷歌的 ARService 才能工作，你需要[从这里](https://github.com/google-ar/arcore-android-sdk/releases/download/sdk-preview/arcore-preview.apk)下载并安装它。然而，如果 ARService 应用程序没有正确安装或运行，那么你可以[获得这个修改版本](https://www.reddit.com/r/androiddev/comments/6x9q59/run_project_arcore_on_all_devices_currently/dmetmna)。我们在 OnePlus 5 上测试了这个修改后的 ARService 应用程序，它为我们工作。请记住，这只是 ARCore 程序的早期预览，在 Google 解决问题的过程中，可能会出现错误、崩溃或性能问题。

* * *

[**来源:GitHub**](https://github.com/tomthecarrot/arcore-for-all)