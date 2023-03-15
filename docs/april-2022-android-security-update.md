# 2022 年 4 月 Android 安全更新现已正式发布

> 原文：<https://www.xda-developers.com/april-2022-android-security-update/>

谷歌每月都会为 Android 操作系统发布一批安全补丁和漏洞修复，通常是在每月的第一个星期一。果然，现在是四月的第一个星期一，新的安全更新开始向谷歌 Pixel 手机和一些第三方设备推出。

## 2022 年 4 月 Android 安全更新公告

2022 年 4 月的安全更新分为两个不同的补丁级别——2022-04-01，修复适用于大多数 Android 设备的安全问题；2022-04-05，仅适用于某些手机和平板电脑的补丁。2022-04-01 安全级别包含 7 个针对 Android 框架的安全补丁，它们都被标记为高严重性。还有两个针对媒体框架的补丁和三个针对系统的补丁，以及两个针对项目主线组件的补丁。

值得注意的是，更新[似乎不包含针对](https://twitter.com/suka_hiroaki/status/1511029748322996226)[“脏管道”安全漏洞](https://www.xda-developers.com/dirty-pipe-linux-vulnerability-root-android/)的修复，该漏洞允许软件覆盖只读文件中的数据。该漏洞已经被[用于三星 Galaxy S22 和谷歌 Pixel 6 的临时 root 访问](https://www.xda-developers.com/dirty-pipe-root-demo-samsung-galaxy-s22-google-pixel-6-pro/)。

## 像素更新公告/功能更新

谷歌还包括一些专门影响 Pixel 设备的安全补丁，修复了 Android 内核、摄像头、引导程序和无线连接。主要的内核修复是针对安全漏洞 [CVE-2021-34866](https://cve.report/CVE-2021-34866) ，该漏洞允许应用程序提升权限并在特定版本的 Linux 内核上执行任意代码。

Pixel 手机也有一些错误修复，如下所示。谷歌在这次更新中没有提到任何新功能，但考虑到上个月的更新是 Android 12L/12.1，这是有道理的。

### 2022 年 4 月谷歌像素更新

**电池&电源**

*   某些配件对无线充电性能的额外改进*[2]。

**摄像机**

*   修复了导致某些应用程序中的前置摄像头预览放大显示的问题*[2]。
*   修正了相机预览中偶尔出现绿屏的问题*[2]。

**用户界面**

*   修复了在某些情况下以画中画(PIP)模式使用应用程序时系统 UI 崩溃的问题*[1]。
*   修复了设置某些动态壁纸时导致错误消息显示的问题*[1]。
*   修正了在某些情况下更换壁纸后通知阴影和快速设置不可见的问题*[1]。
*   修正了取消应用程序抽屉中的搜索时偶尔导致动画显示不正确的问题*[1]。
*   修正了当对讲处于活动状态时，偶尔会阻止概览屏幕中的导航的问题*[1]。
*   修正了在第三方启动器中使用 3 键导航时，偶尔阻止最近按钮显示概览的问题*[1]。

*[1]包含在像素 3a、像素 3a XL、像素 4、像素 4 XL、像素 4a、像素 4a (5G)、像素 5、像素 5a (5G)、像素 6 和像素 6 Pro 上

*[2]包含在 Pixel 6 和 Pixel 6 Pro 中

与最近的一些每月更新不同，Pixel 6 和 Pixel 6 Pro 不必比旧的 Pixel 手机等待更长时间。谷歌表示，从今天开始，2022 年 4 月的更新将推广到所有 Pixel 设备，一些第三方手机已经有了它 Galaxy S21 的 Exynos 版本[刚刚收到了 4 月的补丁，软件版本为 G99xBXXS4CVCG](https://forum.xda-developers.com/t/cvcg-april-galaxy-s21-ultra-5g-official-firmware-sm-g998b-4th-april.4218529/post-86687605) 。

如果你不想等待谷歌向你的 Pixel 手机推送更新，请查看我们的 [Android 12L 下载文章](https://www.xda-developers.com/how-to-download-android-12/#apr2022)以获取最新的 OTA 文件和工厂图像。

**来源:** [像素手机帮助](https://support.google.com/pixelphone/thread/158550017/google-pixel-update-april-2022?hl=en)，[像素更新公告](https://source.android.com/security/bulletin/pixel/2022-04-01)，[安卓安全公告](https://source.android.com/security/bulletin/2022-04-01)