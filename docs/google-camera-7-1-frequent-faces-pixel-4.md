# 谷歌相机 7.1 暗示了 Pixel 4 的“常见面孔”功能

> 原文：<https://www.xda-developers.com/google-camera-7-1-frequent-faces-pixel-4/>

下周，谷歌将在一年一度的谷歌制造活动上正式推出 Pixel 4 和其他 Pixel 品牌的产品。由于过去一个月[的大量泄露](https://www.xda-developers.com/tag/google-pixel4/)，我们知道了很多关于新款 Pixel 智能手机的信息，包括设计、内部硬件和软件功能。Pixel 以其相机实力而闻名，所以我们期待看到它的亮点功能，[天文摄影](https://www.xda-developers.com/google-pixel-4-camera-samples-astrophotograhy-dual-exposure-sliders/)的实际应用。但新的谷歌相机 7.1 APK 可能会与 2019 年的 Pixel 一起推出，它不仅仅会提供更好的夜景。我们刚刚得知，谷歌正在谷歌相机中开发一项名为“频繁面孔”的功能，它可能会在 Pixel 4 上首次亮相。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些特性目前还没有在实时构建中实现，并且可能会被开发人员在未来的构建中随时引入。

上周，我们首先报道了一个更新的像素提示应用程序,展示了一个以前从未见过的相机功能:社交分享。本周早些时候，我们[拿到了谷歌相机应用的 7.1](https://www.xda-developers.com/google-camera-7-1-new-ui-framing-hints-social-share/) 版本，它为所有 Pixel 智能手机启用了新的相机功能。深入研究这一版本，modder [cstark27](https://forum.xda-developers.com/member.php?u=2712580) 发现谷歌正在研究“频繁面孔”，这一功能将自动聚焦于你经常拍照的人。相机应用程序将保存你经常拍摄的面部数据，因此在未来，应用程序将知道自动聚焦谁。面部数据只存储在设备上，只有谷歌相机应用程序可以访问，所以你不必担心数据泄露。如果您禁用该功能，保存的面孔数据将被删除。

有趣的是，该功能的字符串只存在于 7.1 APK for Wear OS 中。7.1.014 版包含描述该功能的字符串，而 7.1.015 版只包含提示您使用该功能并在该功能开启时通知您的字符串。

**7 . 1 . 014 版中的字符串**

```
 <string name="frequent_faces_info">"When you take photos with multiple people, Camera will automatically focus on the people you photograph most.

Frequent Faces data is only saved on this device, and can only be accessed by this Camera app.

When you turn off Frequent Faces, faces data will be deleted.

Frequent Faces will be available when you open Camera from the lock screen."</string>
<string name="frequent_faces_learn_more">Learn more</string>
<string name="frequent_faces_off">Off</string>
<string name="frequent_faces_on">On</string> 
```

**7 . 1 . 015 版中的字符串**

```
 <string name="frequent_faces_on_notification">Frequent Faces is on</string>
<string name="frequent_faces_try_notification">Try Frequent Faces</string> 
```

我检查了主要的 7.1 APK，可以确认代码的频繁面对的功能是存在的。由于这项功能之前没有在任何泄露中显示出来，所以下周 Pixel 4 发布时，它可能还没有准备好。然而，可以肯定的是，假设这项功能没有被淘汰，它最终将在 Pixel 4 上首次亮相。

我们将继续关注这个特性的更多细节。谷歌相机改装者甚至可以在下周之前启动并运行这一功能，或者谷歌可能会推出另一个支持这一功能的相机应用程序更新。

* * *

*感谢 PNF 软件为我们提供了使用许可 [JEB Decompiler](https://www.pnfsoftware.com/?aid=xdadev) ，这是一款针对 Android 应用的专业级逆向工程工具。*