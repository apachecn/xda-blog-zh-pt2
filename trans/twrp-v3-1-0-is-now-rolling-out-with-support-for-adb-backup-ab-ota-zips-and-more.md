# TWRP 3 . 1 . 0 版现在推出了对 ADB 备份、A/B OTA zip 等的支持

> 原文：<https://www.xda-developers.com/twrp-v3-1-0-is-now-rolling-out-with-support-for-adb-backup-ab-ota-zips-and-more/>

大约两周前，我们被告知[下一版本的 TWRP](https://www.xda-developers.com/twrp-v3-1-0-will-bring-support-for-backing-up-directly-to-your-pc/) 将支持通过一个被称为 ADB backup 的功能直接将文件备份到你的 PC 上。我们被告知，这个版本的 TWRP 将被标记为版本 3.1.0，并将很快推出。那就是现在。3.1.0 版本推出了前面提到的 **ADB 备份**功能以及几个值得注意的修复。

特别是，该更新支持在恢复过程中更新 **alpha/beta OTA。目前，这只会对谷歌 Pixel 或 Pixel XL 的用户有用，但随着更多设备开始搭载 Android 7.1 和 A/B 分区方案，更多用户可以利用这一功能。不过，某些 HTC 手机的用户现在可以高兴了，因为更新为一些手机上的数据分区解密提供了更好的支持。**

另一个需要注意的重大修复是，TWRP 将不再擦除为[直接启动功能](https://developer.android.com/training/articles/direct-boot.html)设置的某些应用程序的数据，一些用户在试图备份和恢复他们最喜欢的消息应用程序时发现，他们所有的消息都丢失了。不涉及太多细节，这个问题的要点是为直接引导功能设置的应用程序使用了[设备加密(DE)](https://source.android.com/security/encryption/file-based.html) 存储，而不是凭证加密(ce)存储。Android 7.0 开始将某些扩展属性(xattr)添加到存储在 DE storage 下的应用程序的数据文件夹中，但在此次更新之前，通过 TWRP 进行的备份并没有保存这些扩展属性。因此，当用户试图从缺少这些 xattrs 的备份中恢复数据文件夹时，Android 会删除整个数据文件夹。

最后，我们想指出的另一个变化是，TWRP 现在会要求你在重启前安装官方应用。这个请求，如果被拒绝，可能会被永久禁用，是用户在他们的设备上保持 TWRP 最新的方式，并支持恢复背后的真棒团队。如果你还没有，**在 [Play Store](https://play.google.com/store/apps/details?id=me.twrp.twrpapp) 上查看他们的应用程序！**

还有一些其他的变化我们没有提到，但是你可以看看下面这个更新的(大规模)变化日志的摘要。

* * *

### TWRP 版本 3.1.0 变更日志

1.  vold 解密在一些选定的 HTC 设备上，TWRP 现在将尝试使用系统分区的 vold 和 vdc 二进制文件和库来解密数据分区(nkk71 和 CaptainThrowback)

2.  adb backup 要将备份直接传输到您的 PC 或从您的 PC 传输，请参见此处的文档:https://github . com/omnirom/Android _ bootable _ recovery/commit/ce 8 f 83 c 48d 200106 ff 61 ad 530 c 863 b 15 c 16949d 9(big biff)

3.  调整 MTP 启动程序(mdmower)

4.  支持新的 Android 7.x xattrs 进行备份和恢复，以修复恢复后的数据丢失(Dees_Troy)

5.  支持 POSIX 文件功能备份和恢复，以修复 HTC 设备上的 VoLTE 和其他可能的问题(Dees_Troy)

6.  更好地向用户表明内部存储没有备份(Dees_Troy)

7.  改进自动确定 TW_THEME (mdmower)

8.  最小的 getcap 和 setcap 支持(_that)

9.  尝试在解密期间挂载 ext4 和 f2fs(jcadduono 和 Dees_Troy)

10.  用电源键关闭背光(mdmower)

11.  FDE 解密期间超时(Dees_Troy 和 nkk71)

12.  支持 FBE 解密以及备份和恢复 FBE 政策(Dees_Troy)

13.  启动插槽支持(Dees_Troy)

14.  重启时出现 TWRP 应用安装提示(Dees_Troy)

15.  支持 AB OTA 拉链(Dees_Troy)

16.  支持新的 Android 7.x 日志命令(Dees_Troy)

17.  将恢复源更新到 AOSP 7.1 (Dees_Troy)

18.  无数的错误修正和改进被太多人提及

* * *

否则，您可以在这里跟踪您的设备[的 TWRP 版本的进度，或者在这里](https://jenkins.twrp.me/)查看您的设备[的最新版本是否已经可用。享受更新吧，一定要尽你所能为这个项目做贡献，因为 TWRP 完全是一个由少数优秀的开发人员自发组织的社区。](https://twrp.me/Devices/)