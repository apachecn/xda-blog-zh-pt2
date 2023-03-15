# 一个 UI 4.1 通过 Noble ROM 到达三星 Galaxy S9 和 Note 9

> 原文：<https://www.xda-developers.com/samsung-galaxy-s9-note-9-one-ui-4-1-port-noble-rom-2-1/>

# 开发者将 One UI 4.1 移植到三星 Galaxy S9 和 Galaxy Note 9 上

One UI 4.1 的非官方端口现在可用于三星 Galaxy S9、Galaxy S9 Plus 和 Galaxy Note 9 的 Exynos 变体。

三星非常慷慨地提供了 One UI 4.1 更新。除了旗舰产品，韩国 OEM 厂商还推出了 Galaxy Note 10 Lite 等平价产品。这款手机由 Exynos 9810 处理器提供支持，这是一款 2018 年推出的 10 纳米八核 SoC，也是 Galaxy S9 和 Galaxy Note 9 的国际版本。不幸的是，这些设备甚至没有收到三星的 Android 11 更新，尽管理论上它们都有能力运行它。这促使 XDA 认可的开发商 [AlexisXDA](https://forum.xda-developers.com/m/alexisxda.6114446/) 将 One UI 4.1 风格的 Android 12 固件移植到 Galaxy S9 和 Galaxy Note 9 上。

One UI 4.1 端口被称为 **Noble ROM 2.1** ，兼容 Galaxy S9/S9 Plus 和 Galaxy Note 9 的韩国和全球版本。作为 [Noble ROM 2.0 版本](https://www.xda-developers.com/samsung-galaxy-s9-note-9-one-ui-4-port-noble-rom-2-android-12/)的继任者，新版本在最初的 Android 12 端口上进行了许多改进和错误修复。开发者最近推出了一个修复程序，进一步增加了对 PlayStation 5 DualSense 控制器的 HID 支持。

下面是 Noble ROM 2.1 版本的完整变更日志:

### Noble ROM 2.1 变更日志

*   **贵族 ROM 2.1**
    *   使用 OneUI 4.1 和三月份的补丁(HCV6)将基础更新到 N10+
    *   将 Magisk 更新至 v24.3
    *   固定 LED 通知
    *   固定相机滤镜
    *   OneUI4 相机中的固定前置单镜头
    *   固定共享 USB
    *   修正了 N9 上的 Hi Bixby 语音命令
    *   固定 USB C 耳机
    *   修复了 f2fs 引导循环安装
    *   修复了高级去模糊问题
    *   固定黑暗模式切换丢失
    *   固定无线快速充电
    *   修正了 4G 图标箭头
    *   启用双应用程序中的所有应用程序
    *   在照片编辑器/物体橡皮擦中增加了反射和阴影橡皮擦
    *   已移除，因为开发人员现已停止使用
    *   提高了总体性能
    *   提高了面部解锁和指纹解锁速度
    *   改进的安装脚本，现在 ROM 可以很容易地安装。
*   **Noble ROM 2.1 热修复程序**
    *   改善音质
    *   固定在阳光下锁屏黑屏
    *   改进的性能
    *   内核变更日志:
        *   固定 c 型到 c 型充电
        *   大 CPU 欠锁
        *   GPU 安全补丁
        *   更新的网络
        *   ZRAM 写回 lru 更新
        *   PS5 Hid 支持
        *   USB 更新
        *   通用优化
        *   工具链已更新

按照惯例，你必须首先解锁你的 Galaxy S9/Note 9 的引导程序，然后安装 TWRP 来刷新 ROM。值得注意的是，美国和加拿大的版本与这个定制的 One UI 4.1 版本不兼容，因为它们的骁龙 SoC 和锁定的引导加载程序。要了解更多特性和下载 ROM，请查看我们论坛上针对特定型号的讨论主题。

**下载基于 One UI 4.1 的 Noble ROM 2.1:[三星 Galaxy S9 和 S9 Plus](https://forum.xda-developers.com/t/4253997/) || [三星 Galaxy Note 9](https://forum.xda-developers.com/t/4244747/)**