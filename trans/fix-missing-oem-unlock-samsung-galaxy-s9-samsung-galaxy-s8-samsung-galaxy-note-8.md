# 如何修复三星 Galaxy S9/S8/Note 8 上缺失的 OEM 解锁键

> 原文：<https://www.xda-developers.com/fix-missing-oem-unlock-samsung-galaxy-s9-samsung-galaxy-s8-samsung-galaxy-note-8/>

在任何运行 Android 5.0 Lollipop 和更高版本的智能手机上，你可能会在开发者选项中找到一个名为“OEM 解锁”的选项。通过切换此选项，您将能够解锁设备上的引导加载程序。解锁引导加载程序可以让你安装一个自定义恢复，如 TWRP，根你的设备访问系统文件，闪存自定义 rom，修改内核，等等。如果你拥有三星 Galaxy S8、三星 Galaxy Note 8 或三星 Galaxy S9 的国际/Exynos 版本，并且你缺少 OEM 解锁开关，那么有一个可用的修复程序。

三星允许解锁国际版手机的引导程序。但在三星 Galaxy S8、三星 Galaxy S9 和三星 Galaxy Note 8 上，“OEM 解锁”选项只有在激活设备并向设备添加三星或谷歌账户 7 天后才可用。如果你不想等 7 天，或者即使 7 天后按钮仍然不见了，XDA 资深会员 [altai1963](https://forum.xda-developers.com/member.php?u=8161473) 已经[发布了关于如何修复三星 Galaxy S8/S8+、三星 Galaxy S9/S9+和三星 Galaxy Note 8 上丢失的“OEM 解锁”按钮的说明](https://forum.xda-developers.com/showpost.php?p=76888852&postcount=4)。后者尚未测试，但我们确信它也能工作。

事不宜迟，让我们开始吧:

## 修复三星 Galaxy S9/S8/Note 8 上丢失的 OEM 解锁开关

1.  首先，在你的 Galaxy 设备上打开设置 app
2.  转到常规管理>日期和时间；
3.  取消选中“自动日期和时间”；
4.  应该会出现新的选项。点击“设置日期”并选择上个月的任何日期，这样我们就可以欺骗系统认为我们已经拥有该设备超过 7 天了。在这种情况下，我们选择 5 月 10 日；
5.  退出。在设置中，进入关于手机>软件信息；
6.  点击 7 次内部版本号以激活开发者选项；
7.  退出。在设置中，转到新添加的开发者选项；
8.  取消勾选“自动更新系统”；
9.  退出。转到软件更新；
10.  取消选中“自动下载更新”；
11.  点击“手动下载更新”。它可能会抛出一个错误，但是不要担心，那绝对没问题；
12.  重新启动您的设备；
13.  就是这样！“OEM 解锁”选项现在应该可以在开发者选项中使用了。

按照说明进行操作后，您将能够解锁全新 Galaxy 设备上的引导加载程序。正如我已经提到的，这种方法已经在三星 Galaxy S8、三星 Galaxy S8+、三星 Galaxy S9 和三星 Galaxy S9+上进行了测试，但三星 Galaxy Note 8 理论上也应该可以工作。