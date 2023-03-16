# 自定义主题现在可以在有底层的 Android P 设备上运行

> 原文：<https://www.xda-developers.com/custom-themes-android-p-root-substratum/>

# 自定义主题现在可以在有底层的 Android P 设备上运行

流行的第三方主题管理器 Substratum 已经更新，支持根 Android P 设备，如 Google Pixel、Google Pixel 2 等。

Android P 的用户界面变化最初遇到了一些争议(主要是因为与 iOS 的相似性以及对带缺口显示屏的设备的明显适应)，但随着人们习惯了这些变化，批评似乎已经平息了一些。在过去的几年中，Android 爱好者一直渴望的一个功能就是定制主题。Android Oreo 引入了索尼的主题框架，受欢迎的第三方 Substratum 主题管理器接入该框架，以提供[无根定制主题](https://www.xda-developers.com/custom-themes-android-oreo-substratum/)。不幸的是，Android P [通过要求覆盖图由系统](https://www.xda-developers.com/rootless-custom-themes-android-p/)签名[来阻止第三方覆盖图](https://www.xda-developers.com/android-p-blocks-custom-overlays-substratum-themes/)的安装。然而，对于那些渴望在 Android P 上获得全系统黑暗主题的人来说，Substratum 团队刚刚发布了一个支持根设备的新测试版。

Android 8.1 奥利奥增加了部分黑暗主题，但这个主题有一些明显的缺点。首先，这个主题只有在使用深色壁纸时才会被应用(尽管未来的更新将允许这个主题被手动应用到 T2)。)其次，它只是 Google Pixel 启动器的主题部分，快速设置磁贴和音量面板，而不是整个系统 UI 和框架。相比之下，无根的底层给了用户安装任何他们想要的自定义主题的自由(有时[自担风险](https://www.xda-developers.com/why-app-updates-sometimes-break-substratum-themes/))。)谷歌禁止安装第三方覆盖，但如果你通过 Magisk、SuperSU 或 LineageOS ' addonSU 拥有 root 访问权限，那么你就可以绕过这些限制。

最新的测试版本是 997，可以在任何安装了 Android P 测试程序的设备上运行。这包括以下设备:

*   谷歌像素
*   谷歌像素 XL
*   谷歌像素 2
*   谷歌像素 2 XL
*   基本电话
*   诺基亚 6.1 ( [中国](https://www.xda-developers.com/nokia-6-1-nokia-7-nokia-8-sirocco-android-p-beta/))
*   诺基亚 7 ( [中国](https://www.xda-developers.com/nokia-6-1-nokia-7-nokia-8-sirocco-android-p-beta/))
*   诺基亚 7 Plus
*   诺基亚 8 Sirocco ( [中国](https://www.xda-developers.com/nokia-6-1-nokia-7-nokia-8-sirocco-android-p-beta/))
*   一加 6
*   Oppo R15 Pro
*   索尼 Xperia XZ2
*   Vivo X21UD
*   Vivo X21
*   小米米混合泳 2S

以下是该版本的完整变更日志:

### 底层公开发行版 995 和测试版 997 变更日志

总结:

*   稳定版 995 为 Sungstromeda 模式带来了更多的修复，以及更新的翻译。
*   测试版 997 的目标是 Android P 对根设备的支持。

完整变更日志

*   测试版 997
    *   软件包:确保已安装的软件包具有有效的路径
    *   SettingsFragment:去掉三元运算符意大利面，占 Android P
    *   更新了 P-fix 以利用现已完成的 API
    *   OverlaysManager:不要等待 P 上的意向响应
    *   ThemeManager:为 P 实现卸载
    *   底层:实现对 Android P 的初始支持
*   公开发布 995
    *   SubstratumTile:使用 FLAG_ACTIVITY_NEW_TASK 启动
    *   底层:更新所有梯度相关性
    *   底层:重新添加一些语言
    *   底层:更新本地化
    *   展示活动:小规模清理
    *   SubstratumUI:修复 API 27 的导航栏
    *   OverlaysAdapter:删除蓝色状态
    *   SubstratumCleanup:删除更多不完整的本地化内容
    *   SubstratumCleanup:删除所有不完整/未使用的本地化
    *   信息活动:修复乱码变量名
    *   FileDownloader:使用带资源的 try 重写
    *   相当自动化的棉绒清理
    *   使用 HashSet 来避免重复的覆盖

## 如何安装底层和设置自定义主题

点击加入 [beta 计划，然后从下面的 Play Store 下载应用程序。访问 XDA](https://play.google.com/apps/testing/projekt.substratum) 的[底层论坛，了解主题管理器的最新消息。如果你是根用户，安装一个自定义主题是非常简单的。你可以](https://forum.xda-developers.com/apps/substratum)[遵循我们之前的 Android 奥利奥指南](https://www.xda-developers.com/custom-themes-android-oreo-substratum/)，除了你可以完全跳过第一部分。