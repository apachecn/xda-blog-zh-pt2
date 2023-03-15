# 谷歌 Pixel 2 在 Active Edge 设置中有一个隐藏的复活节彩蛋

> 原文：<https://www.xda-developers.com/google-pixel-2-hidden-easter-egg-active-edge/>

谷歌最新的旗舰智能手机 Pixel,[Pixel 2 和 Pixel 2 XL](https://www.xda-developers.com/google-pixel-2-xl-announced-price/) 最初推出时搭载了 Android 8.0 Oreo，但后来收到了 Android 8.1 的[开发者预览版。我们在版本中记录了很多](https://www.xda-developers.com/android-8-1-oreo-developer-preview-1/)[的细微变化，但是有些变化比其他的更隐蔽。我们发现的一个变化不是你真正所说的功能，但它符合谷歌给 Android 添加一些隐藏幽默的习惯。在运行 Android 8.1 开发者预览版 1 的谷歌 Pixel 2 和 Pixel 2 XL 的 Active Edge 设置屏幕中，有一个隐藏的复活节彩蛋迷你游戏，需要你挤压手机来弹出泡泡。](https://www.xda-developers.com/android-8-1-oreo-developer-preview-features/)

对于那些不熟悉的人，Pixel 2 智能手机有一个名为 Active Edge 的功能，可以让你挤压手机的下半部分来启动谷歌助手或静音来电。你可以在设置中调整挤压灵敏度(或者用 ADB 命令微调[)，但除此之外，没有太多定制 Active Edge 的方法，](https://www.xda-developers.com/customize-active-edge-squeeze-sensitivity-pixel-2/)[至少官方上是这样的](https://www.xda-developers.com/remap-active-edge-squeeze-google-pixel-2/)。

当我们开始深入研究运行 Android 8.1 的谷歌 Pixel 2 XL 上的最新设置应用程序时，我们发现了一个与 Active Edge 相关的新行，我们认为这可能很有趣。首先，我们在设置中发现了一个名为“AssistGestureBubbleActivity”的新活动

```
 <activity android:enabled="true" android:exported="false" android:hardwareAccelerated="true" android:name="com.google.android.settings.gestures.assist.bubble.AssistGestureBubbleActivity" android:resizeableActivity="false" android:screenOrientation="portrait" android:theme="@android:style/Theme.Material"/> 
```

接下来，我们为这个活动发现了一个相应的布局文件:

### assist _ 手势 _ 气泡 _ 活动. xml

```
 <?xml version="1.0" encoding="utf-8"?>
<FrameLayout n1:layout_width="fill_parent" n1:layout_height="fill_parent"
xmlns:n1="http://schemas.android.com/apk/res/android">
<ImageView n1: n1:layout_width="fill_parent" n1:layout_height="fill_parent" />
<ImageView n1: n1:layout_width="fill_parent" n1:layout_height="fill_parent" />
<TextView n1:textColor="#ffffffff" n1:gravity="end" n1:layout_gravity="top" n1: n1:padding="12.0dip" n1:layout_width="fill_parent" n1:layout_height="wrap_content" />
</FrameLayout> 
```

关键字“游戏视图”和“游戏视图”暗示这是某种复活节彩蛋。由于活动被定义为“未导出”，这意味着它不能在没有 root 用户的情况下从命令行运行，也不能从活动启动器中看到。

但是在 XDA 公认的贡献者的帮助下，我们找到了如何得到这个隐藏的复活节彩蛋。他发现了以下代码:

基本上，这个代码是监听在激活边缘设置下的挤压灵敏度设置的重复点击。如果用户没有禁用复活节彩蛋([通过管理配置文件](https://developer.android.com/reference/android/os/UserManager.html#DISALLOW_FUN))，那么手机将启动一个隐藏的迷你游戏，在那里你挤压你的手机以在屏幕上弹出气泡。

上面的视频是由 XDA 初级成员 [InFlames03](https://forum.xda-developers.com/member.php?u=7322252) 在他们运行 Android 8.1 Oreo 的 Pixel 2 XL 上拍摄的。如果你想知道他们的设置应用程序是如何黑暗的，那是因为他们正在运行[无根底层主题引擎](https://www.xda-developers.com/custom-themes-android-oreo-substratum/)和他们自己的黑暗主题，称为赛的奥利奥主题(你可以在这里找到[如何安装](https://www.xda-developers.com/install-dark-theme-android-oreo-without-root/))。)

我个人认为复活节彩蛋有点乏味。Quinny899 将其描述为“再循环到游戏中的工程测试”公平地说，并不是每个复活节彩蛋都能和安卓棉花糖的 flapphydroid 相提并论，但不管怎样，你玩这个游戏也不会超过几秒钟。