# 在运行 OxygenOS 的 OnePlus 6/5T/5/3T/3 上启用持续 OTG

> 原文：<https://www.xda-developers.com/enable-always-on-otg-oxygenos/>

OTG 对许多人来说是一个非常有用的功能，因为它可以让你通过设备的 micro USB 或 USB-C 端口传输数据。你可以连接硬盘，用控制器玩游戏，或者听音乐。一些设备制造商明确允许这样做，一加就是其中之一。OxygenOS 功能的一个主要问题是，如果十分钟不使用，它会自动关闭，用户需要在任何时候使用它时重新启用它。感谢 XDA 资深会员 [Fif_](https://forum.xda-developers.com/member.php?u=5297163) ，有一个简单的方法来避免这一点，它**甚至不需要根**。你所需要的只是亚行，你可以在你的电脑上学习如何设置[这里](https://www.xda-developers.com/install-adb-windows-macos-linux/)。如果您希望在自己的设备上使用 Termux 之类的应用程序，也可以使用 root。

[appbox googleplay com.termux]

## 如何在 OxygenOS 中启用不间断 OTG

### 步骤 1 -在设置中启用 OTG

首先，你需要在你的设备上启用 OTG。打开**设置** - > **高级**并启用 **OTG 存储**即可

### 步骤 2 -永久启用 OTG

接下来，您需要运行 adb 命令。如果您在设备上的终端模拟器中运行此命令，请删除“adb shell”前缀。

```
 adb shell settings put global oneplus_otg_auto_disable 0 
```

您可以使用以下命令验证设置是否已更改。

```
 adb shell settings get global oneplus_otg_auto_disable 
```

现在你完了！请记住，每次禁用并重新启用 OTG 时，您都需要再次运行此命令。因此，如果可能的话，我们建议在根终端内部进行。这将使你不必每次都将手机重新连接到电脑上。您不再需要返回并确保它已在您的设备上启用。所有的命令只是改变一个系统标志来阻止你的手机自动关闭 OTG。这一点已在 OnePlus 3、OnePlus 3T、OnePlus 5、OnePlus 5T 和 OnePlus 6 上得到证实。它应该也适用于为这些设备发布的每个 OxygenOS 版本。