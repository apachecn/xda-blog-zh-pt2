# TWRP 和 LineageOS 17.1 现可用于三星 Galaxy S6 Lite

> 原文：<https://www.xda-developers.com/unofficial-twrp-lineageos-17-1-samsung-galaxy-s6-lite/>

三星是少数几家仍押注平板电脑市场的安卓原始设备制造商之一。韩国原始设备制造商早在今年四月就发布了一款中端平板电脑——Galaxy Tab S6 Lite(T1 ),几个月后,[也进入了印度。作为一款支持三星 S Pen 的经济型平板电脑，该设备提供了一些可靠的规格，如 Exynos 9611 SoC，4GB 内存，64GB 存储，配有 microSD 插槽用于扩展，10.4 英寸 WUXGA+ TFT LCD 显示屏，以及双 AKG 调谐扬声器和杜比音频。如果你是那种喜欢修改他们的小工具的人，那么你会对 Galaxy Tab S6 Lite 感到满意，因为该设备现在已经获得了非官方的 TWRP 版本以及相当稳定的 LineageOS 17.1 版本。](https://www.xda-developers.com/samsung-galaxy-tab-s6-lite-one-ui-2-s-pen-exynos-launch-india/)

**[三星 Galaxy Tab S6 Lite 论坛](https://forum.xda-developers.com/galaxy-tab-s6-lite)**

XDA 初级成员 [Linux4](https://forum.xda-developers.com/member.php?u=10467607) 已经将 TWRP 定制恢复(v3.4.0-0)移植到这款平板电脑上。您可以按照下面链接的 XDA 线程中的说明在您的设备上下载并刷新自定义恢复，之后您将能够刷新 Magisk、一些 mod，甚至是设备上的自定义 ROM。然而，由于这是 TWRP 恢复的早期版本，一些特性不能像预期的那样工作。例如，使用 ADB 的侧向加载被破坏，并且不支持在库存三星 ROM 上的数据解密。

**[下载三星 Galaxy Tab S6 Lite 非官方 TWRP 3 . 4 . 0](https://forum.xda-developers.com/galaxy-tab-s6-lite/development/recovery-twrp-3-4-0-galaxy-tab-s6-lite-t4166985)**

基于 Android 10 的 LineageOS 17.1 ROM 的非官方版本也可用于 Galaxy Tab S6 Lite，由同一位开发者提供。Linux4 的构建使用了开发伙伴 [modpunk](https://forum.xda-developers.com/member.php?u=4297219) 和 [derf elot](https://forum.xda-developers.com/member.php?u=4063475) 的工作作为基础，他们为 Galaxy S10 系列移植了 [LineageOS。要在 Tab S6 Lite 上安装 ROM，首先需要在你的设备上安装前面提到的 TWRP 版本。定制 ROM 带有强制 SELinux，从安全角度来看，这确实是一大优势。LTE 和 Wi-Fi 版本有单独的可擦写拉链，因此请选择适合您型号的拉链。](https://forum.xda-developers.com/galaxy-s10/samsung-galaxy-s10--s10--s10-5g-cross-device-development-exynos/rom-lineageos-17-1-beta0-s10e-update-t4076585)

**[为三星 Galaxy Tab S6 Lite](https://forum.xda-developers.com/galaxy-tab-s6-lite/development/rom-lineageos-17-1-galaxy-tab-s6-lite-t4167037)** 下载非官方 LineageOS 17.1

值得一提的是，在设备上安装定制软件将永久关闭 KNOX，因此您将无法访问 Samsung Pay 和安全文件夹等安全功能。尽管如此，如果你不介意这些权衡，那么请放心，继续在你的平板电脑上享受售后发展。