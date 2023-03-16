# 华为 P30 Pro 或 Honor View 20 的夜视功能有助于在黑暗中看清东西

> 原文：<https://www.xda-developers.com/huawei-p30-pro-honor-view-20-night-vision/>

# 借助华为 P30 Pro 或 Honor View 20，夜视功能让您在黑暗中也能看清东西

一款名为 Night Vision 的新应用程序使用华为 P30 Pro 和 Honor View 20 上的后置 TOF 摄像头，让你在黑暗中也能看清东西。

当飞行时间传感器[被添加到智能手机的后部](https://www.xda-developers.com/honor-view20-tof-sensor-magic-ar/)时，我以为它们只是为了纯粹的噱头功能。当 Honor 在 Honor View 20 上展示一些游戏和相机模式时，我仍然不相信后置 TOF 传感器会有用。当然，有了后置 TOF 传感器，你可以获得人的 3D 深度图，并使用它们来控制游戏，但这对我来说似乎不够酷，我认为每部手机都需要这个传感器，至少直到我在华为 P30 Pro 上尝试了夜视。

**[荣誉观 20 论坛](https://forum.xda-developers.com/honor-view-20) || [华为 P30 Pro 论坛](https://forum.xda-developers.com/huawei-p30-pro)**

下面嵌入的是我在我的华为 P30 Pro 上录制的视频。我正在使用开发人员 lubo vonáSEK 开发的两个应用程序。第一个应用程序叫做夜视/ ToF 浏览器。这个应用程序可以让你以一种夜视的方式看到你周围的一切。这使用激光投影仪和相机来创建具有深度数据的虚拟 3D 模型，并将其渲染为夜视。虽然听起来可能很复杂，但它确实工作得很好，尽管我被限制在 280x180 的低分辨率。这是免费的尝试和发挥左右。

下一个应用程序是来自同一开发者的 3D 重建应用程序的演示版本。该应用程序允许您使用 Honor/Huawei 手机背面的 TOF 摄像头来创建您房间的 3D 网格，在现实世界中与 3D 立方体进行交互，将现实生活中的物体视为《我的世界》积木，或将每个 3D 平面视为紫色墙壁。实际上，您可以将 3D 网格保存为. obj 文件供以后使用。幸运的是，这款应用是免费的。如果你是一名开发者，想要在自己的应用中实现，开发者以 100 美元的价格出售 [Unity 资产。](https://assetstore.unity.com/packages/tools/integration/3d-reconstruction-for-arcore-android-only-136919)

这些是飞行时间传感器真正能力的几个例子。可悲的是，这个应用程序只能在装有传感器的华为和 Honor 手机上运行；我在 [5G 三星 Galaxy S10](https://forum.xda-developers.com/galaxy-s10-5g) 上测试了一下，没有效果。希望在未来，其他旗舰将 TOF 传感器链接到 Camera2 API。一旦原始设备制造商开始这样做，并包括 TOF 传感器，那么 TOF 传感器的真正魔力就可以向所有想要它的人开放。

**注意:华为/Honor 已经停止为其设备提供官方 bootloader 解锁代码。因此，他们设备的引导加载程序无法解锁，这意味着用户无法 root 或安装自定义 rom。**