# XPrivacyLua 是一个保护敏感数据的公开模块

> 原文：<https://www.xda-developers.com/xprivacylua-xposed-module-privacy/>

# XPrivacyLua 是一个保护数据的公开模块

XPrivacyLua 是一个兼容 Android 6.0 Marshmallow 和更新版本的 Xposed 模块，通过向应用程序提供虚假或无意义的数据来保护你的隐私。

如果你曾经错误地下载了一个你不信任其数据的应用程序，你可能会偶然发现 [XPrivacy](https://github.com/M66B/XPrivacy) 。这是一个暴露的模块，通过向应用程序提供虚假数据或根本没有数据，或通过限制应用程序访问联系人和位置等数据类别来保护您的隐私。它不会撤销或阻止应用程序的权限(除了互联网和存储访问)，所以大多数应用程序不会在被拒绝访问时行为不端或崩溃。当应用程序请求权限、连接到互联网或试图访问敏感数据时，它会显示方便的图标。但是 XPrivacy 只兼容 Android 4 . 0 . 3-5 . 1 . 1 版本，而且已经半年没更新了。这就是为什么 XDA 认可的开发者 [M66B](https://forum.xda-developers.com/member.php?u=2799345) 发布了 [XPrivacyLua](https://forum.xda-developers.com/xposed/modules/xprivacylua6-0-android-privacy-manager-t3730663) ，这是 XPrivacy 的精神继承者，用 [Lua](http://www.lua.org/) 编写，兼容 [Android 6.0 棉花糖](https://www.xda-developers.com/android-distribution-numbers-august-nougat/)和更新版本。它目前在 alpha 中，但是已经可以从 [Xposed 模块库](http://repo.xposed.info/module/eu.faircode.xlua)和 [Github](https://github.com/M66B/XPrivacyLua/blob/master/README.md) 中获得。只要你已经安装了 [Xposed 框架](https://forum.xda-developers.com/xposed)，你就可以进行测试了。

M66B 目前专注于修复错误，但表示 XPrivacyLua 的未来版本可能会允许您添加自己的限制和定义。希望如此。

* * *

[**XPrivacyLua 隐私管理器**](https://forum.xda-developers.com/xposed/modules/xprivacylua6-0-android-privacy-manager-t3730663)