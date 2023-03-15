# 使用 Xposed 模块向您所有的朋友发送 Snapchats

> 原文：<https://www.xda-developers.com/xposed-snapchat-mass-send/>

# 轻松向您所有的朋友群发 Snapchat 消息

当您向朋友发送 snapchats 时，Xposed 模块会插入“全选”和“取消全选”选项。

Snapchat 徽标

尽管 Snapchat 本质上明显不安全，但它确实是一种与朋友交流的有趣方式。虽然如果你使用售后客户或任何其他方法来保存数据，你在镜头前做出的那些非常丑陋的面孔在技术上可以超过 10 秒，但大多数普通用户不会这样做，所以这有点像在各种电影中用作情节元素的[自毁磁带](http://www.techweekeurope.co.uk/wp-content/uploads/2012/05/phelpstape.jpg)。但是当*有很多*朋友需要看你难看的自拍照时，不得不单独选择你名单上的每个朋友来发送你的 Snapchat，这可能会相当烦人和乏味。

XDA 论坛成员 [dapaintballer331](http://forum.xda-developers.com/member.php?u=2276986) 开发了一个 Xposed 模块，为这个问题提供了一个简单的解决方案:在 UI 中包含“全选”和“取消全选”复选框。标签说明了一切；如果您想将您的 Snapchat 发送给好友列表中的每一个人，您只需勾选“全选”,或者如果您随后意识到这可能不是一个好主意，您可以选择“取消全选”。但是，当您可以将它包含到您的 Snapchat 故事中时，为什么还要有它呢？嗯，一个可能的原因是，不是每个人都倾向于查看你的 Snapchat 故事，另一个可能是，你故事中的 Snapchat 实际上持续了 24 小时，而不是几秒钟。

如果这听起来像是你想尝试的东西，请查看[Snapchat Select All x posed Thread](http://forum.xda-developers.com/xposed/modules/mod-snapall-select-snapchat-stories-t2957399)了解更多信息。请记住，正如我们过去多次提到的那样，Snapchat 和其他信任客户端设备的机制并不安全，你的信息很容易被你的浏览者存储。