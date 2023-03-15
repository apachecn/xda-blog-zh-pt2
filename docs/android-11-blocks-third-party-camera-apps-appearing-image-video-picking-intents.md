# [更新:更多细节] Android 11 阻止第三方相机应用出现在图像/视频拍摄意图中

> 原文：<https://www.xda-developers.com/android-11-blocks-third-party-camera-apps-appearing-image-video-picking-intents/>

**更新 1 (08/20/2020 @ 06:15 PM ET):** 谷歌已经更新了其开发者文档，以解释为什么 Android 11 上的第三方相机应用无法响应隐式图像/视频意图动作。滚动到底部了解更多信息。下面保留了 2020 年 8 月 19 日发表的文章。

Android 11 正在改变应用程序与设备上第三方相机应用程序的交互方式，这将阻止它们出现在图像/视频拍摄意图中。在旧版本的 Android 中，如果一个应用程序希望让用户捕捉图像，它可以在应用程序内实现拍照(使用 Android 的各种相机 API)，或者它可以发送一个可以由专用相机应用程序处理的意图来捕捉图像。如果一个应用程序决定选择后一个选项，旧版本 Android 上的用户会看到一个消除歧义的对话框，让他们选择相机应用程序来捕捉图像。该对话框通常会显示用户设备上安装的所有相机应用程序，包括第三方相机应用程序，只要它们是为响应某些意图而编写的。然而，在 Android 11 中，该对话框将只包括预装的股票相机应用程序，除非开发者专门针对某些第三方相机应用程序。

这一变化实际上意味着，在大多数情况下，当用户想要拍照时，他们必须手动启动第三方相机应用程序，这使得第三方相机应用程序不太方便使用。当用户发现自己喜欢的相机应用程序无法从其他应用程序中启动时，也会让用户责怪第三方相机应用程序的开发者。谷歌正在 Android 11 中通过阻止第三方相机应用响应以下意图动作来实现这一变化:

*   `android.media.action.VIDEO_CAPTURE`
*   `android.media.action.IMAGE_CAPTURE`
*   `android.media.action.IMAGE_CAPTURE_SECURE`

谷歌表示，这一变化已经在 Android 11 中实施，以保护用户的隐私和安全。该公司没有详细说明如何实现，但很可能一些恶意应用程序伪装成相机应用程序，以获取用户的照片。然而，该公司确实提到了一个针对开发者的解决方案，允许应用程序仍然可以启动第三方相机应用程序。该变通办法实际上要求开发人员在发送意向时以他们选择的特定第三方应用为目标。例如，文档扫描仪应用程序的开发者可以发送一个显式的意图来启动 [Adobe Photoshop Camera](https://www.xda-developers.com/adobe-photoshop-camera-ai-powered-camera-app-android-os/) ，而不是发送一个隐式的意图来打开相机拾取器。Android 11 使得开发者甚至无法查询能够响应上述 3 个意图动作的应用列表，这意味着开发者必须提前知道他们想要支持哪些第三方相机应用。

**来源: [CommonsWare](https://commonsware.com/blog/2020/08/16/action-image-capture-android-r.html) ，[安卓开发者](https://developer.android.com/preview/behavior-changes-11#media-capture)，**

**Via:[Reddit](https://www.reddit.com/r/android_devs/comments/iba7p7/action_image_capture_and_android_r/)**

*感谢 XDA 资深会员 [AndroidDeveloperLB](https://forum.xda-developers.com/member.php?u=5798043) 的提示！*

## 更新 1:谷歌称这一变化是为了维护隐私

谷歌已经更新了其 Android 11 行为改变页面，增加了“[媒体意图动作需要系统默认摄像头](https://developer.android.com/preview/behavior-changes-11#media-capture)”部分的新信息(通过 [*The Verge* )。谷歌解释说，这一变化“旨在确保 EXIF 位置元数据根据发送意图的应用程序中定义的位置权限得到正确处理。”基本上，谷歌担心尚未获得明确位置访问权限的应用程序会让用户打开*已获得*位置访问权限的相机应用程序，由于传递给应用程序的结果照片可能包含 EXIF 位置元数据，因此调用应用程序可以通过从照片中读取位置数据来绕过位置访问请求。如果一个应用程序试图在 Android 11 中这样做，它将需要声明`ACCESS_MEDIA_LOCATION`以及`ACCESS_COARSE_LOCATION`或`ACCESS_FINE_LOCATION`权限，以便读取 EXIF 位置元数据。(值得注意的是，](https://www.theverge.com/2020/8/20/21376391/google-android-11-third-party-camera-picker-intents)[谷歌关闭了 Android 10 中的另一个位置访问漏洞](https://developer.android.com/training/data-storage/shared/media#media-location-permission)，如果一个应用程序试图从照片中检索未经编辑的 EXIF 元数据，它要求应用程序请求`ACCESS_MEDIA_LOCATION`许可。)

虽然这种行为变化将影响应用程序启动用户定义的默认相机应用程序的能力，因为前面提到的 3 个意图动作是如此古老和频繁使用，但谷歌指出，这种变化并不影响所有可以启动用户定义的默认相机应用程序的意图动作，例如:`android.provider.MediaStore.INTENT_ACTION_STILL_IMAGE_CAMERA`、`android.provider.MediaStore.INTENT_ACTION_STILL_IMAGE_CAMERA_SECURE`或`android.provider.MediaStore.INTENT_ACTION_VIDEO_CAMERA`。然而，这些目的并不相同，因为它们只启动默认的相机应用程序，而不允许将图像发送回调用应用程序。