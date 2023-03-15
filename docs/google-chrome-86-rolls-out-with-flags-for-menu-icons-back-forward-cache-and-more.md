# 谷歌 Chrome 86 推出了菜单图标和更多的标志

> 原文：<https://www.xda-developers.com/google-chrome-86-rolls-out-with-flags-for-menu-icons-back-forward-cache-and-more/>

谷歌本周开始向用户推出 Chrome 86，这是它首次出现在测试版频道近一个月之后。这个更新应该可以在除 Chrome OS 之外的所有平台上使用，Chrome OS 将于下周发布。以下是 Chrome 86 的一些新功能。

## 安全改进

如果你在 Android 和 iOS 上的 Chrome 中保存的密码被泄露，浏览器会[通知你，并提示你更改密码](https://www.xda-developers.com/google-chrome-ios-android-check-newly-saved-passwords-compromised/)。有了支持”。众所周知的/更改密码”标准，网站将能够指定用户可以更改其密码的 URL。

有了这个标准，用户可以快速方便地找到他们需要更改密码的页面。通过使密码更改更加方便，用户将有希望更改他们的密码，而不是对整个过程感到气馁。

Chrome 86 还会在用户[遇到不安全的表单或下载](https://www.xda-developers.com/google-chrome-86-protect-users-filling-out-insecure-forms-secure-https-pages/)时发出警告。不安全的表单可能位于加密的 HTTPS 页面上，但通过非加密的 HTTP 操作提交数据。

谷歌希望改善用户导航大菜单的方式，因此该公司正在努力在 Chrome 86 中添加菜单图标。按照 [*安卓警察*](https://www.androidpolice.com/2020/10/07/chrome-86/) 的说法，这些功能必须通过标志启用，有两个要测试出来。有[#选项卡式应用溢出菜单图标](//flags/#tabbed-app-overflow-menu-icons)和[#选项卡式应用溢出菜单重组](//flags/#tabbed-app-overflow-menu-icons)；第一个在 Chrome 的溢出菜单中的每个条目旁边添加图标，而第二个将菜单重新组织成几个部分。

## 本地文件系统

当谷歌推出 Chrome 78 时，它开始[测试一个原生文件系统 API](https://www.xda-developers.com/google-announces-chrome-developer-tools-reduce-page-loads-native-app-experiences/) ，它允许网页直接访问你电脑的文件系统。该功能现在随着 Chrome 86 广泛推出，使得挑选文件上传到网站变得更加容易。

出于安全考虑，网站只能看到您选择的文件，并且只有在被授予权限后才能将更改保存回这些文件。一旦网站拥有文件权限，您还会在地址栏中看到一个指示器，并且文件权限仅在网站打开时有效。

## 面向 Android 的增强型安全浏览

Chrome 86 还为 Android 引入了增强的安全浏览功能——这是之前为桌面版 Chrome 引入的功能。该功能旨在通过主动检查网站和下载是否危险来保护用户免受恶意软件和网络钓鱼的侵害。据谷歌称，增强的安全浏览功能启用后，用户在钓鱼网站上输入密码的次数下降了 20%。

## 更多

Chrome 86 中有更多面向开发者的技术变化，包括 FTP 弃用和 WebHID APU 作为原始试用版。后者将允许基于网络的游戏充分利用游戏手柄。

Chrome 86 还增加了后退前进缓存的标志，后退前进时可以[加快网页加载时间](https://www.xda-developers.com/back-forward-google-chrome-faster-bfcache/)。该功能在 Android 中作为一个标志提供(#back-forward-cache)。