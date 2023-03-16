# 如何解锁诺基亚 2.1 引导加载程序

> 原文：<https://www.xda-developers.com/unlock-nokia-2-1-bootloader/>

### 展开说明

**第一步:下载固件，固件包含服务引导程序文件**

你可以从 https://fih-firmware.hikaricalyx.com/hmd_en.html#e2m 下载

这种情况请下载 E2M-0390-0-00WW-B02 一个。如果你用的是 Android 9，下载 E2M-108C-0-00WW-B01。

然后，解压 E2M-0-0390-00WW-1-2-emmc _ apps boot _ service . zip 得到服务 bootloader 文件，解压密码为“WLBGFIH123”。

**第二步:启动手机至下载模式(Fastboot mode)**

您可以执行以下命令，然后在关机时连接手机，或者使用您熟悉的任何其他方法:

**第三步:Flash 服务引导程序**

代码:

```
fastboot oem dm-verity (md5_of_serial_number)
```

惊讶吧。这个命令在诺基亚 2.1 上仍然可用，甚至在 Android 9 的基础上，不知道为什么。

例如，如果您的序列号是 E2MGAHIKARICALYX，md5 校验和是 0 ab 1 B1 e 9 F3 aacc 85849341 cd5fb 21412，则命令将是:

代码:

```
fastboot oem dm-verity 0ab1b1e9f3aacc85849341cd5fb21412
```

你可以简单地搜索一个网站来计算字符串的 md5 校验和。

和闪存服务引导程序:

代码:

```
fastboot flash aboot /path/to/E2M-0-0390-00WW-1-2-emmc_appsboot_service.mbnfastboot reboot-bootloader
```

**第四步:解锁引导程序**

您的手机将重新启动，以服务引导加载程序。然后使用以下命令授予解锁权限:

代码:

```
fastboot oem dm-verity (md5_of_serial_number)fastboot oem fih onfastboot oem devlock allow_unlock
```

然后解锁引导加载程序:

代码:

```
fastboot oem flashing unlock_critical
```

当您的手机正在清除用户数据时，则:

代码:

```
fastboot oem alive(wait for triggering to download mode)fastboot oem dm-verity (md5_of_serial_number)fastboot oem fih onfastboot oem devlock allow_unlockfastboot oem unlock-go
```

完成了。您的手机已解锁引导加载程序。