# NewPipe 更新增加了对 Android TV 和 YouTube 音乐解析器的支持

> 原文：<https://www.xda-developers.com/open-source-youtube-client-newpipe-adds-android-tv-support-youtube-music-parser/>

对于那些手机上没有 Google Play 服务的人来说，Android 上的开源 YouTube 客户端 NewPipe 是 YouTube 应用程序的一个很好的替代选择。客户端不使用 YouTube APIs，只是解析 YouTube 网站提取数据，播放你想要的视频，没有任何限制，也没有广告。由于 NewPipe 的工作方式，它还规避了谷歌可能添加到 YouTube 应用程序的任何限制。例如，YouTube 最近在印度将智能手机上的视频质量限制在 480 p,此前印度为应对新冠肺炎疫情实施了全国范围的封锁。但是用户可以通过使用 NewPipe 很容易地克服这个限制。

现在，为了让客户端对用户更有用，NewPipe 背后的开发者正在推出一个重大更新，为 Android TV 提供支持，添加了 YouTube 音乐解析器等等。根据开发人员最近的博客帖子，NewPipe 版本 0.19.3 现已向用户推出，它带来了以下值得注意的变化:

### Android 电视支持

虽然你已经可以在 Android 电视上运行之前版本的 NewPipe，但是客户端并没有正式支持这个平台。由于这个原因，客户有一些问题，使它实际上无法使用。随着最新的更新，开发人员已经解决了所有这些问题，现在你可以在你的 Android 电视上使用 NewPipe，而不会遇到任何烦人的错误。

更新之后，你将能够滚动浏览长视频描述，关注屏幕上的任何元素，使用原生键盘而不是屏幕键盘，以你喜欢的方式搜索视频，并且不会遇到令人讨厌的涟漪效应。要在您的 Android 电视上试用 NewPipe，您可以从下面的 GitHub 链接下载 APK，并将其加载到您的电视上。

### YouTube 音乐解析器

在最新的更新中，NewPipe 还获得了原生解析 YouTube 音乐库的能力，并允许用户轻松搜索音乐。要在客户端搜索 YouTube 音乐内容，您可以点击搜索 UI 中的过滤器按钮，然后选择歌曲、视频、专辑或播放列表来查看 YouTube 音乐的搜索结果。

除了前面提到的变化，NewPipe v0.19.3 还为客户端带来了大量的改进和错误修复。以下是最新更新的完整变更日志:

*   新的
    *   搜索 YouTube 音乐
    *   基本 Android 电视支持
*   改良的
    *   改进了对新版本的检查
    *   避免对已保存流的上传日期进行不必要的更改
    *   在首选项中保存和恢复回放参数
    *   当内容不被支持时显示消息而不是崩溃
    *   改进了抽屉标题的大小处理
    *   改进的弹出播放器缩放手势
    *   长按背景和频道中的弹出按钮，将流排入队列
    *   增加了从本地播放列表中删除所有观看的视频的功能
*   固定的；不变的
    *   修复了订阅片段中组排序按钮的可见性
    *   修复了网络相关异常的检测
    *   固定年龄限制内容设置不起作用
    *   修正了某些种类的夺回
    *   修复了播放列表为空时打开书签时的崩溃问题
    *   修复了使用 nanojson 而不是 org.json 报告的崩溃所导致的 JSON 中的转义
*   发展
    *   添加了 Checkstyle 来构建脚本和代码风格改进
    *   通过确保调试 apk 文件名仅用于调试版本，修复了 F-Droid 版本
    *   对 Gradle 强制使用 UTF-8 编码

**[从 GitHub](https://github.com/TeamNewPipe/NewPipe/releases) 下载 NewPipe(v 0 . 19 . 3)T3**

* * *

**来源: [NewPipe 博客](https://newpipe.schabi.org/blog/release/pinned/newpipe-0.19.3-release/)**