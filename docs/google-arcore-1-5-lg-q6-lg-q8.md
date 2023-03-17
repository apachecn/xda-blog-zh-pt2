# 谷歌 ARCore 1.5 宣布，LG Q6 和 LG Q8 现在支持

> 原文：<https://www.xda-developers.com/google-arcore-1-5-lg-q6-lg-q8/>

谷歌 ARCore 最近真的火了。增强现实平台已经得到了许多新设备的支持。不像它的前身 [Tango](https://www.xda-developers.com/project-tango-dead-google-arcore/) ，它不需要任何专用硬件来工作。一切都是在软件端完成的，这帮助 ARCore 找到了在各种设备上的受欢迎程度和兼容性。今天，我们有新的东西。谷歌决定不仅宣布新的设备支持，而且还宣布新版本的 ARCore。

我们都知道增强现实相机应用程序不太电池友好。谷歌很长时间以来一直致力于解决这个问题。我们之前已经发现了关于 ARCore 1.5 的线索，暗示了一加 6T、华为 Mate 20 等设备的兼容性。 [LG Q6](https://www.xda-developers.com/lg-q6-android-oreo-update-dtsx-3d-stereo/) 、 [LG Q8](https://www.xda-developers.com/lg-q8-6-2-inch-display-stylus/) 、华硕 ROG 手机和[三星 Galaxy Tab S3](https://www.xda-developers.com/samsung-galaxy-tab-s3-android-oreo-uk/) 现在都是官方支持的设备，但让我们谈谈新功能。

## 运行时加载 glTF

如果您曾经开发过基于 ARCore 的应用程序，那么您应该知道加载 glTF 模型在以前是不可能的。你必须把它们转换成 SFB 格式才能正确使用。从现在开始，您将能够使用 Sceneform 中的 API，该 API 将允许您从云中或本地存储中加载 glTF 模型。

## Sceneform 现在是开源的

Sceneform 帮助开发人员在应用程序中使用内置模型和元素，节省了大量时间。不幸的是，不可能按照我们的喜好改变或修改元素，所以 Sceneform 有时没有多大意义。从现在开始，Sceneform 是开源的，它存在于 GitHub 上。你可以随意修改任何你喜欢的元素，并在你的应用程序中使用它。

## 将点云 id 添加到 ARCore

显然，当涉及到点云时，一些开发人员已经要求能够将帧之间的点关联起来。这给了他们制造更坚固结构的能力。新点 id 是唯一的，当它们离开视图时就会丢失。

目前，这些设备正式支持 ARCore:

### 截至 2018 年 9 月 28 日 ARCore 支持的设备

您可以从下面的链接下载或更新 ARCore 应用程序。如果你使用一个新添加的设备或想更新到 1.5 版本的应用程序，你可能需要等待几天，因为更新还没有广泛提供。此外，确保下载一行代码来测试增强现实的能力。

* * *

[**来源:谷歌开发者博客**](https://developers.googleblog.com/2018/09/introducing-new-apis-to-improve.html)