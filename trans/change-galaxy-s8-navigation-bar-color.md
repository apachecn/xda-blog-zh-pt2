# 更改 Galaxy S8、S8+或 Note 8 导航条颜色，不带 Root

> 原文：<https://www.xda-developers.com/change-galaxy-s8-navigation-bar-color/>

三星 Galaxy S8、Galaxy S8+和 Galaxy Note 8 是三星第一批放弃传统电容按钮、支持软件导航键的旗舰智能手机。除了允许我们定制按键的布局，我们还可以改变导航条的颜色。在我们必须选择的标准颜色中，三星还包括一个色轮选项，这样他们就可以选择他们想要的任何颜色。然而，该公司在 6 月的 OTA 更新中删除了这一色轮选项，但由于 ADB 命令，我们仍然可以手动更改 Galaxy S8、Galaxy S8+或 Galaxy Note 8 导航栏的颜色。

例如，如果你想设置一个持续的黑色导航栏颜色，现在你可以！以下指南将带您了解如何通过电脑使用 ADB 命令改变颜色。

* * *

## 教程-更改 Galaxy S8、S8+或 Note 8 导航栏颜色

1.  遵循本教程在您的 Windows、Mac 或 Linux 电脑上设置 ADB。
2.  打开命令提示符或终端窗口，在命令提示符或终端窗口中执行以下命令:`adb shell`
3.  现在我们在三星 Galaxy S8、Galaxy S8+或 Galaxy Note 8 的 ADB shell 环境中。接下来，我们需要获取我们想要设置的导航栏颜色的颜色代码。
4.  你[可以在这里](https://codepen.io/anon/pen/mwQjEZ)进入这个网站，并使用页面底部显示的颜色选择器。
5.  选择一种颜色后，复制框中显示的整个 Android 数值(包括减号，如果有的话)
6.  将注意力转回到命令提示符或终端窗口，执行以下两个命令:

    ```
     settings put global navigationbar_color <insert Android color value>
    settings put global navigationbar_current_color <insert Android color value> 
    ```

7.  然后重启你的三星 Galaxy S8/S8+/Note 8。
8.  在没有将导航栏更改为特定颜色的应用程序中，您应该会看到新的颜色。

* * *

### 说明

由于三星还没有出来给我们一个他们为什么从三星 Galaxy S8/S8+/Note 8 导航栏颜色选项中删除色轮的原因，我们不太确定该公司为什么要这样做。有可能三星只是不想让人们使用奇怪的颜色，因为这会与操作系统的其他部分冲突。此外，三星实现这一功能的方式可能存在一些问题，导致该平台的其他部分出现一些问题。

无论哪种方式，该功能仍然存在于三星的 OEM 皮肤下，谢天谢地，我们能够通过一些简单的 ADB 命令来访问它。XDA 成员 [haksancan](https://forum.xda-developers.com/member.php?u=5318157) 首先在我们的银河 S8 论坛指出了这一点[，并做了大量工作解释这一功能隐藏在哪里，甚至如何计算特定的颜色。幸运的是，看起来这个功能在](https://forum.xda-developers.com/galaxy-s8/themes/change-navigation-bar-colors-t3622626)[新发布的 Galaxy Note 8](https://www.xda-developers.com/galaxy-note-8-835-rear-cameras-spen/) 上仍然有效。

我们在这里使用的值格式是一个转换成带符号十进制的 RGB 十六进制颜色代码。有很多方法可以手动计算颜色值，但是我们将只使用上面指南的步骤 15 中链接的色轮。

当从设置菜单中手动选择颜色时，这些值会被改变，但我们只是用 ADB shell 命令将它们注入到软件中。如果您想恢复传统颜色，只需进入设置->显示->导航栏，然后选择三星提供的标准颜色之一。请记住，我们只是用这些命令手动注入一个颜色代码，因此您可以通过在此选择不同的颜色来轻松恢复这一更改。

不过这种方法有一些注意事项，它们也适用于三星的解决方案。例如，一些应用程序自己手动改变导航栏的颜色。这不能用这种方法覆盖，因此这些应用程序将自己控制 Galaxy S8、S8+或 Note 8 导航条的颜色。除了少数应用程序(如图库或概览页面)，完全透明的导航栏是不可能的。

这是因为应用程序通常不在导航栏下绘制。所以将它设置为透明只会显示一个空白，因为应用程序不会在它下面绘制自己。最后，在大多数应用中，将其设置为完全透明的真黑会显示为不透明的白色。这里的解决方法是使用几乎是黑色的颜色，而不是真正的黑色。