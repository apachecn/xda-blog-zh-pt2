# 新的谷歌浏览器标志将在桌面的 omnibox 中显示完整的网址

> 原文：<https://www.xda-developers.com/google-chrome-flag-show-full-url/>

# 新的谷歌浏览器标志将在桌面的 omnibox 中显示完整的网址

Chrome 76 使得整个 URL 不会显示在 omnibox 中。一个新的 Chrome 标志将允许用户显示完整的网址。

人们喜欢 Chrome 浏览器的原因之一是它简单的设计。虽然在性能方面可能感觉不到轻量级，但界面仍然干净简单。然而，有时这种简单会走得太远。Chrome 76 从 omnibox 中移除了部分 URL，但一个新的 Chrome 标志可以将它带回来。

从 Chrome 76 开始，omnibox 不显示完整的 URL。网站名称(www，HTTP 或 HTTPS)前的一切都被切断。所以“https://www.xda-developers.com”看起来像“xda-developers.com”，你必须在 omnibox 中点击两次才能看到完整的 URL(一次点击突出显示 URL，第二次点击显示完整的内容)。这种行为惹恼了许多开发人员，正如在这个反馈帖子中记录的[。](https://bugs.chromium.org/p/chromium/issues/detail?id=883038)

谷歌决定“让网址更容易阅读和理解，并消除可注册域名的干扰。”他们声称这些 URL 组件“与大多数 Chrome 用户无关”虽然这可能是真的，但它们与某些人有关，而且目前没有内置的方法来恢复它们。谷歌目前的“官方”解决方案是使用“[可疑网站举报人](https://chrome.google.com/webstore/detail/suspicious-site-reporter/jknemblkbdhdcpllfgbfekkdciegfboi)”扩展。

幸运的是，Chromium Gerrit 中的一个新提交为 omnibox 中的上下文菜单选项添加了一个标志，以显示完整的 URL。一旦这个开关打开，它就会一直开着。提交还没有被合并，但是当它被合并时，它将位于chrome://flags # context-menu-show-full-URLs。该标志仅适用于桌面版 Chrome。我们很高兴谷歌至少在考虑这个问题，但人们已经抱怨了很长时间。