# 谷歌 Chrome 将阻止 HTTPS 页面加载不安全的内容

> 原文：<https://www.xda-developers.com/google-chrome-block-insecure-content-loading-https-pages/>

为了保护用户，谷歌[今年早些时候开始用 Chrome 68 给 HTTP 网站贴上“不安全”的标签。由于这一变化，用户在浏览潜在不安全的网站时更容易发现。此外，它还促使开发人员用 SSL 证书更新他们的网站。现在，为了进一步加强安全性，谷歌正在努力防止不安全的 HTTP 子资源加载到 HTTPS 页面上。](https://www.xda-developers.com/google-chrome-68-http-not-secure/)

在 Chromium 博客最近的一篇文章中，该公司概述了完全屏蔽混合内容的步骤。对于不知情的人来说，HTTPS 页面通常以混合内容为特色，其中一些子资源通过 HTTP 不安全地加载。尽管浏览器在默认情况下会屏蔽许多类型的混合内容，但图像、音频和视频仍然可以加载。这可能会允许攻击者篡改混合内容并危及用户安全。

因此，从 [Chrome 79](https://www.xda-developers.com/google-chrome-canary-adds-a-shared-clipboard-feature-for-android-and-pc/) 开始，浏览器将逐渐默认阻止所有混合内容。为了防止网站因这一变化而中断，谷歌将自动升级混合资源到 HTTPS。然而，用户仍然可以选择不屏蔽特定网站上的混合内容。该公司还为开发者提供资源，帮助他们找到并修复网站上的混合内容。

在将于今年 12 月发布到稳定频道的 Chrome 79 中，谷歌将引入一个新的设置来解锁混合内容。新的设置将适用于混合脚本、iframes 和 Chrome 当前默认阻止的其他混合内容。混合的音频和视频资源将在 Chrome 80 中自动升级到 HTTPS。如果资源无法通过 HTTPS 加载，它们将被阻止。然而，混合图像仍然允许加载，但是它们会在 omnibox 中显示“不安全”标签。

在接下来的 Chrome 81 更新中，混合图像也将自动升级到 HTTPS。同样，无法加载到 HTTPS 的图片将被屏蔽。希望将其混合内容迁移到 HTTPS 的开发者可以在下面链接的官方帖子中查看可用资源。

* * *

**来源:[铬博客](https://blog.chromium.org/2019/10/no-more-mixed-messages-about-https.html)**