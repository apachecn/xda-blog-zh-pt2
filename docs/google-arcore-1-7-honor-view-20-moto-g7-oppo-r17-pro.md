# 谷歌 ARCore 1.7 现在支持 Honor View 20、Moto G7 等

> 原文：<https://www.xda-developers.com/google-arcore-1-7-honor-view-20-moto-g7-oppo-r17-pro/>

谷歌的增强现实软件开发工具包 ARCore 正在对 1.7 版进行重大更新。在一篇博客文章中，谷歌表示，1.7 版专注于“创造性元素”，比如增强现实自拍，在 Sceneform AR 应用程序中设置角色动画，集成 ARCore Elements，以及添加共享摄像头访问。此外，受支持设备的官方列表已经扩大，包括了诸如 Honor View 20、Moto G7 系列、OPPO R17 Pro 等设备以及更多设备。

## ARCore 1.7 概述

### 增强人脸 API

新的[增强人脸 API](https://developers.google.com/ar/develop/java/augmented-faces/) 允许开发者用 3D 效果覆盖用户的脸。例如，谷歌表示，开发人员可以创建动画面具、眼镜、虚拟帽子等效果，或者进行皮肤修饰。它使用前置摄像头创建一个 468 点的 3D 网格，提供坐标和特定区域的锚点。开发人员可以使用 Unity 或 Sceneform 开始使用增强的 Faces API。

### 场景格式中的动画

在 Sceneform 中创建的对象现在可以添加动画，比如跳舞、跳跃或旋转。

### ARCore 元素集成

ARCore SDK for Unity 集成了 ARCore Elements，这些通用 AR UI 组件旨在简化您的工作流程。平面寻找和对象操纵分别简化了检测表面和使用手势操纵虚拟对象的过程，是谷歌在博客中强调的两个 AR UI 组件。

### 共享摄像机访问

由于 SDK 中的共享相机访问，用户在 AR 模式中的切换将变得更加无缝。这项功能让用户暂停 AR 体验，跳到相机上拍照(理想情况下，是你的应用程序中的某个东西)，然后优雅地返回 AR 体验。

### ARCore SDK for Android 1.7.0 变更日志

#### **新的 API 和功能**

*   新增`Camera.getTrackingFailureReason()` (Java)和`ArCamera_getTrackingFailureReason()` (NDK)方法，当跟踪状态为`PAUSED`时返回 AR 跟踪失败的原因。
*   新的`Frame.transformCoordinates2d(…)` (Java)和`ArFrame_transformCoordinates2d(…)` (NDK)方法，将 2D 坐标列表从一个 2D 坐标系转换到另一个 2D 坐标系。
*   新的会话构造函数`Session(Context, Set<Session.Feature>)` (Java)和`ArSession_createWithFeatures()` (NDK)启用了新的功能，从:
*   **前置摄像头&增强人脸**
    *   应用程序现在可以通过在创建会话时请求`FRONT_CAMERA`功能来启用前置(自拍)摄像头的增强面部。
    *   新方法`CameraConfig.getFacingDirection()` (Java)和`ArCameraConfig_getFacingDirection()` (NDK)让应用程序检查它是否正在使用前置摄像头。
    *   **注意:**使用前置摄像头时，运动跟踪、所有类型的锚点、增强图像和平面检测都不可用。
    *   新方法`Config.setAugmentedFaceMode(…)`让一个应用程序能够增强人脸。
    *   新的 Trackable `AugmentedFace`类，用于检测人脸、确定区域姿态和生成 3D 人脸网格。
    *   `AugmentedFace` (Java)类和一组`ArAugmentedFace_*` (NDK)方法提供 getters 来请求 3D 人脸网格的中心姿态、区域姿态、顶点、法线和三角形索引。
*   **共享摄像头访问**(仅限 Java)
    *   应用程序现在可以通过在创建会话时请求`SHARED_CAMERA`功能来与 ARCore 共享相机控制。该功能主要用于在仅相机(非 AR)和 ARCore 模式之间快速切换。
    *   演示如何与 ARCore 共享摄像机访问的新`shared_camera_java`示例。
    *   新的`SharedCamera`类使应用程序能够与 ARCore 共享 Camera2 API 访问。
        *   **注意:** `Frame.getImageMetadata()`使用共享相机会话时抛出`IllegalStateException`。相反，使用`SharedCamera.setCaptureCallback(…)`直接订阅相机回调，并使用`Frame.getAndroidCameraTimestamp()`将帧与元数据相关联。
    *   新方法`Session.getSharedCamera()`获取会话的共享相机对象。
    *   新方法`Frame.getAndroidCameraTimestamp()`返回图像的 Android 相机时间戳。
*   其他仅针对 Java 的更改:
    *   新方法`Session.close()`允许明确释放 ARCore 会话持有的资源，以实现更好的资源控制。
    *   `PointCloud`现在实现了`Closeable`，允许它与 Java try-with-resources 和 Kotlin `use`块一起使用。

#### **折旧**

*   `Frame.transformDisplayUvCoords` (Java)和`ArFrame_transformDisplayUvCoords` (NDK)现已弃用。请用`frame.transformCoordinates2d(Coordinates2d.VIEW_NORMALIZED, …, Coordinates2d.TEXTURE_NORMALIZED, …)` (Java)和`ArFrame_transformCoordinates2d(…, AR_COORDINATES_2D_VIEW_NORMALIZED, …, AR_COORDINATES_2D_TEXTURE_NORMALIZED, …)` (NDK)代替。

#### **Bug 修复**

*   第 630 期:
    *   **Java:** `Session.createAnchor()`和`Trackable.createAnchor()`现在会正确的在适当的时候抛出`SessionPausedException`和`NotTrackingException`而不是`FatalException`。
    *   **C:** `ArSession_acquireNewAnchor()`和`ArTrackable_acquireNewAnchor()`现在会在适当的时候正确返回`AR_ERROR_SESSION_PAUSED`和`AR_ERROR_NOT_TRACKING`而不是`AR_ERROR_FATAL`。

## 支持 ARCore 的新设备

自从我们[上次](https://www.xda-developers.com/oneplus-6t-xiaomi-mi-mix-3-google-arcore/) [在谷歌的增强现实平台上带来](https://www.xda-developers.com/google-arcore-1-6-lighting-huawei-p20-lite/)你的新闻以来，这里是被添加到谷歌支持的设备列表中的设备。

*   荣誉观 20
*   华为 Nova 4
*   华为 Y9 2019
*   摩托罗拉摩托 G7
*   摩托罗拉 G7 Plus
*   摩托罗拉摩托 G7 动力
*   摩托罗拉摩托 G7 Play
*   OPPO R17 Pro
*   Vivo NEX 双显版

[**荣誉观 20 论坛**](https://forum.xda-developers.com/honor-view-20) [**华为 Nova 4 论坛**](https://forum.xda-developers.com/nova-4) [**Moto G7 论坛**](https://forum.xda-developers.com/moto-g7) [**Moto G7 玩论坛**](https://forum.xda-developers.com/g7-play) [**Moto G7 Plus 论坛**](https://forum.xda-developers.com/g7-plus) [**Moto G7 力量论坛**](https://forum.xda-developers.com/g7-power)

[Honor View 20](https://www.xda-developers.com/honor-view20-india-launch/) 、[华为 Y9 2019](https://www.xda-developers.com/huawei-y9-2019-india-launch-specifications-pricing/) 、 [Moto G7 Power](https://www.xda-developers.com/motorola-moto-g7-play-power-plus-launch/) 、 [OPPO R17 Pro](https://www.xda-developers.com/oppo-r17-r17-pro-india/) 都于近日在印上市。华为 Nova 4[和 Vivo NEX 双屏版](https://www.xda-developers.com/huawei-nova-4-48mp-rear-camera-display-hole/)尚未在中国以外推出。

如果你设法在支持的设备上下载谷歌 ARCore 1.7，请查看谷歌 Play 商店上提供的一些增强现实体验。我在下面链接了一个简单的应用程序，我想用它来验证 ARCore 是否有效。

* * *

[**来源 1:谷歌开发者博客**](https://developers.googleblog.com/2019/02/new-ui-tools-and-richer-creative-canvas.html?m=1) [**来源 2:谷歌 ARCore GitHub 发布页面**](https://github.com/google-ar/arcore-android-sdk/releases/tag/v1.7.0) [**来源 3:谷歌 ARCore 支持的设备**](https://developers.google.com/ar/discover/supported-devices)