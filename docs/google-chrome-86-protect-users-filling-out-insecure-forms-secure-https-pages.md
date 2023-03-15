# 当用户在安全页面上填写不安全的表格时，谷歌浏览器会发出警告

> 原文：<https://www.xda-developers.com/google-chrome-86-protect-users-filling-out-insecure-forms-secure-https-pages/>

# 谷歌 Chrome 86 将警告用户在 HTTPS 页面上填写不安全的表格

当用户试图填写在其他安全(HTTPS)页面上提交的不安全表格时，谷歌 Chrome 86 会发出警告。

当谷歌在 10 月份推出 Chrome 86 时，当人们试图在其他安全(HTTPS)页面上填写不安全提交的表格时，网络浏览器会发出警告。据谷歌称，新的警告旨在为用户提供更安全的浏览体验，因为在不安全的表格上提交信息可能会向窃听者泄露私人信息。

谷歌表示，Chrome 86 将引入以下变化:

*   混合表单上的自动填充将被禁用，但 Chrome 的密码管理器将继续工作。这是因为密码管理器旨在帮助用户输入唯一的密码，因此即使在不安全提交的表单上使用也是安全的。允许用户使用密码管理器比让他们重复使用旧密码要好。

*   当用户开始填写混合表单时，他们会看到警告他们该表单不安全的文本。
*   如果用户试图提交一个混合表单，他们将看到一个整页的警告，提醒他们潜在的风险，并确认他们是否仍然要提交表单。

过去，当使用混合表单时，Chrome 会从地址栏中移除锁图标。谷歌表示，这种体验令最终用户感到困惑，因为它没有正确告知用户以不安全的形式提交数据的相关风险，这就是为什么它做出了改变。

今天的声明是谷歌终止在网络上使用 HTTP 内容的最新努力。回到 2018 年 7 月，[谷歌 Chrome 开始将所有 HTTP 网站](https://www.xda-developers.com/google-chrome-68-https-no-secure-july-2018/)标记为“不安全”。该浏览器还阻止[混合下载](https://www.xda-developers.com/google-chrome-block-insecure-downloads-https-pages/)和[其他不安全内容](https://www.xda-developers.com/google-chrome-block-insecure-content-loading-https-pages/)加载到 HTTPS 页面。阻止混合表单是一个合乎逻辑的过程，所以 web 开发人员应该已经看到了这种变化的到来。对于那些想将网站上的表单完全迁移到 HTTPS 的人，谷歌提供了[提示来帮助他们完成迁移](https://developers.google.com/web/fundamentals/security/prevent-mixed-content/fixing-mixed-content)。