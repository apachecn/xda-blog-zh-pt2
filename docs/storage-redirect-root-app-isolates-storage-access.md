# 存储重定向是一个根应用程序，用于隔离对不良应用程序的存储访问

> 原文：<https://www.xda-developers.com/storage-redirect-root-app-isolates-storage-access/>

# 存储重定向是一个根应用程序，用于隔离不良 Android 应用程序的存储访问

存储重定向是一个应用程序，其工作原理与作用域存储相同，并允许您管理应用程序如何使用您的存储。

如果你曾经浏览过你手机的文件目录，你可能会注意到一大堆基本上没有任何价值的休眠文件夹和文件。许多应用程序没有遵循最佳实践，并在您从手机中卸载它们后留下了大量文件。为了让用户更多地控制他们的存储并限制应用程序混乱，谷歌[在](https://www.xda-developers.com/google-gives-developers-more-time-android-q-scoped-storage/) [Android 10](https://www.xda-developers.com/how-to-enable-android-10-rules-feature-any-pixel-smartphone/) 中引入了范围存储访问，限制应用程序如何访问外部存储。虽然实现[范围存储](https://developer.android.com/training/data-storage)对于针对 Android 10 的应用程序来说不是强制性的，但谷歌将在下一个主要版本:Android 11 中全面实现这一新变化。

但是你不必等待 Android 11 来控制你的设备存储。*存储重定向*是一个应用程序，其工作原理与作用域存储相同，并让您管理应用程序如何使用您的存储。借助存储重定向，您可以选择要隔离的应用程序以及要授予共享存储完全访问权限的应用程序。一旦应用程序被隔离，它只能从自己的目录中访问文件，应用程序生成的文件也将保留在隔离存储中。

### 以下是您可以通过存储重定向实现的功能:

*   你可以控制应用程序可以使用哪些私人文件(按文件夹)
*   应用程序创建的文件将保留在独立存储中
*   卸载 app 后会自动删除独立存储
*   您可以创建自己的规则来决定将哪些重要文件从独立存储“同步”到共享存储空间

存储重定向需要 [root 访问权限](https://www.xda-developers.com/root/)才能发挥其魔力，所以在尝试之前，请确保您满足这一要求。