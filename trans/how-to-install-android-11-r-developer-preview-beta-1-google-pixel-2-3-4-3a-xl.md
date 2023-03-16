# 如何在你的谷歌 Pixel 智能手机上安装 Android 11 开发者预览版

> 原文：<https://www.xda-developers.com/how-to-install-android-11-r-developer-preview-beta-1-google-pixel-2-3-4-3a-xl/>

# 如何在你的谷歌 Pixel 智能手机上安装 Android 11 开发者预览版

谷歌刚刚发布了用于 Pixel 智能手机的 Android 11 开发者预览版 1。下面是如何安装在你的 Pixel 和 Pixel XL 上！看看吧！

这是全新的一年，这意味着随着 Android 11 新的开发者预览版和测试版的到来，我们可以继续推进年度 Android 发布周期。尽管谷歌已经选择用 Android 10 抛弃甜点品牌，他们仍然继续在内部用字母顺序引用下一个 Android 更新——在这种情况下是 Android R。Android 11/Android R 的第一个开发者预览版刚刚针对受支持的设备发布，这意味着有经验的开发者现在可以将 Android 软件的前沿加载到他们的测试设备上，并确保他们自己的应用程序为新的 OS 更新将带来的变化做好准备。如果你想在 Pixel 智能手机上安装 Android 11 开发者预览版 1，请继续阅读。

以下说明仅适用于受支持的 Google Pixel 设备，即 [Pixel 2](https://forum.xda-developers.com/pixel-2) 、 [Pixel 2 XL](https://forum.xda-developers.com/pixel-2-xl) 、 [Pixel 3](https://www.xda-developers.com/tag/google-pixel-3/) 、 [Pixel 3 XL](https://www.xda-developers.com/tag/google-pixel-3/) 、Pixel 3a、Pixel 3a XL、Pixel 4 和 Pixel 4 XL。

还要注意，这些更新仅供开发人员使用，不适合日常使用。不言而喻，这些开发者预览版和测试版会包含 bug。我们强烈建议您在继续之前备份所有重要数据，即使这些步骤不会导致数据擦除。

* * *

## 方法 1:通过恢复和 ADB 侧装 Android 11 开发者预览版 1

要安装第一个开发者预览版，您需要通过 ADB 从 Recovery 下载 OTA 包。这种方法适用于带有锁定引导加载程序的设备。这种方法的一个缺点是，您需要一台安装了 ADB 的计算机来安装更新。

1.  下载更新。你电脑上的 zip 文件[从这里](https://www.xda-developers.com/how-to-download-android-11-developer-preview-for-google-pixel-and-other-android-devices/)。为了方便起见，您可以将该文件重命名为一个更简单的名称，并将该文件放在您计算机上 ADB 所在的目录中。
2.  可选但建议:验证您下载的文件的 SHA-256 校验和，以确保该文件已完全正确下载。
3.  在手机上启用 USB 调试-进入设置>关于手机>轻按“内部版本号”10 次以启用开发者选项，然后导航至设置>开发者选项>启用“USB 调试”。
4.  将手机连接到电脑。如果这是您第一次与亚行计算机连接，当手机上出现提示时，请在手机上授权您的计算机连接。
5.  在您的计算机上，运行命令:

    ```
     adb reboot recovery 
    ```

6.  您的手机现在应该处于恢复模式。
7.  在您的手机上，选择“应用亚行更新”选项
8.  在您的计算机上，运行命令:

    ```
     adb devices 
    ```

    这将返回一个设备序列号，其名称旁边带有“sideload ”,表明您的设备以 sideload 模式连接到计算机。
9.  在您的计算机上，运行命令:

    ```
     adb sideload "filename".zip 
    ```

    ，其中“文件名”将替换为在步骤 1 中下载的文件的名称
10.  更新应该会安装在您的手机上。安装完成后，在手机上选择“立即重启系统”，重启进入 Android 11。

* * *

## 方法 2:通过快速启动刷新完整的工厂映像

如果你有一个未锁定的 bootloader，你需要通过 Fastboot 刷新 Android 11 开发者预览版 1 的完整出厂映像。通常，这是通过下载文件中包含的 *flash-all.sh* 或 *flash-all.bat* 脚本文件来完成的，但这也会完全擦除设备。但是，您可以通过从脚本的命令中删除“-w”wipe 属性来保留您的数据。

1.  下载工厂图像。你电脑上的 zip 文件[从这里](https://www.xda-developers.com/how-to-download-android-11-developer-preview-for-google-pixel-and-other-android-devices/)。
2.  可选但建议:验证您下载的文件的 SHA-256 校验和，以确保该文件已完全正确下载。
3.  提取。zip 文件，为了方便起见，将结果文件复制并粘贴到您计算机上的 ADB 和 fastboot 文件夹中。
4.  可选:结果文件将包含一个 *flash-all.sh* 或 *flash-all.bat* 脚本文件。使用文本编辑器，打开 *flash-all.sh* (如果你在 macOS/Linux 上)或 *flash-all.bat* 脚本文件(如果你在 Windows 上)。找到并移除/删除快速启动更新命令中的-w 标志。这将跳过你的手机数据擦除。为了避免兼容性问题，建议进行数据擦除。
5.  在手机上启用 USB 调试-进入设置>关于手机>轻按“内部版本号”10 次以启用开发者选项，然后导航至设置>开发者选项>启用“USB 调试”。
6.  将手机连接到电脑。如果这是您第一次与亚行计算机连接，当手机上出现提示时，请在手机上授权您的计算机连接。
7.  在你的电脑上，运行:

    ```
     adb reboot bootloader 
    ```

    这将重新启动你的手机进入快速启动模式。
8.  在你的 macOS/Linux PC 上，运行:

    ```
     flash-all 
    ```

    这个命令执行 *flash-all.sh* 脚本文件，然后安装必要的引导程序、基带固件和操作系统。如果您使用的是 Windows，只需双击 flash-all.bat 文件。
9.  一旦脚本完成，您的设备将重新启动到新的操作系统。

* * *

如果你想了解 Android 11[的所有新功能，请跟随我们的报道](https://www.xda-developers.com/tag/android-11/)！