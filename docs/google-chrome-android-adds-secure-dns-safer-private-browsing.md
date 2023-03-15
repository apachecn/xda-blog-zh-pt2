# 谷歌 Android Chrome 浏览器增加了安全域名系统，使浏览更加安全、私密

> 原文：<https://www.xda-developers.com/google-chrome-android-adds-secure-dns-safer-private-browsing/>

# 谷歌 Android Chrome 浏览器增加了安全域名系统，使浏览更加安全、私密

Google Chrome for Android (v85)为浏览器增加了安全 DNS 功能，为用户提供了更安全、更私密的浏览体验。

随着今年 5 月早些时候 Chrome 83 的发布，谷歌为桌面版浏览器引入了新的安全 DNS 功能。该功能利用 HTTPS DNS 来加密一个被称为“DNS(域名系统)查找”的步骤，以确保用户更安全、更隐私的浏览体验。现在，该公司已经开始推出谷歌 Chrome 85，将该功能引入 Android 设备。

根据谷歌最近的一篇博客文章，Chrome 85 为 Android 版 Chrome 带来了对安全 DNS 的支持，并与桌面版本共享相同的设计原则。有了这项功能，如果你当前的 DNS 提供商支持这项功能，Chrome 将自动切换到 HTTPS 域名系统(DoH)。自动模式将确保 Chrome 可以退回到用户当前提供商提供的常规 DNS 服务(包括 DNS-over-TLS，如果配置的话)，以确保用户不会面临任何中断，同时定期重试以保护 DNS 通信。

如果默认行为不适合用户，谷歌 Chrome 还会给用户一个手动配置选项，让他们使用特定的提供商，而没有退路。此外，用户将能够从浏览器设置中完全禁用该功能。

这篇博客文章进一步补充说，Chrome 将自动禁用安全 DNS*“如果它通过一个或多个企业政策的存在检测到一个受管理的环境。”*谷歌还增加了 HTTPS 域名系统企业政策*“允许安全域名系统的管理配置，并鼓励 IT 管理员考虑为他们的用户部署 HTTPS 域名系统。”*与桌面版一样，Android 版 Chrome 的安全 DNS 将在一段时间内向用户推出，以确保稳定性和性能。逐步推出也将*“帮助卫生部提供者相应地扩展他们的服务。”*

同样值得注意的是，自从谷歌[去年因 HTTPs 协议上的 DNS 而受到来自 ISP](https://www.xda-developers.com/congress-google-chrome-private-dns/)的一些抵制后，该公司补充说，它将*“继续对反馈持开放态度，并与感兴趣的各方合作，如移动运营商和其他 ISP、DNS 服务提供商和在线儿童安全倡导者，以在保护 DNS 方面取得进一步进展。”*

* * *

**来源:[铬博客](https://blog.chromium.org/2020/09/a-safer-and-more-private-browsing.html)**