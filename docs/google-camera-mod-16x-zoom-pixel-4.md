# 谷歌相机模式支持谷歌像素 4 的 16 倍变焦

> 原文：<https://www.xda-developers.com/google-camera-mod-16x-zoom-pixel-4/>

Pixel 4 是谷歌第一款拥有多个后置摄像头的智能手机。与许多其他竞争对手的旗舰智能手机不同，Pixel 4 在背面提供了超宽和长焦摄像头，只有一个辅助长焦摄像头。值得称赞的是，Pixel 4 使用长焦相机的效果非常好。它不仅能够实现更好的人像模式拍摄和大约 2 倍的变焦，而且由于谷歌的 Super Res Zoom 算法，用户可以在质量损失最小的情况下拍摄高达 8 倍的变焦照片。谷歌很可能将谷歌相机应用程序限制为 8 倍变焦，因为再放大会降低拍摄质量，但这并不意味着再放大会产生无用的照片。相反，可以在 Pixel 4 上拍摄 16 倍变焦的照片，在我的快速实践中，这似乎还可以。

XDA 资深成员 [cstark27](https://forum.xda-developers.com/member.php?u=2712580) ，因修改谷歌相机应用程序以[在旧 Pixel 智能手机](https://www.xda-developers.com/google-camera-7-2-astrophotography-super-res-zoom-pixels/)上启用新功能而闻名，他发现了一种方法，不仅可以增加应用程序的最大变焦，还可以在更高的变焦水平上使用长焦相机。在 Pixel 4(和其他 Pixel 智能手机)上安装这个具有更高最大缩放限制的修改后的应用程序不需要 root，因为软件包名称不同于原始的谷歌相机应用程序。然而，如果你想在这个修改后的应用程序中以高于 8 倍的变焦水平使用 Pixel 4 的长焦相机，[你必须启动你的设备](https://www.xda-developers.com/google-pixel-4-root-magisk/)。

*左图:修改后的 app 中的设置页面。所有自定义设置都可以在“像素模块设置”中找到右边:“像素模式设置”页面，你可以设置最大缩放级别和其他设置。*

为了在更高的变焦水平下启用长焦相机，您必须刷新 cstark27 提供的 Magisk 模块，或者输入以下 shell 命令:

```
 adb shell su -c "setprop persist.camera.maxzoom 51" 
```

如果您还没有授予 shell 的 root 访问权限，那么在出现提示时授予它访问权限。输入这个命令后，强制关闭“Camera PX”(修改后的谷歌相机应用)或者重启你的 Pixel 4。该属性控制长焦相机在 Google Camera 应用程序中使用的最大缩放级别。如果你不设置这个属性，那么放大 8 倍会把你踢回主摄像头。这里选择的值是“51 ”,所以你可以将应用程序中的最大缩放级别提高到 50 倍，但如果你想要可用的照片，我不建议超过 16 倍。

这里有一个 Google 相册，里面有我今天拍的一些照片(包括之前展示的照片):

**[谷歌像素 4 16X 变焦样照](https://photos.app.goo.gl/293GaWoLi8FAvYgd9)**

对于这个模块的任何问题或反馈，[在我们的](https://forum.xda-developers.com/apps/google-camera-mods/gcam-google-pixel-1-2-3-t3875663)[谷歌相机模块论坛](https://forum.xda-developers.com/apps/google-camera-mods)查看 cstark27 的帖子。[在他的论坛帖子](https://forum.xda-developers.com/showpost.php?p=80797211&postcount=1757)中有 Magisk 模块的下载链接和他修改的谷歌相机应用程序的最新版本。

**[谷歌 Pixel 4 论坛](https://forum.xda-developers.com/pixel-4)**| |**|[谷歌 Pixel 4 XL 论坛](https://forum.xda-developers.com/pixel-4-xl)**

这个 mod 的一个非根版本允许使用超过 8 倍变焦的远摄相机应该是可能的，但这可能需要一些时间来完成，因为属性是在库中读取的。我们会继续关注这个 mod 的进一步发展，如果修改者想出了办法，我们会让你知道。