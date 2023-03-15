# Chrome 的开发频道为 Chromecast 增加了一个隐藏的“媒体遥控”功能

> 原文：<https://www.xda-developers.com/chromes-dev-channel-adds-a-hidden-media-remoting-feature-for-chromecast/>

数百万人使用他们的 Chromecast 在电视上观看媒体，许多人直接从 Chrome 本身的一个标签上观看。如果视频服务不直接支持 Chromecast，你可以简单地将整个标签页投射到电视上，然后以全屏模式播放视频。谷歌意识到，由于电池寿命和视频质量的下降，这不是最好的解决方案。为了改善这种体验，该公司正在试验一种新的“铸造标签”功能。

这一新功能目前可以在 Chrome 的开发者频道中获得，因为它还处于早期开发阶段。所以有可能这里或那里有一些虫子。你还需要深入到 *chrome://flags* 页面，然后寻找#media-remoting 开关。一旦找到，就像平常一样启用它，然后重启 Chrome，这样改动就可以生效了。然后是时候测试这个特性了。

Chrome 开发团队的 Franç ois Beaufort 建议去 Vimeo 这样的网站，然后找一个视频进行测试。开始播放视频后，展开 Chrome 菜单，然后点击“Cast ...”选项启动到您的电视演员。完成后，您可以将视频置于全屏模式，媒体远程功能应该会自动启动。因为它检测到你正在播放视频，你应该在屏幕上看到不同。

这种新的媒体远程功能可以直接将视频内容比特流转发到 Chromecast 连接的任何设备。因此，它不会将 Chrome 标签的内容转移到屏幕上，而是知道你只想观看视频并生效。博福特先生说，这种方法不仅能延长电池寿命，还能保持视频质量不变。

[**来源:+FrancoisBeaufort**](https://plus.google.com/+FrancoisBeaufort/posts/bCAFwn7EQGi)