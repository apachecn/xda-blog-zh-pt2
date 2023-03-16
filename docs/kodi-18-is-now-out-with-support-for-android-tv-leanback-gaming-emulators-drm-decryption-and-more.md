# Kodi 18 现在支持 Android 电视后仰、游戏模拟器、DRM 解密等等

> 原文：<https://www.xda-developers.com/kodi-18-is-now-out-with-support-for-android-tv-leanback-gaming-emulators-drm-decryption-and-more/>

Kodi 是最受欢迎的免费开源软件，用于管理您的个人多媒体收藏，无论是离线还是在线。它的跨平台特性让你可以将它安装在几乎任何机器上，甚至是像 Raspberry Pi 这样的物联网设备上。Kodi 能够将您的 PC、笔记本电脑、电视、智能手机或平板电脑变成机顶盒。在数以千计的免费插件和附件的帮助下，您可以轻松地观看电影、电视、流媒体音乐等等。Kodi 最初是由 XBMC 基金会开发的，从那以后他们一直维护着这个平台。昨天，他们发布了 Kodi 的第 18 个主要版本“Leia”，达到了一些伟大的里程碑:

*   接近 10，000 次提交(代码块已更改)
*   超过 3000 个拉请求(一次提交的提交集合)
*   近 9，000 个更改的文件
*   添加了将近 50 万行代码，删除了差不多同样多的代码
*   超过 36 个开源开发者

让我们深入了解 Kodi 18 引入的主要功能。第一个是复古游戏支持。Kodi 现在支持游戏模拟器、侧装 rom 和控制游戏。从现在起，如果你想在树莓派上玩一些复古游戏，你就不必在 RetroPie 内部安装 Kodi 了。Kodi 18 最后还包括 DRM 解密支持，这将允许用户流式传输一些受保护的视频内容。除此之外，你还可以将 Kodi 与 Android TV 集成。最新的向后倾斜功能增加了谷歌助手的支持，具有完整的语音功能，以及 Android TV 中的建议和其他好东西。

Kodi 18 还包括新的音乐库。在这里，您可以过滤、排序并轻松访问所有音频内容。创建新库也比以往更加容易。不太引人注目的功能包括蓝牙支持、新的可视化和屏保。Kodi 18 Leia 还有更多的功能，你可以在下面的 Kodi 博客中看到所有功能的列表。以下是 Android 特有的变化:

### Kodi v18 (Leia) Android 专用变更日志

*   移动到 Android API 26 和 SDK 26，最低为 NDK 18(意味着至少仍需要 Android 5.0)
*   在 Android 电视上的 Kodi OSD 键盘中增加了语音到文本的支持(由遥控器上的语音按钮触发)
*   增加了支持 Android 将 Kodi app 移动到 SD 卡^([【144】](https://kodi.wiki/view/Kodi_v18_(Leia)_changelog#cite_note-144))
*   增加了对安卓电视后仰搜索和推荐元数据的支持，元数据来自 Kodi^([【145】](https://kodi.wiki/view/Kodi_v18_(Leia)_changelog#cite_note-145))
    *   Android TV 对随机未观看电影和音乐专辑的向后倾斜建议的默认设置^([【146】](https://kodi.wiki/view/Kodi_v18_(Leia)_changelog#cite_note-146))
*   将 Android mediacodecssurface^([【147】](https://kodi.wiki/view/Kodi_v18_(Leia)_changelog#cite_note-147))的渲染类型从 GUILayer 更改为 VideoLayer
*   改为使用 Android MediaCodec 的 NDK 原生 C 接口(为了性能增益)^([【148】](https://kodi.wiki/view/Kodi_v18_(Leia)_changelog#cite_note-148))
*   更改为通过原生 Android API 支持 ZeroConf(并反对 mDNSresponder)^([【149】](https://kodi.wiki/view/Kodi_v18_(Leia)_changelog#cite_note-149))
*   更改为通过原生 Android API 支持网络信息(并反对 POSIX)^([【150】](https://kodi.wiki/view/Kodi_v18_(Leia)_changelog#cite_note-150))
*   为了更好的一致性^([【151】](https://kodi.wiki/view/Kodi_v18_(Leia)_changelog#cite_note-151))，改变了通过 JNI 对 Kodi 的 Java 接口的处理

* * *

[**来源:Kodi 发布公告**](https://kodi.tv/article/kodi-180)