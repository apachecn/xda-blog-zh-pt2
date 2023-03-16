# Snap Kit SDK 允许开发人员集成 Snapchat 的功能

> 原文：<https://www.xda-developers.com/snap-kit-sdk-integrate-snapchat-features/>

Snapchat 背后的公司 Snap Inc .推出了 Snap Kit:一套开发人员工具，允许开发人员在开发人员的应用程序中集成 Snapchat 的一些最佳功能，也便于用户与 Snapchat 社区分享这些应用程序中的瞬间。

Snap Kit 还考虑到了用户的隐私和安全，并设置了一些基本限制来保护用户的隐私(尽管用户与 Snapchat 分享多少内容可能会让隐私意识完全远离平台)。Snap Kit 在登录时仅共享用户的显示名称和 Bitmoji，而当用户使用 Snap Kit 登录时，不会共享用户的朋友数据。使用 Snap Kit SDK 的外部应用程序无法访问用户的电话号码、电子邮件、位置跟踪、朋友图表和人口统计数据。90 天不使用的应用程序也会自动与用户帐户断开连接。返回的用户需要重新认证。

## 快照套件 SDK

Snap Kit SDK 分为四个部分，开发人员可以自由地集成他们最感兴趣的功能。不同的套件如下:

*   **创意套件**:允许开发者将自己的贴纸、滤镜、链接等集成到 Snapchat 的摄像头中。这将使 Snapchatters 能够将外部应用程序的亮点(如高分、锻炼统计数据或新播放列表)直接显示在预览屏幕上，这样他们就可以添加自己的特色，然后在 Snapchat 大家庭中分享。
*   **登录套件**:允许开发者使用 Snapchat 的账户凭证提供一种替代的快速登录应用的方式。这也将让 Snapchatters 将他们的 Bitmoji 头像带进外部应用程序。
*   **Bitmoji Kit** :让 Snapchatters 在开发者的应用中使用 Bitmoji，赋予表情符号一种自己的个性感。
*   **Story Kit** :允许开发者将 Snapchat 故事嵌入到他们的外部平台(应用或网站)中，以展示他们的社区。开发者还可以根据地点、时间、标题等搜索公共故事，这样开发者就可以看到粉丝群在做什么。

请注意，与 Snap Kit 集成的应用程序必须提交给 Snap Inc .进行审查，然后才能公开使用。Snap Inc .将审查所有应用程序，以确保集成和应用程序非常适合 Snap 社区。不幸的是，我们最初翻找文档时没有发现任何审查指南，因此我们担心这个过程可能完全不透明，由 Snap Inc .自行决定。

## 发布合作伙伴

### 邮局食品递送:订购食品和酒

[Postmates](https://play.google.com/store/apps/details?id=com.postmates.android&hl=en) 利用创意套件和登录套件，允许其用户发送带有 Postmates ETA 贴纸的快照。用户还可以在附近捕捉顶部选项。这种集成是实时的，所以你可以安装应用程序来检查它。

### 潘多拉音乐

Pandora 利用创意套件，允许用户发送他们正在听的歌曲的快照。打开 snap 的朋友可以在 Pandora 上滑动鼠标免费听这首歌。用户不必连接他们的 Snapchat 和 Pandora 应用程序就可以利用这一功能。整合的预计时间是本月晚些时候。

### 国外手机交友软件

Tinder 利用 Bitmoji 工具包，允许 Snapchatters 在 Tinder chat 中直接发送 Bitmoji。这次整合的预计时间是 7 月初。

### ScoreStream 高中体育

[ScoreStream](https://play.google.com/store/apps/details?id=com.scorestream.scorestream) 利用创意套件和故事套件，让 Snapchatters 分享当地的实时体育比分，为他们喜欢的球队和球员加油。这次整合的预计时间是 7 月。

### SoundHound -音乐探索&免提播放器

[SoundHound](https://play.google.com/store/apps/details?id=com.melodis.midomiMusicIdentifier.freemium) 利用创意套件，允许用户直接向 Snapchat 分享发现，并在动画快照上完成音乐细节。这种集成目前是活的。

* * *

这些是当前使用 iOS 和 Android 的 Snap Kit SDK 可用的一些集成。我们可以期待更多的应用程序具有类似的集成功能，以增加他们的用户群。

要试用 Snap Kit SDK，请访问 [Snap Kit 门户](https://kit.snapchat.com/portal/)。

[**来源:Snapchat**](https://kit.snapchat.com/#)