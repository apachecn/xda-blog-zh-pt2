# 如何在三星 Galaxy 设备上自定义快速设置按钮布局的大小

> 原文：<https://www.xda-developers.com/customize-size-quick-settings-button-layout-samsung-galaxy/>

谷歌在 Android Lollipop 的通知栏中引入了可操作的快速设置切换，但三星设备早就有这个功能了。在基于 Android 7.0 牛轧糖的三星软件的最新版本(现在称为三星体验，尽管我们大多数人仍然认为它是 Touchwiz)中，用户可以自定义快速设置磁贴的按钮布局。

默认情况下，您可以在 3x3、4x3 或 5x3 快速设置单幅图块布局之间切换。如果你像我一样，依赖大量的磁贴来快速访问你最喜欢的应用和快捷方式，那么你可能会发现这些布局没有为你显示足够多的快速设置磁贴。如果是这样的话，那么这里有一个快速的提示来使用几个简单的 ADB 命令将按钮布局修改成你想要的大小。

* * *

## 修改三星 Galaxy 设备上的快速设置布局尺寸

如前所述，我们将使用 ADB 命令来修改快速设置按钮布局的大小。如果您已经安装了 ADB，请跳过下一部分。如果没有，那么这里有一个快速指南。

### 建立亚洲开发银行

首先，[直接从 Google](https://www.xda-developers.com/google-releases-separate-adb-and-fastboot-binary-downloads/) 为您的特定操作系统下载 ADB 二进制文件，并将其解压缩到您计算机上的一个单独目录中。接下来，[为你的手机安装合适的驱动](https://developer.android.com/studio/run/oem-usb.html)。然后，在设置- >开发者选项中启用“USB 调试”。如果你看不到开发者选项，那么你需要进入设置- >关于手机，然后点击 7 次内部版本号来启用它。最后，通过在与 ADB 二进制文件相同的目录中启动命令提示符(右键单击->“open command prompt here”)并运行以下命令，确保 ADB 正在工作:

```
 adb devices 
```

如果你看到你的设备的序列号(它没有说未经授权)，你是黄金。如果你在手机上看到一个弹出窗口，要求你授予你的计算机 ADB 访问权限，那么就说是。如果你看不到这两种情况，那么试着重启你的电脑/手机，并重新连接到你的电脑上。否则，请尝试重新安装驱动程序。

### 发送 ADB 命令

一旦您确认 ADB 正在您的设备上运行，就该修改设置了。我们可以修改三个设置，每个设置都取整数值。要修改的三个值如下:

*   `qs_tile_column` -速凝瓷砖列数
*   `qs_tile_column_landscape` -风景模式下快速设置磁贴列数
*   `qs_tile_row` -快速设置磁贴行数(仅影响纵向模式)

例如，如果我想要纵向模式下的 6 列 4 行按钮布局，我必须在命令提示符下输入以下命令:

```
 adb shell settings put secure qs_tile_column 6

adb shell settings put secure qs_tile_row 4 
```

一旦输入这些命令，布局应该立即改变以反映您的输入。如果我想要一个 2 列 2 行的布局，我可以输入以下命令:

```
 adb shell settings put secure qs_tile_column 2

adb shell settings put secure qs_tile_row 2 
```

您可以摆弄这些数字，直到找到您喜欢的布局。但是，在使用这些值之前，有两个注意事项需要注意。

1.  横向模式中的行数总是固定为 2。
2.  如果为列和行都输入 0，SystemUI 将开始崩溃。要阻止它崩溃，只需为任一设置输入任何大于 1 的值。

试试这些 ADB 命令，让我知道你喜欢什么样的按钮布局！