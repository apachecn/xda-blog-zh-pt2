# 如何在非 4K 手机和平板电脑上观看 YouTube 4K 视频

> 原文：<https://www.xda-developers.com/how-to-watch-4k-youtube-videos-on-non-4k-phones/>

对许多人来说，移动设备已经取代台式机和笔记本电脑成为内容消费的主要渠道。全球有数亿人使用安卓版的 YouTube 官方应用来了解他们最喜欢的频道。随着 60FPS 选项和 4K 分辨率的引入，YouTube 上的视频质量近年来大幅提高，尽管对于大多数没有 4K 显示器的人来说，YouTube 4K 视频对他们来说根本无法访问。

一些手机，如索尼 Xperia XZ Premium，提供 4K 分辨率的显示器，尽管这是一种例外，而不是规则。索尼 Xperia XZ Premium 的用户可以观看全 4K 分辨率的 YouTube 视频，但大多数其他设备不能。如果你有能力观看 4K 的视频，为什么不选择观看呢？幸运的是，通过简单的 build.prop 修改，任何有根的手机都可以观看 4K 的视频！

上面的截图是在 YouTube 官方应用中的一个 Google Pixel 上拍摄的。谷歌像素有一个 1080p 的屏幕，所以默认情况下，YouTube 上的最高视频质量是 1080p。我们测试这一修改的视频是 MKBHD 的“[4K 状态:2017](https://www.youtube.com/watch?v=f0NdOE5GTgo) ”视频。

通过比较 1080p 和 2160p 的网络流量，我们确认了更高质量的视频流正在被提供。1080p 流的速度为 1.5 Mbps，而 2160p 流的速度为 4.5 Mbps。此外，我的测试人员主观上声称，虽然锐度没有变化，但**的色彩质量和伪像明显改善了**。

关于在低分辨率屏幕上观看 4K 视频的质量，有许多相互矛盾的信息。一些消息来源[声称这比观看原生 1080p 内容](http://www.phonearena.com/news/Did-you-know-4K-vs-1080p-chroma-sub-sampling-and-why-you-should-record-in-4K-even-if-your-TV-does-not-support-it-yet_id61878)更好，而其他消息来源声称下采样不会改变质量。尝试修改一下，自己看看。

* * *

### YouTube 4K 修改

要让 YouTube 应用程序显示 4K 内容，必须满足以下要求:

您所要做的就是使用根文件浏览器(或使用类似于 [BuildProp Editor](https://play.google.com/store/apps/details?id=com.jrummy.apps.build.prop.editor) 的应用程序)修改/system 中的 build.prop 文件，并添加以下行:

```
 sys.display-size=3840x2160 
```

强制关闭 YouTube 应用程序并清除其数据，然后重启手机。当你再次打开 YouTube 时，该应用程序会认为你的手机有 4K 屏幕，所以它会提供这些更高质量的视频。如果你的手机没有硬件 VP9 解码器支持，那么你不会看到 4K 视频选项，但至少你会看到一个 2K 分辨率的选项，如果你还没有看到这个选项的话。

* * *

关注 [XDA 教程 RSS 源](https://www.xda-developers.com/category/tutorials/feed/)获取更多类似的内容。下载 [XDA 实验室](https://www.xda-developers.com/xda-labs/)，快速了解 XDA 门户网站上发布的所有最新新闻和原创专题。

非常感谢 XDA 公认的开发者 [Rizal Lovins](https://forum.xda-developers.com/member.php?u=4666531) ，他最初[在我们的论坛](https://forum.xda-developers.com/crossdevice-dev/sony/guide-enable-2k-youtube-app-4k-xperia-t3617879)上发布了这个方法！