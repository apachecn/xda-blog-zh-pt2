# 翻录菜单按钮:Android 10 放弃了对极旧应用的传统支持

> 原文：<https://www.xda-developers.com/rip-menu-button-android-10-drops-legacy-support-extremely-old-apps/>

这个网站上的很多人都是 Android 的长期用户，从 Froyo 和 Gingerbread 的时代就开始了。那时候，智能手机都是带物理按键的(喘气！)用于 UI 导航:即后退按钮、菜单按钮、主页按钮和搜索按钮。实体按钮被电容触摸按钮所取代，搜索按钮也被一些原始设备制造商放弃了——但通过其他三个专用按钮导航 UI 和应用程序的总体想法在当时的 Android 世界中仍然存在。

通过 Android 3.0 Honeycomb，谷歌推动平板电脑制造商采用基于软件的屏幕导航按钮来取代物理按钮，并引入了 [ActionBar](http://developer.android.com/reference/android/app/ActionBar.html) 作为标准解决方案，使用户选项中的操作立即可见并快速调用。“菜单”按钮的想法让[也将](https://android-developers.googleblog.com/2012/01/say-goodbye-to-menu-button.html)演变成了一个“动作溢出”按钮，表示一个检索不适合动作栏的动作的按钮；尽管如此，用户仍然继续称它为菜单按钮。Honeycomb 最近还为平板电脑推出了应用程序按钮，而 Android 4.0 冰淇淋三明治则将这一功能推至智能手机。由后退、主页和最近应用组成的标志性 3 按钮导航栏就这样诞生了，留下了专用菜单和搜索按钮。

 <picture>![Android Market](img/3b4f50ef7277412b4379f39ce542e937.png)</picture> 

Android Market with the Overflow button, along with the 3-button navigation bar

有一个专用的菜单按钮导致应用程序开发人员采用糟糕的设计选择，因为开发人员对屏幕上显示什么动作和菜单中有什么相当粗心。当时，用户会下意识地点击菜单按钮，希望找到更多对他们有用的选项，这是不必要的浪费行为。因此，动作栏的引入带来了更多的设计一致性，因为它建议开发人员将最重要的动作直接放在动作栏上或屏幕上的其他地方，只有那些没有找到位置的动作才会出现在溢出按钮中。

然而，当时许多针对 Android 2.3 和更低版本的应用程序尚未更新以在屏幕上显示菜单，因此没有专用菜单按钮的用户将无法启动菜单。谷歌通过为传统应用程序添加兼容性行为来解决这一问题，允许系统在仅支持 Android 2.3 和更低版本的应用程序上的系统导航按钮旁边显示操作溢出/菜单按钮。

这种遗留支持从 Android 3.0 蜂巢一直延伸到 Android 9 派。但随着 Android 10 的推出，谷歌终于拔掉了插头。针对 Android 2.3 或更早版本的 Android 应用程序现在将不再有菜单按钮显示在 [Android 10](https://www.xda-developers.com/android-10-android-q-brand-redesign/) 上，以及更高版本。在[对强调删除的错误报告](https://issuetracker.google.com/issues/140699628)的回应中，谷歌确认了删除:

> 这是有意删除的，因为该 API 现已在多个版本中被弃用。所以，这是预期的工作。

这个决定将影响到非常非常少的用户，他们一直继续依赖古老和长期被遗弃的应用程序-如果它有效，它就有效，对吗？如果你是那些突然发现你最喜欢的应用程序之一不再能够显示它的菜单的人之一，也许是时候继续前进，寻找更新的替代品了。

* * *

**来源:[谷歌问题跟踪者](https://issuetracker.google.com/issues/140699628)**

**故事 Via:[/r/Android](https://www.reddit.com/r/Android/comments/dvuwpn/remember_the_old_menu_key_of_android_23_now_its/)**