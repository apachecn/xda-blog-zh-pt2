# 如何解锁 bootloader 并 root 一加 7 Pro

> 原文：<https://www.xda-developers.com/unlock-bootloader-root-oneplus-7-pro/>

一加设备是开发市场上最好的设备之一。一加 7 Pro 内核源代码在发布时直接发布，开发者可以马上开始使用。更不用说该公司仍然为开发者提供设备，这意味着你可以从我们的论坛上为几乎任何一加智能手机获得许多不同的定制 rom 和内核。一加 7 Pro 与过去的设备没有什么不同(除非你是在 T-Mobile 上购买的)，你可以很容易地解锁引导加载程序，并用 Magisk 根它。下面的过程将擦你的手机，所以要小心。

在尝试本教程之前，请确保您使用的是最新版本的 OxygenOS。否则，你将无法进入 TWRP。

[**一加 7 大职业论坛**](https://forum.xda-developers.com/oneplus-7-pro)

## 如何解锁 Bootloader 并 Root 一加 7 Pro

### 步骤 1–启用 OEM 解锁

您需要启用 OEM 解锁，这可以通过在您的设备上启用开发者设置来完成。为此，进入**设置>** **关于手机**并反复点击**构建号**。开发者选项将被添加到您的系统设置中，然后您可以启用 OEM 解锁。

### 第二步-解锁你的手机

设置 [adb](https://www.xda-developers.com/install-adb-windows-macos-linux/) ，重新启动您的引导程序，并运行以下命令。是的，真的就这么简单！

```
 <a href="https://www.xda-developers.com/google-releases-separate-adb-and-fastboot-binary-downloads/"><span >fastboot</span></a><span > oem unlock</span> 
```

您可以通过打开 USB 调试，设置 adb 和 fastboot 并键入“adb reboot bootloader”来重新启动 bootloader。或者，您可以按住音量键和电源键来启动您的设备。USB 调试也位于开发人员选项下。

### 第三步——启动 TWRP

接下来，你需要闪现 TWRP。您需要获得可启动映像文件和相应的安装程序 zip 文件。你可以在下面找到两者。

[**下载 TWRP**](https://dl.twrp.me/guacamole/)

一旦你有了这些，启动到快速启动并运行以下命令。

`[fastboot](https://www.xda-developers.com/google-releases-separate-adb-and-fastboot-binary-downloads/) boot twrp_file_name.img`

你现在将被引导到 TWRP，在那里你应该闪存 TWRP 安装压缩文件。现在启动 OxygenOS。

### Step 4 - Flash Magisk

一旦你启动到 OxygenOS，重新启动恢复并刷新 Magisk。

[**下载魔法**](https://forum.xda-developers.com/apps/magisk/official-magisk-v7-universal-systemless-t3473445)

### 步骤 5 -安装在线旅行社

安装 OTA 将需要您再次经历整个过程。幸运的是，Magisk 有一个针对一加 7 Pro 等 A/B 设备的功能，让你在 OTA 后将 Magisk 刷新到另一个插槽，这样你就不会失去 root 访问权限。如果你想了解更多关于 A/B 分区的信息，[你可以点击](https://www.xda-developers.com/how-a-b-partitions-and-seamless-updates-affect-custom-development-on-xda/)。你需要做的就是像往常一样安装 OTA**(不要重启)，**然后打开 Magisk 管理器，点击安装，点击“安装到非活动插槽”。

然而，你现在已经失去了 TWRP，因为你安装了在线旅行社。为了解决这个问题，你可以像一个 Magisk 模块一样刷新常规的 TWRP 安装程序的 zip 文件。暂时不要重启。因为我们刷新了 TWRP，如果重启，您将失去 root 访问权限。返回 Magisk 主页，选择安装，然后选择直接安装和安装到非活动插槽。

* * *

## 对于那些通过 T-Mobile 购买一加 7 Pro 的用户

如果你的一加 7 Pro 是通过 T-Mobile 购买的，那么你只能在全部付清并在 T-Mobile 的网络上使用四十天后*才能解锁你的设备。之后，你可以通过[一加的在线表单](https://onepluscom.pxf.io/c/2233363/916678/12532?subId1=UUxdaUeUpU24961&subId2=exda&u=https%3A%2F%2Fwww.oneplus.com%2Faccount%2Fsign-in%3Freturn_to%3Dhttps%253A%252F%252Funlockbootloader.oneplus.com%252Funlock_token)解锁引导程序。接下来，按照以下步骤解锁您的引导加载程序。*

### 步骤 1 -启用 OEM 解锁

您需要启用 OEM 解锁，这可以通过在您的设备上启用开发者设置来完成。为此，转到**设置**、**关于手机**并反复点击**内部版本号**。开发者选项将被添加到您的系统设置中，然后您可以启用 OEM 解锁。

### 第二步-获取您的 IMEI

通过在电话拨号器中拨打*#06#来获取电话的 IMEI。IMEI 码会显示出来。稍后您将需要这个来填写 T-Mobile 的表格。

### 第 3 步-获取您的解锁代码

在您的设备上重新启动进入快速启动模式。您可以通过打开 USB 调试，设置 adb 和 fastboot 并键入“adb reboot bootloader”来重新启动 bootloader。USB 调试也位于开发人员选项下。或者，您可以按住音量键和电源键来启动您的设备。接下来键入“fastboot oem get_unlock_code”。记下这段代码，因为 T-Mobile 的在线表单也需要它。

### 步骤 4 -填写在线表格并出示您的令牌

这是你需要输入 IMEI 码和解锁码的地方。一旦你提交，你应该会在两周内收到一个闪存解锁令牌。可以用“fastboot flash cust-unlock”来闪存。

### 第 5 步-解锁和根

现在你可以像普通的一加 7 专业版一样解锁手机了！只需输入“快速启动 oem 解锁”,您就可以开始了！现在你可以按照一个普通的，解锁的一加 7 专业版的步骤来根你的设备。这些在上面有详细说明。