# 动态 Android 将允许开发者在任何 Android Q 设备上测试 AOSP

> 原文：<https://www.xda-developers.com/android-q-dynamic-android-aosp-gsi/>

多亏了 Project Treble(T1 ),智能手机制造商提供 Android Pie 软件更新的速度比他们提供 Android Oreo 更新的速度更快，至少对于旗舰智能手机来说是这样。不过，谷歌不想看到只有原始设备制造商从 Project Treble 中获益。该公司此前[曾表示有兴趣](https://www.xda-developers.com/google-test-android-q-project-treble-gsi/)为开发者发布 Android Q 的通用系统映像(GSI)，这样他们就不必依赖仿真器，使用[云服务](https://www.xda-developers.com/genymotion-cloud-google-cloud-platform/)，或者等待自己设备上的更新来测试最新 API 级别的应用程序。理论上，发布 GSI 应该允许任何拥有 Project Treble 兼容设备(最初是 Android 8.0 Oreo 和更高版本，但现在被认为只有使用 Android 9 Pie 推出的设备)的开发者测试最新的 Android 版本。开发人员只需在其现有软件安装的基础上刷新系统映像，无需定制恢复、引导或供应商映像。

然而，当前的 GSI 安装过程存在几个问题。首先，你需要一个解锁的引导加载程序，这在华为或 Honor 设备(无需向 T2 支付费用)、HMD Global 的诺基亚设备(不包括 T4 的诺基亚 8)或美国运营商品牌的设备上是不可能的。接下来，[过程](https://www.xda-developers.com/flash-generic-system-image-project-treble-device/)对于任何不熟悉通过快速启动来闪烁图像的人来说将会很难。最后，现在刷新 GSI 将需要您完全擦除内部存储，这意味着您可能需要一个备用设备来测试。现在，闪烁 GSI 只是原始设备制造商用来在他们的设备上测试项目三重兼容性的东西，除此之外，它只对顽固的定制 ROM 爱好者有吸引力。谷歌新的“动态安卓”项目可能会改变这一点。

## 动态 Android——在任何 Android Q 设备上轻松测试 AOSP GSI

在过去的几个月里，谷歌一直在研究一种无需解锁引导程序就能安全启动 GSI 的方法。简而言之，谷歌正在开发一款拥有特殊权限的应用，允许它下载 GSI，为其保留存储空间，并将 GSI 标记为可启动。这个项目有几个组成部分，所以让我们逐一讨论。

### 动态 Android 和 Android On Tap

Android Q 增加了两项新服务:动态 Android 和 Android On Tap 服务。动态 Android 处理 GSI 的安装，而 Android On Tap 通过回调和广播通知系统应用程序。例如，如果设备受到 PIN、密码或模式的保护，Android On Tap 会提醒 KeyguardManager 要求用户确认安装请求。当用户启动 GSI 时，AOT 也会提醒用户。

根据对“DynamicAndroidManager”的描述，这项服务“提供了一种临时使用新 Android 图像的机制。”安装后，设备可以使用新创建的/data 重新启动到新安装的映像中。在 GSI 中重新引导会使用户返回到原始系统映像，但是新安装的映像及其数据只是被禁用，而不会被删除。但是，如果用户选择这样做，可以完全删除 GSI 及其数据。

来源:[ [1](https://android-review.googlesource.com/c/platform/frameworks/base/+/861575) ，[ [2](https://android-review.googlesource.com/c/platform/frameworks/base/+/862409) ，[ [3](https://android-review.googlesource.com/c/platform/frameworks/base/+/868930) ，[ [4](https://android-review.googlesource.com/c/platform/system/gsid/+/876972) ]

### GSID

GSI 守护程序在/data 分区中分配空间来存储 GSI 映像及其数据，并使映像可引导。GSI 的元数据存储在/metadata 中，而 GSI 本身及其数据存储在/data/gsi 中。默认情况下，GSID 为新安装的 GSI 分配 8GB 用户数据。一般来说，GSID 在开始安装之前会寻找至少 40%的可用空间。最后，出于显而易见的原因，该守护程序会阻止用户在 GSI 中安装 GSI。

来源:[ [1](https://android-review.googlesource.com/c/platform/system/gsid/+/880716) ，[ [2](https://android-review.googlesource.com/c/platform/system/gsid/+/876155) ，[ [3](https://android-review.googlesource.com/c/platform/system/gsid/+/863812) ，[ [4](https://android-review.googlesource.com/c/platform/system/gsid/+/864937) ]

### 安全性

新安装的 EXT4 系统镜像(system_gsi 挂载到/system)启用了 Android 验证启动(AVB)。谷歌也为新服务实施了 SELinux 政策。最后，安装 GSI 需要应用程序具有新的 MANAGE_DYNAMIC_ANDROID 权限。这是一个签名级别的权限，这意味着应用程序必须由 OEM 签名。

来源:[ [1](https://android-review.googlesource.com/c/platform/system/core/+/889973) ，[ [2](https://android-review.googlesource.com/c/platform/system/sepolicy/+/864995)

### ADB 和 Fastboot 命令

GSIs 也可以通过新的 ADB 命令安装。新的 ADB gsi_tool shell 命令将允许用户禁用、重新启用、安装和保留用户数据、安装和创建用户数据、安装和擦除用户数据或检查安装状态。

```
 gsi_tool - command-line tool for installing GSI images.

Usage:
  gsi_tool <disable|install|wipe|status> [options]

  disable Disable the currently installed GSI.
  enable Enable a previously disabled GSI.
  install Install a new GSI. Specify the image size with

  wipe Completely remove a GSI and its associated data
  status Show status 
```

将添加两个新的 fastboot 命令来管理 GSI，尽管 fastboot 安装不受支持，因为 fastboot 不能挂载 userdata。

```
 fastboot gsi wipe
fastboot gsi disable 
```

来源:[ [1](https://android-review.googlesource.com/c/platform/system/gsid/+/871412) ，[ [2](https://android-review.googlesource.com/c/platform/system/core/+/889793)

## 这对谁有利？

我想说，应用程序开发人员将能够利用动态 Android 和 Android On Tap，但我不完全确定。虽然谷歌对此表示了兴趣，但不能保证非谷歌原始设备制造商发布的每个 Android Q 版本都会有这个功能。为了在设备上利用这一点，该软件需要一个 GSI picker 应用程序，该应用程序由与 ROM 相同的证书签名。由于 SELinux 政策的原因，我也不确定在没有 ADB root 的情况下从 ADB 安装 GSI 是否可行。 **更新:**一项新的[承诺](https://android-review.googlesource.com/c/platform/system/gsid/+/894013)确认亚行根将被要求使用 GSI 工具。如果这不是为了让应用程序开发人员在一个干净的 Android 版本上测试他们的应用程序，那么它可能只会让那些希望在他们的设备上测试兼容性测试套件(CTS)和供应商测试套件(VTS)的 OEM 工程师受益。

*特别感谢 XDA 认可开发者 [luca020400](https://forum.xda-developers.com/member.php?u=5778309) 对本文的协助。*