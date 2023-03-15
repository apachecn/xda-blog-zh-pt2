# 【更新】以下是谷歌 Pixel 2 的 Now Playing 功能可以识别的 10000+首歌曲

> 原文：<https://www.xda-developers.com/google-pixel-2-now-playing-song-list/>

**2017 年 10 月 19 日更新:** Google 主动联系我们，告知我们数据库每周更新，是区域性的，可以识别数万首歌曲。请[阅读这篇后续文章](https://www.xda-developers.com/how-google-pixel-2-now-playing-works/)了解更多详情。

* * *

谷歌 Pixel 2 的最新功能被称为 Now Playing，它所做的是自动检测背景中播放的歌曲，并在锁定屏幕上显示有关它的信息。谷歌表示，环境音乐识别功能可以离线工作，不需要将任何数据卸载到服务器上来帮助歌曲识别。此外，该公司表示，他们的数据库可以匹配超过 10，000 首歌曲，并且该数据库可以更新，以支持在未来识别更多歌曲。

但是谷歌到底选择了哪些歌曲作为它最初的正在播放的识别数据库呢？经过一番挖掘，我们现在可以分享谷歌 Pixel 2 的 Now Playing 功能可以识别的的 10，000 多首歌曲的完整列表。我们通过提取位于`/system/etc/ambient`中的 53MB matcher.leveldb 文件实现了这一点。

LevelDB 是一个键值存储库，我们认为它包含了 Now Playing 特性的歌曲列表。我们将这个文件发送给了 Kieron Quinn，在我们的论坛上被称为 XDA 公认的贡献者 [Quinny899](https://forum.xda-developers.com/member.php?u=3563640) ，他确认了这个文件确实是 Pixel Ambient Services 应用程序所需的数据库(该应用程序具有“正在播放”功能)。

当试图运行这个应用程序时，应用程序会崩溃，并指出它“无法找到音乐识别器核心碎片。”在 APKTool 的帮助下，Quinny899 能够找到抛出该错误信息的代码。瞧，Pixel 环境服务寻找的文件是 matcher.leveldb 文件。

确认这一点后，Quinny899 运行一个[脚本](https://github.com/golang/leveldb/tree/master/cmd/ldbdump)来转储数据库的内容，然后他的另一个脚本解析结果来修复格式。结果是“[谷歌像素环境歌曲列表](http://quinny898.co.uk/resources/pixel-songs/)”，这是一个包含 17，300 首歌曲的表格，包含现在播放的每首歌曲的歌曲名称和艺术家。

为什么是 17300？没有特别的原因。Quinny899 不确定这是否是所有的歌曲，因为脚本可能没有转储所有的歌曲。有些歌曲也不止出现一次，但我们怀疑里面有成千上万的重复。

请记住，虽然现在播放的歌曲列表很可能是全面的，但在未来可能不是。这是因为，如前所述，谷歌将更新他们的数据库。目前还不清楚更新数据库是否需要 OTA 更新，或者 Pixel Ambient Services 应用程序是否可以自行更新数据库。

* * *

## “环境意识”的最新情况

鉴于匹配的名称和主题，我们早些时候认为这一功能与之前对一种名为“ [AmbientSense](https://www.xda-developers.com/google-pixel-2-now-playing-ambientsense-battery-drain/) 的技术的研究有关，但谷歌向我们表示，他们现在播放的功能不是基于 AmbientSense。据推测，这意味着与 AmbientSense 文件匹配的应用程序包名称是不相关的。我们已经联系了谷歌以获取更多关于正在播放功能的信息，当我们收到回复时会更新我们的文章。