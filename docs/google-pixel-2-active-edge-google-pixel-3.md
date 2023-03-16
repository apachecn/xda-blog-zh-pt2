# 谷歌 Pixel 2 的主动边缘挤压功能将在谷歌 Pixel 3 上回归

> 原文：<https://www.xda-developers.com/google-pixel-2-active-edge-google-pixel-3/>

HTC 在过去的几年里表现不太好，但这并没有阻止该公司不时地生产一些非常棒的手机。HTC U11 的挤压功能看起来像是一个一次性的噱头，但由于 HTC 和谷歌之间的[密切合作，它已经成为了](https://www.xda-developers.com/google-signs-1-1-billion-deal-to-acquire-htcs-pixel-smartphone-team-non-exclusive-ip-rights/)[谷歌 Pixel 2 和谷歌 Pixel 2 XL](https://www.xda-developers.com/google-pixel-2-xl-announced-price/) 的一部分。谷歌 Pixel 2 上名为“ [Active Edge](https://www.xda-developers.com/tag/active-edge/) ”的功能可以让你挤压设备的框架来启动谷歌助手，并使闹钟、定时器、通知和来电静音。它不像 HTC U12+ 上的 [Edge Sense 2.0 那样可定制(至少，](https://www.xda-developers.com/htc-u12-official-specifications-features/)[不是正式的](https://www.xda-developers.com/customize-google-pixel-2-active-edge-sense-plus/))，但它完成了任务。对于那些喜欢这项功能的人来说，我们有一些好消息——我们有强有力的证据表明，它将在谷歌 Pixel 3 和谷歌 Pixel 3 XL 上回归。

现在，对于那些大喊“它当然会回来”的人来说，请记住谷歌在后来的智能手机中删除现有功能的历史。谷歌 Nexus 4、谷歌 Nexus 5、谷歌 Nexus 6 和谷歌 Nexus 7 (2013)上的无线充电在谷歌 Nexus 5X 和谷歌 Nexus 6P(以及所有后续的谷歌 Pixel 手机)上被删除。)谷歌在谷歌 Pixel 和谷歌 Pixel XL 发布会上取笑苹果移除的耳机插孔在谷歌 Pixel 2 和谷歌 Pixel 2 XL 上被移除了。我们不认为他们会删除 Active Edge，但可能性仍然存在，因为没有其他确认。自从收购了参与制造 Pixel 2 的 HTC 工程师以及来自 HTC 的知识产权后，谷歌似乎拥有了他们在未来智能手机中继续实现 Pixel 2 挤压功能所需的一切。只是这一次，谷歌 Pixel 3 将由富士康制造[。](https://www.xda-developers.com/google-pixel-3-xl-foxconn-dual-front-camera-lenses-verizon-exclusive/)

## 谷歌 Pixel 3 的 Active Edge 证据

我们的第一点证据来自我们的线人，XDA 资深会员 [meraz9000](https://forum.xda-developers.com/member.php?u=4287865) ，他发布了据称是谷歌 Pixel 3 XL 原型机的第一张真实照片。他与我们分享了[更多的图片和细节](https://www.xda-developers.com/google-pixel-3-xl-glass-back-display-notch/)，比如这款智能手机可能有玻璃背面(他说，这肯定不是塑料或金属)。他无法确认无线充电是否存在，但我们挖掘了 [Android P beta 2](https://www.xda-developers.com/android-p-beta-2-google-pixel-2/) (开发者预览版 3)并找到了[无线充电底座](https://www.xda-developers.com/android-p-wireless-charging-dock-google-pixel-3/)的证据，我们认为这是谷歌 Pixel 3 的无线充电底座，所以随你便吧。他*确实*向我们报告说，在他不小心软制了设备(这就是为什么他的泄露在引导程序上显示了设备)之前，他报告说通过挤压他的手机测试 Active Edge，并且手机振动。我相信他的信息是可信的，但为了确保万无一失，我决定在最新的 Android P 开发者预览版中寻找任何确凿的证据。我做到了。

在 SystemUIGoogle APK 中,“WakeMode”类已经用一些新代码进行了轻微的修改。“WakeMode”是位于/com/Google/Android/systemui/**El Myra**/gates 下的一个类。顺便说一下，埃尔迈拉是主动边缘的代号。

在这个类中有一个名为 isWakeSettingEnabled 的方法。该方法检查[设置的值。secure . assist _ gesture _ wake _ enabled](https://android.googlesource.com/platform/frameworks/base/+/master/core/java/android/provider/Settings.java#6916)如果它返回“1”，那么这意味着挤压手势也应该将手机从睡眠中唤醒。如果它返回“0”，那么挤压不会唤醒手机。不过，你不能在任何手机上将这个值设置为“1”就指望它能工作。显然，你的手机需要一个可挤压的框架...此外，该方法本身会检查您的设备是否兼容。恰好这个方法增加了检查“`ro.product.model`”的代码，这是一个定义设备名称的系统属性值。在 Google Pixel 2 XL 上，`ro.product.model=Pixel 2 XL`)“交叉线”和“蓝线”是该方法检查的两个产品模型。我们已经知道“交叉线”是早期泄露的谷歌 Pixel 3 XL，所以我们假设“蓝线”是更小的谷歌 Pixel 3。

*左图:谷歌 Pixel 3 XL 原型在引导程序屏幕上显示“交叉线”代号。*

*右图:谷歌 Pixel 2 的 Active Edge 设置显示“关闭屏幕时允许”(设置。secure . assist _ gesture _ wake _ enabled*T2)

因此，不难得出结论，主动边缘挤压功能将回归谷歌 Pixel 3 和谷歌 Pixel 3 XL。它可能会在最终生产开始前被废弃，因为我们的信息是基于工程原型样本和 Android P Developer Preview 3 中的代码，所以如果有任何事情与我们的说法相矛盾，我们一定会让你们知道。在那之前，请继续关注 XDA 门户网站，了解关于 Pixel 3 的更多信息！