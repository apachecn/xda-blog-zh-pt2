# 如何从共享菜单中删除直接共享

> 原文：<https://www.xda-developers.com/remove-direct-share-share-menu-root/>

直接分享是那些表面上看起来有用，但实际上却令人讨厌的功能之一。每当你打开“共享”菜单时，它就会出现，并将其他应用程序中联系人的快捷方式放在顶部。我相信许多人都会同意，他们通常不会*最终直接在共享菜单中选择他们的一个联系人，还有一个事实是，它会导致共享菜单跳转，这可能会让你错过你想要的点击。如果你宁愿完全取消这些联系人的建议，你可以在 LG 和三星手机上禁用它们，而不用 root，也可以通过 Intent Firewall 在其他手机上禁用它们。*

首先，如果您有一台 LG 或三星设备，那您就走运了。两个原始设备制造商都在其设备设置中包含了禁用该功能的方法。在三星手机上，您只需要转至“高级功能”部分并禁用“直接共享”在 LG 手机上，进入**网络标签**、**共享&连接、**最后进入**共享面板**。如果您没有这些设备，请继续阅读。

我们建议使用 Magisk 之类的根解决方案。您还需要一个支持根的文件浏览器。我个人推荐 MiXplorer。

[appbox xda com.mixplorer]

### 步骤 1 -创建 XML 文件

您需要创建一个 XML 文件，但是名称并不重要。意图防火墙将读取任何 XML 文件，不管其名称如何。为了简单起见，我将我的命名为“disable-direct-share.xml”。将以下内容粘贴到文本编辑器中。

```
 <rules>
  <service block="true" log="true">
    <intent-filter>
      <action name="android.service.chooser.ChooserTargetService" />
    </intent-filter>
  </service>
</rules> 
```

现在保存文本文件并关闭它。

### 步骤 2 -移动文件

这是需要 root 的部分，因为我们必须通过将文件放在/data/system/ifw 中来直接修改/data。只要把它复制到那个文件夹里，就大功告成了。你甚至不需要重启。

### 第 3 步-测试它！

差不多就是这样。只需尝试共享一个项目，您应该会注意到，不再有任何联系人建议您发送项目。

### 意图防火墙-我们所做的

意图防火墙是 Android 4.4.2 中引入的一个功能，但是还没有正式的文档。因此，它不仅会随时改变，而且也不是官方支持的特性。但这并不意味着我们不能利用它，因为您需要的只是 root 访问权限。当我们将文件添加到/data/system/ifw 时，意图防火墙将扫描任何。它检测到文件夹中的 XML 文件已被修改，并尝试分析其规则。然后，有效的规则将应用于整个系统。我们利用这一点来阻止来自 ChooserTargetService 的广播，ChooserTargetService 负责发送广播来询问应用程序在 Direct Share 下显示什么。如果 ChooserTargetService 无法广播该请求，则直接共享菜单无法显示，因为没有应用程序会响应。Intent 防火墙还有很多其他用途，甚至 GitHub 上的一个用户利用它来帮助防止由于调用不必要的服务而导致的电池耗尽[。](https://github.com/LaelLuo/Intent-Firewall-List)

当然，如果你有一个三星或 LG 设备，那么你不应该这样做，而是应该在你的设置中禁用这个选项。Google anywhere 没有记录 Intent Firewall，这表明它要么没有完成，要么已经被放弃。系统似乎也没有在任何场合使用它。意图防火墙并不是阻止意图和广播的最强大的解决方案，但它是目前唯一的方法。它完成了工作，尤其是在这种情况下，并且可能还有其他重要的用途。

* * *

[**来源:rehh(stack exchange)**](https://android.stackexchange.com/questions/128053/removing-a-contact-from-direct-share-panel/160350#160350)

[**Via:/u/forbid reality(Reddit)**](https://www.reddit.com/r/Android/comments/9ijt3z/psa_how_to_remove_direct_share_from_share_menu/)