# Android 13 在 Camera2 API 中增加了 HDR 视频和“流用例”支持

> 原文：<https://www.xda-developers.com/android-13-hdr-vide-stream-use-case-camera2-api/>

在 Android 5.0 中引入了 [Camera2 API](https://www.xda-developers.com/camera2-api/#whatiscamera2api) ，作为原始相机 API 的继承者。该 API 允许开发人员检查设备上有哪些相机功能，并向应用程序展示粒度相机功能，包括曝光和白平衡增益的每帧控制、锐化、去噪等。这也是安装[谷歌摄像头端口](https://www.xda-developers.com/google-camera-port-hub/)的先决条件。随着 [Android 13](https://www.xda-developers.com/tag/android13/) ，谷歌给 Camera2 API 增加了一些新功能。

正如斯珀发现的那样，Android 13 的 HAL 允许智能手机制造商向 Camera2 API 展示 10 位视频输出。如果 OEM 选择公开 10 位相机输出，它必须至少支持 HLG10 配置文件。如果设备支持其他 HDR 格式，如 HDR10+和 Dolby Vision，设备制造商可以使用[camera characteristics # REQUEST _ RECOMMENDED _ TEN _ BIT _ DYNAMIC _ RANGE _ PROFILE](https://developer.android.com/reference/android/hardware/camera2/CameraCharacteristics#REQUEST_RECOMMENDED_TEN_BIT_DYNAMIC_RANGE_PROFILE)常量向应用程序发布推荐的配置文件。同时，支持 Camera2 API 的应用程序可以使用 output configuration . setdynamicrangeprofile API 设置特定设备支持的动态范围配置文件。

除了 HDR 视频支持，Camera2 API 还增加了对“流用例”的支持，允许 OEM 在不同的流场景中优化相机性能。

> 流用例从最终用户的角度说明了特定摄像机流的目的。相机使用案例的一些示例包括:向用户显示的实时取景器的预览流、用于生成高质量照片捕捉的静态捕捉、用于对相机输出进行编码以便将来回放的视频记录，以及用于实时视频会议的视频通话。

如果设备制造商选择实现这一功能，则需要实现以下流用例:

*   实时取景器预览和应用内图像分析
*   静态照片捕捉的静态 _ 捕捉
*   VIDEO_RECORD 用于录制视频片段
*   PREVIEW_VIDEO_STILL 用于取景器、视频录制和静态图像捕捉的单个视频流。
*   用于长时间视频通话的 VIDEO_CALL

当流用例支持可用时，相机设备可以使用 Camera2 API 执行诸如选择最佳相机传感器模式、选择调谐参数和构建图像处理流水线之类的配置。应用程序可以使用[camera characteristics # SCALER _ AVAILABLE _ STREAM _ USE _ CASES](https://developer.android.com/reference/android/hardware/camera2/CameraCharacteristics#SCALER_AVAILABLE_STREAM_USE_CASES)字段来查询设备上支持的 steam 用例列表。

* * *

**来源** : [斯珀](https://blog.esper.io/android-13-deep-dive/#camera2_hdr_video)