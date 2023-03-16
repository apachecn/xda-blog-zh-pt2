# Chrome OS 现在在文件应用中显示 Android 文件

> 原文：<https://www.xda-developers.com/chrome-os-android-files-app/>

**2018 年 5 月 30 日更新**:提交已被合并，并已在 Canary 上线。截图见下图。

继一系列 Android 相关的 Chromium Gerrit for Chrome OS 之后，[我们发现了另一个](https://chromium-review.googlesource.com/c/chromium/src/+/1067378)，这可能是迄今为止最好的补充。我们已经看到了对[父母控制](https://www.xda-developers.com/chrome-os-managing-android-apps-child-accounts/)和[的改进，增加了安卓应用快捷搜索](https://www.xda-developers.com/chrome-os-android-app-shortcuts-search/)。现在我们得到了一个备受期待的功能——支持 Android 应用程序的 Chromebooks 可能很快就能在原生 Chrome OS 文件应用程序中看到设备上的所有 Android 文件。

支持 Android 应用程序的 Chromebooks 目前有一个主要限制:你看不到 Android 的/data/media 中的文件，这是 Android 应用程序存储文件供用户访问的存储位置。嗯，这并不完全正确，因为你可以访问 Android 下载文件夹，但仅此而已。如果你想访问 Android 应用程序存储在另一个目录中的文件，你要么必须将其移动到云存储位置，要么将其移动到 Android 下载文件夹。这种情况将会改变。

 <picture>![Chrome OS](img/a2ccc79c36b30be68029162b1f1bd753.png)</picture> 

The commit message.

现在，在 Chrome 操作系统上访问你的 Android 文件将变得更加容易，因为你将能够看到你的 Android 外部存储的全部内容。这很有用，原因有很多，包括应用程序可能会将文件下载到自己的文件夹，而不是下载文件夹。

 <picture>![](img/68bd29a1b5718e9874854aa58433d566.png)</picture> 

The flag description.

这是一个实验性的功能，需要通过一个名为`chrome://flags#show-android-files-in-files-app`的标志来启用。“Android 文件”选项将在 Chrome OS 文件应用程序的左窗格中可见。

对于那些想在它可用时就尝试一下的人来说，您必须等待提交被合并，然后切换到 Canary 构建。Canary 构建每隔几天发布一次，但是通常非常不稳定，不建议日常使用。不过，你不仅可以从任何地方复制你的 Android 文件，还可以获得我们最近几周发现的所有其他 Android 相关功能。这还不包括谷歌可能已经打包的任何额外改进。如果您切换到 Canary build，请确保事先备份您的所有文件，您应该可以开始了！

* * *

## 更新:Android 文件部分已上线

正如/u/ [在/r/ChromeOS](https://www.reddit.com/r/chromeos/comments/8mrtai/android_files_section_in_the_file_manager/) 上指出的，ChromeOS 金丝雀上的谷歌 Pixelbook 现在可以在文件应用中访问 Android 文件，只要你启用`chrome://flags#show-android-files-in-files-app`。