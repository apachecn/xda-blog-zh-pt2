# 如何解锁引导加载程序和 Root 一加 6T

> 原文：<https://www.xda-developers.com/oneplus-6t-unlock-bootloader-root/>

开发社区总是很好地支持一加设备。随着一加 6T 内核资源在发布日可用[，再加上该公司之前在我们的论坛](https://www.xda-developers.com/oneplus-6t-kernel-source-code/)上向开发者提供 OnePlus 6 设备[，解锁和 root 一加智能手机通常是一个简单的过程。一加 6T 也没什么不同(](https://www.xda-developers.com/oneplus-6-developer-application/)[，除非你用的是 T-Mobile 版](https://www.xda-developers.com/oneplus-6t-t-mobile-model-details/))，所以你可以很容易地解锁它的引导程序，并找到它。如果您感兴趣，我们已经为您详细介绍了整个过程，请注意，该过程将删除您的手机！我们将使用 TWRP 进行自定义恢复，使用 Magisk 管理 root 访问。

## 如何解锁引导加载程序和 Root 一加 6T

### 步骤 1 -启用 OEM 解锁

您需要启用 OEM 解锁，这可以通过在您的设备上启用开发者设置来完成。为此，转到**设置**、**关于手机**并反复点击**内部版本号**。开发者选项将被添加到您的系统设置中，然后您可以启用 OEM 解锁。

### 第二步-解锁你的手机

设置 adb，重新启动引导程序并运行以下命令。是的，真的就这么简单！

```
 fastboot oem unlock 
```

您可以通过打开 USB 调试，设置 adb 和 fastboot 并键入“adb reboot bootloader”来重新启动 bootloader。或者，您可以按住音量键和电源键来启动您的设备。USB 调试也位于开发人员选项下。

### 第 3 步-启动 TWRP 和闪存和 Magisk

因为一加 6T 使用 A/B 分区系统，所以刷新自定义恢复比在纯 A 设备上稍微复杂一些。[你可以在这里阅读更多关于 A/B 设备的信息](https://www.xda-developers.com/how-a-b-partitions-and-seamless-updates-affect-custom-development-on-xda/)。你需要下载最新版本的 blu _ spark TWRP oxygen OS rom，你可以在下面下载。您需要下载 zip 文件和 img 文件。我们需要这个 zip 文件，因为我们稍后会刷新它。

[**blu_spark TWRP 为一加 6T**](https://forum.xda-developers.com/devdb/project/?id=27466#downloads)

[**下载魔法**](https://github.com/topjohnwu/Magisk/releases)

当您的设备处于引导加载程序中时，键入以下内容，以与我们之前相同的方式访问它。

```
 fastboot boot twrp-3.2.3-x_blu_spark_v9.86_op6.img 
```

一旦启动，进入**高级**、 **ADB 侧载**并输入以下内容。

```
 adb sideload twrp-3.2.3-x_blu_spark_v9.86_op6.zip 
```

现在，重新启动以恢复(从 TWRP 内部)。现在以完全相同的方式刷新 Magisk zip 文件。

```
 adb sideload Magisk-v17.3.zip 
```

重新启动你的设备系统，你就完成了！

对于那些在几周或几个月后阅读本教程的人来说，请注意可能会有更新版本的 TWRP 图像。如果是这种情况，只需更改“fastboot boot”命令，使其包含您下载的较新映像的名称。

* * *

## 对于那些通过 T-Mobile 购买一加 6T 的用户

如果你的一加 6T 是通过 T-Mobile 购买的，那么你只能在全部付清并在 T-Mobile 的网络上使用 40 天后*才能解锁你的设备。之后，你可以通过[一加的在线表单](https://onepluscom.pxf.io/c/2233363/916678/12532?subId1=UUxdaUeUpU22751&subId2=exda&u=https%3A%2F%2Fwww.oneplus.com%2Faccount%2Fsign-in%3Freturn_to%3Dhttps%253A%252F%252Funlockbootloader.oneplus.com%252Funlock_token)解锁引导程序。接下来，按照以下步骤解锁您的引导加载程序。*

### 步骤 1 -启用 OEM 解锁

您需要启用 OEM 解锁，这可以通过在您的设备上启用开发者设置来完成。为此，转到**设置**、**关于手机**并反复点击**内部版本号**。开发者选项将被添加到您的系统设置中，然后您可以启用 OEM 解锁。

### 第二步-获取您的 IMEI

通过在电话拨号器中拨打*#06#来获取电话的 IMEI。IMEI 码会显示出来。稍后 T-Mobile 的表格需要用到这个。

### 第 3 步-获取您的解锁代码

在您的设备上重新启动进入快速启动模式。您可以通过打开 USB 调试，设置 adb 和 fastboot 并键入“adb reboot bootloader”来重新启动 bootloader。USB 调试也位于开发人员选项下。或者，您可以按住音量键和电源键来启动您的设备。接下来键入“fastboot oem get_unlock_code”。记下这段代码，因为 T-Mobile 的在线表单也需要它。

### 步骤 4 -填写在线表格并出示您的令牌

这是你需要输入 IMEI 码和解锁码的地方。一旦你提交，你应该会在两周内收到一个闪存解锁令牌。可以用“fastboot flash cust-unlock <unlock_token.bin>”来闪存</unlock_token.bin>

### 第 5 步-解锁和根

现在你可以像普通的一加 6Ts 一样解锁你的手机了！只需输入“快速启动 oem 解锁”,您就可以开始了！现在你可以按照一个普通的，解锁的一加 6T 的步骤来根你的设备。这些在上面有详细说明。

* * *

想知道你应该做什么后解锁引导加载程序和根一加 6T？加入我们的论坛，获取所有可用的 mod、自定义内核和自定义 rom！

 **[**加入一加 6T 论坛！**](https://forum.xda-developers.com/oneplus-6t)**