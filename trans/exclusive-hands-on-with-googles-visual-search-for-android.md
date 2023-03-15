# 谷歌 Android 可视化搜索实践

> 原文：<https://www.xda-developers.com/exclusive-hands-on-with-googles-visual-search-for-android/>

世界上有如此多的信息，互联网搜索引擎对获取知识至关重要。通过台式机或笔记本电脑上的网络浏览器、智能手机或平板电脑上的专用应用程序，或者通过智能手表或家庭助理设备上的语音，您可以获得如此多的选项来找到您想要的信息。绝大多数网络搜索仍然是通过文本查询进行的，尽管谷歌眼镜的出现是将视觉搜索带给大众的一个有希望的开始。可悲的是，由于缺乏更新，Goggles 已经半途而废，但最近在 I/O 上宣布的[谷歌镜头](https://www.xda-developers.com/google-lens-introduced-at-io-allows-you-to-connect-to-a-wifi-network-by-pointing-your-camera/)似乎正在复兴这个概念。我们能够接触到谷歌应用程序的新视觉搜索功能，尽管我们无法确认这是否与谷歌镜头相同。

* * *

### 谷歌的视觉搜索

从我们所知的谷歌眼镜的实际工作原理来看，它似乎是谷歌眼镜的兴奋剂。谷歌的图像识别已经非常强大，但由于谷歌不断增长的人工智能实力，谷歌眼镜不仅能够识别所有不同类型的物体，还能够提供上下文相关的结果。Lens 将能够与谷歌的其他服务接口，以提供更个性化的反馈。

总之，理论上是这样的。除了在 Google I/O 上展示 WiFi 网络连接的快速演示之外，还有很多我们不知道的关于 Google Lens 的细节。但至少，我们可以看看它在谷歌应用中的界面是什么样的。

**请注意，以下截图可能并不代表最终的谷歌视觉搜索产品。该功能被明确标记为“测试版”，因此我们的服务问题(详见下文)可能会在最终版本中得到解决。此外，这意味着界面可能会发生变化。**

正如你所看到的，界面由屏幕上半部分的大相机取景器和底部的类别列表组成。图像识别类别包括:

*   全部
*   衣服
*   鞋子
*   手提包
*   太阳镜
*   条形码
*   制品
*   地方
*   猫
*   狗
*   花

当你选择一个类别，我们怀疑视觉搜索缩小其数据库，以更快地完成查询。在任何情况下，一旦你选择了一个类别(或坚持“全部”)，然后开始搜索你只需在相机取景器的任何地方点击。如果周围太暗，您可以通过点击左上角的闪光灯图标来启用相机闪光灯。

执行搜索将显示结果的卡片视图列表。你可以左右滑动来查看所有结果。点击一个结果将打开一个与该商品或产品相关的谷歌搜索页面，尽管你可以通过滚动搜索页面顶部的迷你卡片视图来轻松选择另一个结果的搜索页面。打开任何视觉搜索结果上的三点菜单，也可以直接访问图像源，很像谷歌的桌面图像搜索。

我们测试了来自网络的静态图片和实时图片的视觉搜索。正如你所料，视觉搜索在静态图片上表现出色，但我们无法让这个测试版处理实时图片。我试图让它识别 PlayStation 4 和我自己的 Google Home 的 DualShock 4 无线控制器，但在这两种情况下，它都无法识别它。鉴于我们拿到的是 beta 测试版本，我们不能说这是产品的一个错误。老实说，如果视觉搜索的实时版本不能识别像谷歌主页这样的东西，我会感到震惊(尽管我有一部分希望它会可笑地误认为是空气清新剂)。

* * *

### 视觉搜索和谷歌镜头一样吗？

我们进行的搜索都没有显示出 Google Lens 在 Google I/O 舞台上展示的智能迹象。然而，最新的 Google App APK 文件中的几个字符串确实显示了这两者之间的联系。在 search_widget.xml 布局文件中有一行提到 Google search 小部件可能会添加一个按钮来启动可视化搜索。但是最有趣的是，这个可以向用户直观地识别这个特性的 drawable 被命名为“google_lens”。

```
 <ImageButton android:orientation="horizontal" android: android:background="@drawable/search_box_click_on_transparent" android:paddingLeft="8.0dip" android:paddingTop="8.0dip" android:paddingBottom="8.0dip" android:visibility="gone" android:layout_width="56.0dip" android:layout_height="fill_parent" android:src="@drawable/google_lens" android:scaleType="centerInside" android:contentDescription="@string/accessibility_visual_search_button" android:layoutDirection="locale" /> 
```

上图所示的图标与谷歌 I/O 发布谷歌镜头时显示的图标完全相同。

此外，这个相同的图标出现在另一个名为 navigation_menu.xml 的文件中。该文件定义了哪些元素将出现在 Google 应用程序的侧边栏菜单中。这项新功能的名字将被称为视觉搜索，但它的图标来自镜头。

```
 <com.google.android.apps.gsa.shared.ui.drawer.DrawerEntry android: android:tag="ve=37333;track:click" android:visibility="gone" android:layout_width="fill_parent" android:layout_height="wrap_content" thegoogle:imageSrc="@drawable/quantum_ic_google_lens_grey600_24" thegoogle:text="@string/visual_search" /> 
```

因此，把二加二放在一起并不太难。很有可能谷歌的视觉搜索实际上是谷歌镜头，尽管让我有点犹豫的是，这是从谷歌应用程序中访问的，而不是在谷歌 I/O 上承诺的谷歌助手中访问的。此外，由于我无法让任何智能功能工作(并且界面不像谷歌 I/O 上显示的那样)，我不能肯定地说我玩的是谷歌镜头。

不过，我们很高兴看到谷歌镜头在实践中的表现，特别是考虑到三星 Bixby Vision 的努力令人失望。谷歌的 I/O 演示很简洁，但我个人会推迟，直到我们可以自己尝试一下。

* * *

**你如何看待谷歌镜头？请在下面的评论中告诉我们你的想法！**