# 谷歌文件测试了一个“安全文件夹”,它用一个 4 位数的 PIN 码来保护文件

> 原文：<https://www.xda-developers.com/files-by-google-safe-folder-protect-files-4-digit-pin/>

# 谷歌 1.0.315 的文件测试了一个“安全文件夹”,它用一个 4 位数的 PIN 码隐藏和保护文件

谷歌 1.0.3 版的文件揭示了一个“安全文件夹”的工作，它将隐藏和保护你的私人文件，带有一个 4 位数的 PIN。

谷歌文件是一个文件管理应用程序，已经成为谷歌像素设备在 Android 11 上的默认文件管理器，因为 AOSP 文件应用程序现在只能从存储设置中访问。APK 的最新版本最近开始推出，它也被上传到 [APKMirror](https://www.apkmirror.com/apk/google-inc/files-go/files-go-1-0-315758190-release/) 。版本 1.0.315 揭示了一个新的“安全文件夹”功能的工作，该功能将允许您使用 4 位 PIN 隐藏和加密文件。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些特性目前还没有在实时构建中实现，并且可能会被开发人员在未来的构建中随时引入。

今天早些时候， [*9to5Google*](https://9to5google.com/2020/06/12/files-by-google-safe-folder/) 首次发现了该功能的字符串，但我们已经通过 Google 应用程序在文件中完全启用了该功能。它的工作原理很简单:一个新的“安全文件夹”按钮出现在“浏览”标签的“收藏”部分。当你点击安全文件夹时，你会被要求设置一个 4 位密码。一旦您设置了 PIN，它会警告您，如果您忘记了 PIN，将无法再次打开安全文件夹。设置 PIN 后，您可以移动文件，方法是选择一个或多个文件，然后在菜单中选择“移动到安全文件夹”。

在引擎盖下，文件存储在一个名为。FilesByGoogle 位于外部存储的根目录下(位于/data/media/{user})。由于有了一个[，这个文件夹的内容对其他应用程序是隐藏的。目录中的 nomedia 文件](https://www.xda-developers.com/keep-those-pesky-data-folders-out-of-the-gallery-with-gallery-excluder-for-android/)。文件本身似乎是加密的，所以如果你忘记了你的密码，确实没有办法恢复它们。如果通过 Google app 卸载文件，安全文件夹的内容不会被删除。然而，当你重新安装谷歌文件时，它将无法再次读取旧的安全文件夹内容。您可以使用相同(或不同)的 PIN 设置新的安全文件夹，所有移动到安全文件夹的新文件也将保存在。FilesByGoogle 目录。

在最新版本的谷歌应用程序文件中，用户还不能使用该功能。然而，一旦它推出，我们会让你知道。

*感谢 PNF 软件为我们提供了使用许可 [JEB Decompiler](https://www.pnfsoftware.com/?aid=xdadev) ，这是一款针对 Android 应用的专业级逆向工程工具。*