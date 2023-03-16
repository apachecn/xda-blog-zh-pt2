# 在 Exynos 三星 Galaxy Note 8/Galaxy S8 上启用 4K@60fps 视频

> 原文：<https://www.xda-developers.com/enable-4k60fps-video-exynos-samsung-galaxy-note-8-galaxy-s8/>

以 60fps 的速度录制 4K 视频已经成为今年旗舰智能手机的一项流行功能。高通骁龙 845 是第一款支持这一功能的高通 SoC [，我们已经看到它被 OnePlus 6、三星 Galaxy S9、LG G7 ThinQ、三星 Galaxy Note 9 等手机采用。由于 Apple A11 和 A12 SoCs 的编码功能，苹果 iPhone X、iPhone XS 和 iPhone XR 也支持 4K@60fps 视频录制。海思的麒麟 SOC 还是没有 4K@60fps 编码支持(连](https://www.xda-developers.com/qualcomm-snapdragon-845-spectra-uhd-premium-video/)[麒麟 980](https://www.xda-developers.com/hisilicon-kirin-980-honor-magic-2-huawei-mate-20-pro/) 都没有这个功能)。另一方面，三星的[旗舰 exy nos SOC](https://www.xda-developers.com/samsung-unveils-exynos-9810-3rd-generation-custom-cpu-cores-mali-g72mp18-gpu/)在视频编码能力方面可以说已经领先于骁龙 SOC。

比如 2017 年推出的 Exynos 8895，[，官方支持 4K@60fps 视频录制。然而，高通骁龙 835 不支持这一功能，这就是为什么三星限制三星 Galaxy S8/Galaxy S8+和三星 Galaxy Note 8 以 30fps 的速度录制 4K 视频。三星禁用了这一功能，以便在其旗舰手机的骁龙和 Exynos 版本之间实现功能对等。(该公司在 Exynos Galaxy S9/S9+和 Galaxy Note 9 上禁用 4K@120fps 视频编码时也做了同样的事情。)](https://www.xda-developers.com/samsung-launches-the-exynos-9-series-8895-octa-core-processor-on-10nm-finfet-process-technology/)

这意味着 Exynos 三星 Galaxy S8、三星 Galaxy S8+和三星 Galaxy Note 8 的用户无法正式录制 4K@60fps 视频，尽管 Exynos 8895 SoC 确实具有这样的编码功能。

## 如何在 Exynos 三星 Galaxy Note 8 或 Galaxy S8 上启用 60FPS 的 4K 视频录制

然而，XDA 青年成员 [KunkerLV](https://forum.xda-developers.com/member.php?u=6187441) 现在[分享了一个脚本](https://forum.xda-developers.com/galaxy-note-8/how-to/guide-note8-4k60fps-t3842579)，非正式地在上述 2017 年 Exynos 驱动的三星旗舰手机上启用 4K@60fps 视频录制。好消息是方法**不需要 root** ，这意味着股票用户无需修改系统文件就可以轻松应用。

在 Exynos Galaxy S8/S8+和 Galaxy Note 8 上启用 4K@60fps 视频录制的步骤如下所示:

*   1.  下载[rubber big pepper . LG camera APK](https://forum.xda-developers.com/attachment.php?attachmentid=4596711&d=1537013470)并安装。
    2.  打开应用程序>点击设置>点击最后一个标签>点击“编辑相机脚本”
    3.  粘贴以下代码:

        ```
         preview-size=%pref_width%x%pref_height%
        video-size=%video_width%x%video_height%
        camera-mode=1
        cam_mode=1
        cam-mode=1
        video-hfr=60
        preview-fps-range=60000,60000 
        ```

    4.  点击“应用”。用户现在可以在他们的 Exynos Galaxy S8、Galaxy S8+和 Galaxy Note 8 上录制 4K@60fps 视频。

用户可以更改 4K@60fps 视频的视频录制比特率，XDA 论坛线程上的用户报告视频大小可以高达 750MB。从技术上讲，这个脚本使 2017 Exynos 三星 Galaxy 旗舰成为第一款能够录制 4K@60fps 视频的 Android 手机，尽管三星从未正式启用这一功能。用户现在可以取消功能限制，享受设备的全部编码功能。