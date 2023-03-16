# 私人剪贴板有助于在旧的 Android 设备上模仿 Android 10 的剪贴板隐私

> 原文：<https://www.xda-developers.com/private-clipboard-mimic-android-10-privacy/>

# 私人剪贴板有助于在旧的 Android 设备上模仿 Android 10 的剪贴板隐私

XDA 资深会员 easyjoin 开发的私人剪贴板应用程序可以让你在 Android 6.0 及以上版本上模仿 Android 10 的剪贴板隐私功能。

Android 10 上一个被低估的功能是内置的对剪贴板访问的限制。在 Android 10 之前的 Android 版本中，[每个应用程序都可以读取你的剪贴板内容](https://www.xda-developers.com/stop-apps-reading-android-clipboard/)。这是在不需要向任何应用授予任何运行时权限的情况下完成的。普通用户最终会一直复制用户名、密码和地址等敏感信息，因此应用程序在后台不断抓取这些数据是相当微不足道的。[米莎尔在 2019 年 1 月发现](https://www.xda-developers.com/android-q-block-background-clipboard-external-storage-permissions-downgrading-apps/)Android Q/Android 10 将最终阻止背景剪辑阅读。但如果你使用的是旧版本的 Android，你可以用这个私人剪贴板应用模仿同样的功能。

[私人剪贴板](https://forum.xda-developers.com/android/apps-games/app-private-clipboard-t3964055)XDA 资深会员 [easyjoin](https://forum.xda-developers.com/member.php?u=8401881) 模仿 Android 10 的剪贴板隐私功能。虽然 Android 10 带来了一个新的权限“`READ_CLIPBOARD_IN_BACKGROUND`”，将后台剪贴板访问限制为仅 OEM 应用程序，但私有剪贴板采用了一种迂回的方法，即创建一个私有剪贴板。用户需要有意识地避免 Android 内默认的复制选项，转而寻找文本选择后的三点菜单。然后，选择“复制到私人剪贴板”选项。类似地，要粘贴文本，选择三点菜单并单击“从私有剪贴板粘贴”,而不是默认的粘贴选项。这个应用不需要任何权限就可以运行，但是需要 Android 6 棉花糖以上版本。

**[私人剪贴板 App - XDA 线程](https://forum.xda-developers.com/android/apps-games/app-private-clipboard-t3964055)**

显然，如果你在 Android 10 上，你已经有了剪贴板隐私。Android 应用程序具有剪贴板读取权限，以便首先从剪贴板接受文本，因为没有基本权限，用户根本无法粘贴任何已复制的文本。幸运的是，将这限制在前台的应用程序上，就堵住了一个相当大的疏忽。但是附带的损害是，因为这个改变，我们失去了剪贴板管理器的功能。