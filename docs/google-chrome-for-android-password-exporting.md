# 谷歌 Android 版 Chrome 将很快支持密码导出

> 原文：<https://www.xda-developers.com/google-chrome-for-android-password-exporting/>

# 【更新:生活在 Chrome 金丝雀】谷歌 Android 版 Chrome 将很快支持密码导出

一份承诺显示，谷歌 Android 版 Chrome 将支持密码导出。一个新的“导出密码”选项将出现在应用程序的设置菜单中。

2018 年 2 月 1 日:密码导出功能在最新的 Chrome Canary 和 Chromium nightly 版本中上线。你可以通过打开 [chrome://flags](chrome://flags) 中的密码导入和密码导出标志来启用它。

这有点难以置信，但自从谷歌发布用于 Android 的 [Chrome 以来，已经过去了将近五年。自此，谷歌热门网页浏览器的移动端口取代了大多数安卓手机上的存量](https://play.google.com/store/apps/details?id=com.android.chrome&hl=en)[安卓开源项目](http://xda-developers.com/tag/aosp) (AOSP)浏览器，获得了无数次更新，成为安卓上下载量最大的浏览器之一。现在，它获得了一个新功能:密码导出。

上个月，我们报道了谷歌 Chrome 浏览器的[选项，可以查看保存的密码](https://www.xda-developers.com/google-chrome-android-saved-passwords/)，让你不必登录你的谷歌账户或访问[谷歌密码](http://passwords.google.com)网站就可以查看你的密码。谷歌 Git 中的一个新的[提交显示，谷歌计划用一个内置的密码导出工具来扩展该功能。](https://bugs.chromium.org/p/chromium/issues/detail?id=788701#c1)

以下是提交的描述:

> #### 【安卓设置】增加导出密码的菜单项
> 
> #### 这个 CL 在默认关闭功能后面增加了一个菜单项，用于从 Chrome 的设置中导出密码。菜单项当前不执行任何操作。

当该功能上线时，你会在 Chrome 设置菜单的密码页面右上角看到一个**导出密码**选项。点击它将启动导出过程，这将提示您输入锁屏密码，并将您保存的密码的 CSV 文件下载到您的智能手机。(遗憾的是，提交并没有指定文件的格式，但它可能不是专有的。)

Chrome 的密码输出器将是一个强大的网络浏览器的受欢迎的补充。随着来自第三方网络浏览器的竞争日益激烈，如三星互联网、T2、火狐量子和 T4 微软边缘，谷歌明智的做法是不断增加功能，吸引用户加入其生态系统。谷歌 Git 承诺表明这个搜索巨头正在这么做。

* * *

[**来源:谷歌 Git**](https://bugs.chromium.org/p/chromium/issues/detail?id=788701#c1)