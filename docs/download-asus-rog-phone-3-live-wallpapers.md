# 下载华硕 ROG 手机 3 壁纸和移植活壁纸

> 原文：<https://www.xda-developers.com/download-asus-rog-phone-3-live-wallpapers/>

2018 年，华硕冒险进入当时新生的游戏智能手机市场，将其超受欢迎的玩家国度(ROG)品牌扩展到移动设备。虽然第一代华硕 ROG 手机因其高昂的价格而反应冷淡，但 ROG 手机 II 因其极具竞争力的价格而受到好评；华硕是时候再次复制这一成功了。华硕 ROG 手机 3 刚刚正式宣布，它配备了令人难以置信的规格，如骁龙 865 Plus，144Hz AMOLED 显示屏，高达 16GB 的内存，RGB 照明，以及许多比上一代产品改进的游戏功能和附件。即使你无法体验 ROG 系列中最新游戏智能手机的糟糕硬件，你也可以获得该设备附带的 4 张实时壁纸和 29 张壁纸。

**[华硕 ROG 手机 3 XDA 论坛](https://forum.xda-developers.com/asus-rog-phone-3)**

有 4 张实时壁纸，其中两张以 60fps 渲染，另外两张以 30fps 渲染。所有这些动态壁纸都以视频的形式提供，分辨率为 2352 x 2353 像素。感谢 XDA 公认的贡献者 [linuxct](https://forum.xda-developers.com/member.php?u=4787101) ，他因移植动态壁纸和其他 APK mod 的工作[而闻名，我们已经修改了 4 个动态壁纸 APK 的版本，你可以安装在任何运行 Android 9 Pie 或更高版本的 Android 设备上。](https://www.xda-developers.com/download-miui-12-super-earth-mars-live-wallpapers-ported-other-devices/)

此外，共有 29 张静态壁纸，其中 12 张的分辨率为 2340 x 1080 像素，9 张的纵横比为 1:1，分辨率为 2340 x 2340 像素。剩下的 8 张壁纸是取自前述 4 张现场壁纸的剧照。这些来自实时壁纸的快照有两个版本，当 ROG 手机 3 进入 X 模式时，它们会改变颜色，这是一种提高游戏性能的特殊模式。

上面添加的图片仅用于本文的预览，你可以通过下面的链接获得这些高分辨率的壁纸。

**[下载华硕 ROG 手机 3 壁纸](https://www.androidfilehost.com/?fid=8889791610682897984)**

**XDA 回顾:** [华硕 ROG Phone 3 回顾:游戏智能手机之王回来了](https://www.xda-developers.com/asus-rog-phone-3-review/)

## 如何安装华硕 ROG 手机 3 的动态壁纸端口

为了让动态壁纸像开发者 linuxct 解释的那样工作，你需要安装一个他制作的名为 X-Mode Toggler 的配套应用。这个应用程序增加了一个快速设置磁贴，当切换时，欺骗实时壁纸认为 X 模式是活跃的。这触发了动态壁纸外观的变化。这在非 ROG 设备上是必要的，因为 X 模式只存在于 ROG 设备上。

首先，从下面的链接下载 ZIP 文件:

**[下载华硕官方 ROG 手机 3 动态壁纸移植 APKs by linuxct](https://www.androidfilehost.com/?fid=8889791610682897978)**

然后，解压 zip 文件并安装动态壁纸 APKs。接下来，打开命令提示符或终端窗口，输入以下 ADB shell 命令:

```
 adb shell pm grant space.linuxct.rogcontroller android.permission.WRITE_SECURE_SETTINGS 
```

(如果你还没有在你的电脑上设置 ADB，我们有一个[教程告诉你如何在这里设置](https://www.xda-developers.com/install-adb-windows-macos-linux/)。)最后，使用 X-Mode Toggler 的快速设置磁贴来“启用”X-Mode。